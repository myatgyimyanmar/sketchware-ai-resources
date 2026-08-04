# Sketchware Pro V7 — AI Training Resource Repository

> **Purpose:** This repository contains the complete source code and documentation of **Sketchware Pro V7.0.0 (GitHub Stable Release)** structured specifically for AI agent skill training. An AI that reads this repository should fully understand how Sketchware Pro V7 is architected, how projects are stored, and how to generate error-free projects programmatically.

---

## Table of Contents

1. [What is Sketchware Pro V7](#1-what-is-sketchware-pro-v7)
2. [App Architecture Overview](#2-app-architecture-overview)
3. [Project File System](#3-project-file-system)
4. [SWB Backup File Format](#4-swb-backup-file-format)
5. [View System — UI Components](#5-view-system--ui-components)
6. [Block System — Logic Coding](#6-block-system--logic-coding)
7. [Event System](#7-event-system)
8. [Component System](#8-component-system)
9. [Library System](#9-library-system)
10. [Custom Blocks System](#10-custom-blocks-system)
11. [File Index — Source Code Map](#11-file-index--source-code-map)
12. [Data Format Reference](#12-data-format-reference)
13. [Error Messages Reference](#13-error-messages-reference)

---

## 1. What is Sketchware Pro V7

Sketchware Pro V7 is an Android application development tool that runs **on Android devices**. It allows developers to build Android apps visually using:

- **Drag-and-drop UI builder** (Views)
- **Visual block-based coding** (Logic Blocks)
- **Firebase integration** (Realtime Database, Storage, Auth)
- **Custom Gradle libraries** (Local Libraries)
- **Custom Blocks** (user-defined reusable code blocks)

The V7.0.0 stable release is the open-source fork of the original Sketchware, published at:
`https://github.com/Sketchware-Pro/Sketchware-Pro`

### Minimum Requirements
- Android device running API 21+ (Android 5.0)
- Internet connection (for Firebase, libraries)
- The APK itself targets API 33

---

## 2. App Architecture Overview

```
Sketchware Pro V7 App
│
├── Project Editor
│     ├── FILE Tab       → Manage activities, custom views
│     ├── VIEW Tab       → UI layout design (drag & drop views)
│     ├── EVENT Tab      → Add onClick, onResume, etc.
│     ├── LOGIC Tab      → Connect blocks to events
│     ├── LIBRARY Tab    → Enable Firebase, AdMob, Google Map
│     └── CONFIG Tab     → App name, package, colors, permissions
│
├── Build System
│     ├── Java code generation (a.a.a.Jx)
│     ├── XML layout generation (a.a.a.Ox)
│     ├── AndroidManifest generation (a.a.a.Ix)
│     ├── D8/R8 DEX compiler
│     └── APK packager + signer
│
├── Custom Blocks Manager
│     ├── Global custom blocks (.sketchware/data/system/extra_block)
│     ├── Per-project custom blocks (.sketchware/data/{sc_id}/custom_blocks)
│     └── Palette manager (.sketchware/data/system/palette)
│
└── Backup/Restore
      ├── .swb file = ZIP with AES-128-CBC encrypted data
      └── Key/IV = "sketchwaresecure" (16 bytes UTF-8)
```

### Key Package Structure

| Package | Role |
|---|---|
| `com.besome.sketch.*` | Core original Sketchware classes (UI beans, editors) |
| `a.a.a.*` | Obfuscated core logic (code generators, file system) |
| `mod.hey.studios.*` | Major contributor features (backup, block manager, src editor) |
| `mod.agus.jcoderz.*` | Block/event/component extra features |
| `mod.hilal.saif.*` | BlocksHandler, events, config activity |
| `mod.jbk.*` | Build system, diagnostics, utilities |
| `dev.aldi.sayuti.*` | Local library manager |
| `pro.sketchware.*` | Modern refactored code, utilities, activities |

---

## 3. Project File System

All Sketchware Pro data is stored in internal storage at `.sketchware/`:

```
/sdcard/.sketchware/
│
├── mysc/
│     └── list/
│           └── {sc_id}/            ← One folder per project
│                 └── project        ← AES-encrypted JSON (project metadata)
│
├── data/
│     └── {sc_id}/                  ← Project data folder
│           ├── file                 ← AES-encrypted: activity/customview list
│           ├── library              ← AES-encrypted: Firebase/AdMob config
│           ├── view                 ← AES-encrypted: UI layout data
│           ├── logic                ← AES-encrypted: block/event/component data
│           ├── resource             ← AES-encrypted: images/fonts/sounds list
│           ├── permission           ← Plain JSON: Android permissions array
│           ├── build_config         ← Plain JSON: dexer, java version
│           ├── local_library        ← Plain JSON: Gradle dependencies array
│           ├── custom_blocks        ← Plain JSON: per-project custom blocks
│           ├── proguard             ← Plain JSON: ProGuard on/off
│           ├── proguard-rules.pro   ← Plain text: ProGuard rules
│           └── stringfog            ← Plain JSON: StringFog on/off
│
├── resources/
│     └── {sc_id}/                  ← Project resources
│           ├── fonts/
│           ├── icons/
│           ├── images/
│           └── sounds/
│
├── libs/
│     └── local_libs/               ← Global custom Gradle libraries (.jar/.aar)
│
└── data/
      └── system/
            ├── extra_block          ← Global custom blocks JSON
            ├── palette              ← Global custom block palettes JSON
            ├── events.json          ← Custom activity events
            └── listeners.json       ← Custom component listeners
```

### sc_id (Project ID)
- Every project has a unique numeric string ID called `sc_id`
- Example: `"700"`, `"1"`, `"23"`
- Referenced in: file paths, project JSON, backup filenames

### Encryption
```
Algorithm : AES/CBC/PKCS5Padding
Key       : "sketchwaresecure"  (16 bytes, UTF-8)
IV        : "sketchwaresecure"  (16 bytes, UTF-8)
Files     : project, file, library, view, logic, resource
```
Source: `BackupFactory.java` → `getProject()` + `writeEncrypted()`

---

## 4. SWB Backup File Format

A `.swb` file is a standard **ZIP archive** with the following entry structure:

```
MyProject.swb  (ZIP)
│
├── project                          ← AES-encrypted JSON (project metadata)
├── data/
│     ├── file                       ← AES-encrypted
│     ├── library                    ← AES-encrypted
│     ├── view                       ← AES-encrypted
│     ├── logic                      ← AES-encrypted
│     ├── resource                   ← AES-encrypted
│     ├── permission                 ← Plain JSON
│     ├── build_config               ← Plain JSON
│     ├── local_library              ← Plain JSON
│     ├── proguard                   ← Plain JSON
│     ├── proguard-rules.pro         ← Plain text
│     ├── stringfog                  ← Plain JSON
│     ├── custom_blocks              ← Plain JSON
│     └── Injection/
│           └── androidmanifest/
│                 └── app_components.txt
│
└── resources/
      ├── images/
      │     ├── .nomedia
      │     └── {image files}
      ├── sounds/
      │     └── .nomedia
      └── fonts/
            └── .nomedia
```

### Restoring a SWB
When Sketchware restores a `.swb`, it:
1. Reads the `project` entry → decrypts → extracts `sc_id` for new project
2. Copies `data/*` files to `.sketchware/data/{new_sc_id}/`
3. Copies `resources/*` to `.sketchware/resources/{subtype}/{new_sc_id}/`
4. Optionally copies `local_libs/` (user is asked)

Source: `BackupFactory.java` → `restore()` method

---

## 5. View System — UI Components

### View JSON Format (inside `data/view`)

The `data/view` file is AES-encrypted text containing sections separated by newlines.
Each section starts with `@{ActivityName}.xml` header.
Each view is one JSON object per line.

```
@splash.xml
{"adSize":"","adUnitId":"","alpha":1.0,"checked":0,"choiceMode":0,"clickable":1,"convert":"LinearLayout","customView":"","dividerHeight":1,"enabled":1,"firstDayOfWeek":1,"id":"root_ll","image":{"resName":"default_image","rotate":0,"scaleType":"CENTER"},"indeterminate":"false","index":0,"inject":"","layout":{"backgroundColor":-16777216,"borderColor":-16740915,"gravity":0,"height":-1,"layoutGravity":0,"marginBottom":0,"marginLeft":0,"marginRight":0,"marginTop":0,"orientation":1,"paddingBottom":0,"paddingLeft":24,"paddingRight":24,"paddingTop":0,"weight":0,"weightSum":0,"width":-1},"max":100,"parent":"root","parentType":0,"preId":"root_ll","preIndex":0,"preParentType":0,"progress":0,"progressStyle":"?android:progressBarStyle","scaleX":1.0,"scaleY":1.0,"spinnerMode":1,"text":{"hint":"","hintColor":-10453621,"imeOption":0,"inputType":1,"line":0,"singleLine":0,"text":"","textColor":-16777216,"textFont":"default_font","textSize":12,"textType":0},"translationX":0.0,"translationY":0.0,"type":0}
@auth.xml
...
```

### View Types (`convert` field + `type` integer)

| `type` | `convert` string | Description |
|---|---|---|
| `0` | `LinearLayout` | Vertical/Horizontal container |
| `1` | `RelativeLayout` | Relative positioning container |
| `2` | `ScrollView` | Vertical scrollable container |
| `3` | `Button` | Clickable button |
| `4` | `TextView` | Display text |
| `5` | `EditText` | Text input field |
| `6` | `ImageView` | Display image |
| `7` | `ListView` | Scrollable list |
| `8` | `Spinner` | Dropdown selector |
| `9` | `CheckBox` | Boolean checkbox |
| `10` | `RadioButton` | Single-choice button |
| `11` | `RadioGroup` | Container for RadioButtons |
| `12` | `ProgressBar` | Loading indicator |
| `13` | `HorizontalScrollView` | Horizontal scrollable |
| `14` | `Switch` | Toggle switch |
| `15` | `SeekBar` | Slider |
| `16` | `CalendarView` | Calendar picker |
| `17` | `FloatingActionButton` | Material FAB |
| `18` | `DatePicker` | Date selection |
| `19` | `TimePicker` | Time selection |
| `20` | `MapView` | Google Maps (needs lib) |
| `21` | `VideoView` | Video player |
| `22` | `WebView` | Web browser |
| `23` | `RecyclerView` | Efficient list (needs lib) |
| `24` | `ViewPager` | Swipeable pages |
| `26` | `TabLayout` | Tab headers |
| `29` | `SwipeRefreshLayout` | Pull-to-refresh |

### View JSON Key Fields Explained

```json
{
  "id": "btn_login",           // Unique view ID (used in events/logic)
  "convert": "Button",         // View type string
  "type": 3,                   // View type integer
  "parent": "ll_main",         // Parent view ID ("root" = root layout)
  "parentType": 0,             // Parent type (0=LinearLayout, 2=ScrollView)
  "index": 2,                  // Position within parent
  "clickable": 1,              // 1=clickable, 0=not
  "enabled": 1,                // 1=enabled, 0=disabled
  "alpha": 1.0,                // Transparency (0.0-1.0)

  "layout": {
    "width": -1,               // -1=match_parent, -2=wrap_content, Ndp=fixed
    "height": -2,
    "orientation": 1,          // 0=horizontal, 1=vertical (LinearLayout only)
    "backgroundColor": -16777216, // ARGB signed 32-bit integer
    "gravity": 17,             // Android Gravity flags (17=center)
    "layoutGravity": 0,        // Layout gravity within parent
    "marginTop": 16,           // dp values
    "marginBottom": 0,
    "marginLeft": 0,
    "marginRight": 0,
    "paddingTop": 12,
    "paddingBottom": 12,
    "paddingLeft": 24,
    "paddingRight": 24,
    "weight": 1,               // LinearLayout weight
    "weightSum": 0             // LinearLayout weightSum
  },

  "text": {
    "text": "LOGIN",           // Display text
    "hint": "",                // Hint text for EditText
    "textColor": -16777216,    // ARGB signed 32-bit integer
    "hintColor": -10453621,    // Hint text color
    "textSize": 16,            // sp value
    "textType": 1,             // 0=normal, 1=bold, 2=italic, 3=bold+italic
    "textFont": "default_font",// Font name or "default_font"
    "inputType": 129,          // Android InputType flags (1=text, 3=number, 129=password)
    "singleLine": 0,           // 0=multiline, 1=single line
    "line": 0,                 // Max lines (0=unlimited)
    "imeOption": 0             // IME action (0=none, 2=go, 6=done)
  },

  "image": {
    "resName": "icon",         // Image resource name (without extension)
    "scaleType": "CENTER_CROP",// CENTER, CENTER_CROP, FIT_XY, etc.
    "rotate": 0               // Rotation degrees
  }
}
```

### Color Format (ARGB Signed 32-bit)

```java
// Formula: (alpha << 24) | (red << 16) | (green << 8) | blue
// All values cast to signed 32-bit integer

White  : -1           // 0xFFFFFFFF
Black  : -16777216    // 0xFF000000
Gold   : -32   // (255<<24)|(255<<16)|(215<<8)|0 → approximate
Transparent: 0

// Java helper:
int color = (((255 << 24) | (r << 16) | (g << 8) | b) | 0);

// Common colors:
// #0D0D1A → c(13,13,26)   = -16316134
// #FFD700 → c(255,215,0)  = -32
// #141423 → c(20,20,35)   = -16119773
// #F44336 → c(244,67,54)  = -769226
```

---

## 6. Block System — Logic Coding

### Block JSON Format

Each block is one JSON line inside a logic section:

```json
{
  "color": -10701022,
  "id": "1",
  "nextBlock": 2,
  "opCode": "addSourceDirectly",
  "parameters": ["String uid = prefs.getString(\"uid\",\"\");"],
  "spec": "add source directly %s.inputOnly",
  "subStack1": -1,
  "subStack2": -1,
  "type": " ",
  "typeName": ""
}
```

### Block Field Reference

| Field | Type | Description |
|---|---|---|
| `id` | String | Unique block ID within an event (starts at "1") |
| `color` | Integer | Block color (ARGB signed 32-bit) |
| `opCode` | String | Block operation code (block name) |
| `spec` | String | Block display spec with param placeholders |
| `type` | String | Block return type (see Block Types below) |
| `typeName` | String | Variable type name for typed returns |
| `parameters` | Array | Block parameter values (strings) |
| `nextBlock` | Integer | Next block ID (-1 = end) |
| `subStack1` | Integer | First sub-stack block ID (-1 = none) |
| `subStack2` | Integer | Second sub-stack block ID (-1 = none) |

### Block Types (`type` field)

| `type` | Return Type | Description |
|---|---|---|
| `" "` (space) | void | Statement block (no return) |
| `"c"` | Control | Container block with one sub-stack |
| `"e"` | Control | Container block with two sub-stacks |
| `"d"` | void | Statement inside a container |
| `"b"` | Boolean | Returns true/false |
| `"s"` | String | Returns a String |
| `"l"` | List | Returns an ArrayList |
| `"a"` | void | Event listener block |
| `"f"` | double | Returns a number |
| `"h"` | Header | Palette section header (visual only, no code) |

### Block Spec Placeholders

| Placeholder | Meaning |
|---|---|
| `%s.inputOnly` | String text input |
| `%s.{varName}` | String variable reference |
| `%d.{varName}` | Integer variable reference |
| `%b.{varName}` | Boolean variable reference |
| `%l.{varName}` | List variable reference |
| `%m.activity` | Activity reference |
| `%m.view` | View reference |
| `%m.textview` | TextView reference |
| `%m.edittext` | EditText reference |
| `%m.imageview` | ImageView reference |
| `%m.listview` | ListView reference |
| `%m.spinner` | Spinner reference |
| `%m.progressbar` | ProgressBar reference |
| `%m.progressdialog` | ProgressDialog reference |
| `%m.alertdialog` | AlertDialog reference |
| `%m.map` | Map (HashMap) reference |
| `%m.webview` | WebView reference |
| `%m.calendar` | Calendar reference |
| `%m.firebase` | Firebase reference |
| `%m.intent` | Intent reference |

### Built-in Block Colors

```
#4A6CD4 → View/UI blocks
#E1A92A → Variable blocks  
#EE7D16 → Math blocks
#8A55D7 → List/Map blocks
#5CB6D8 → Component (Firebase, Intent) blocks
#29A7E4 → Dialog/Alert blocks
#E04D41 → Control (if/for/while) blocks
#FF6B6B → IO (file, sharedprefs) blocks
#A1887F → Misc utility blocks
#FF4336 → addSourceDirectly (custom Java)
```

### Logic Data Format (inside `data/logic`)

The `data/logic` file contains sections separated by newlines:

```
@SplashActivity.java_var
2:strVar1
2:strVar2
1:intVar1
@SplashActivity.java_list
1:myIntList
2:myStrList
@SplashActivity.java_func
@SplashActivity.java_components
{"componentId":"intent1","param1":"","param2":"","param3":"","type":1}
{"componentId":"db1","param1":"","param2":"","param3":"DB_URL","type":10}
@SplashActivity.java_events
{"eventName":"onResume","eventType":3,"targetId":"onResume","targetType":0}
{"eventName":"onClick","eventType":1,"targetId":"btn_login","targetType":0}
@SplashActivity.java_onResume_initializeLogic
{"color":-10701022,"id":"1","nextBlock":2,"opCode":"addSourceDirectly","parameters":["your code here"],"spec":"add source directly %s.inputOnly","subStack1":-1,"subStack2":-1,"type":" ","typeName":""}
...
@SplashActivity.java_btn_login_onClick
...
```

### Variable Type Prefixes

```
1: → int (Integer)
2: → String
3: → boolean
4: → Map (HashMap<String,Object>)
5: → List (ArrayList)
```

### Component Types in Logic

| `type` | Component | Parameters |
|---|---|---|
| `1` | Intent | param1="", param2="", param3="" |
| `2` | SharedPreferences | param1=pref_name |
| `3` | Calendar | param1="" |
| `4` | Vibrate | param1="" |
| `5` | Timer | param1="" |
| `6` | Firebase Auth | param1="" |
| `7` | AdMob Interstitial | param1=unit_id |
| `8` | MediaPlayer | param1="" |
| `9` | SoundPool | param1="" |
| `10` | Firebase Database | param1="", param2="", param3=DB_URL |
| `11` | Firebase Storage | param1="" |
| `12` | MediaController | param1="" |

---

## 7. Event System

### Standard Activity Events (from `EventsHandler.java`)

```java
// All available events (in order):
"Import"                  // Code placed at top of Activity file
"initializeLogic"         // Runs in onCreate()
"onActivityResult"        // When startActivityForResult returns
"onBackPressed"           // When back button pressed
"onPostCreate"            // After onCreate
"onStart"                 // Activity starts
"onResume"                // Activity resumes (use this as onCreate)
"onPause"                 // Activity pauses
"onStop"                  // Activity stops
"onDestroy"               // Activity destroyed
"onSaveInstanceState"     // Save state
"onRestoreInstanceState"  // Restore state
"onCreateOptionsMenu"     // Menu created
"onOptionsItemSelected"   // Menu item selected
"onCreateContextMenu"     // Context menu
"onContextItemSelected"   // Context menu item
"onTabLayoutNewTabAdded"  // TabLayout tab added
```

### Component Events

| Component | Events |
|---|---|
| View (Clickable) | `onClick`, `onLongClick` |
| SwipeRefreshLayout | `onSwipeRefreshLayout` |
| AsyncTask | `onPreExecute`, `doInBackground`, `onProgressUpdate`, `onPostExecute` |

### Event JSON Format (in `data/logic` `@{Activity}.java_events` section)

```json
{"eventName":"onClick","eventType":1,"targetId":"btn_login","targetType":0}
{"eventName":"onResume","eventType":3,"targetId":"onResume","targetType":0}
{"eventName":"onActivityResult","eventType":3,"targetId":"onActivityResult","targetType":0}
```

| `eventType` | Meaning |
|---|---|
| `1` | View event (onClick, onLongClick) |
| `2` | Component event (Firebase, Timer) |
| `3` | Activity lifecycle event |

---

## 8. Component System

### Built-in Component Types (from `ComponentsHandler.java`)

| ID | Name | Usage |
|---|---|---|
| `1` | Intent | Navigate between activities |
| `2` | SharedPreferences | Local key-value storage |
| `3` | Calendar | Date/time operations |
| `4` | Vibrate | Device vibration |
| `5` | Timer | Delayed/periodic execution |
| `6` | Firebase Auth | User authentication |
| `7` | AdMob Interstitial | Full-screen ads |
| `8` | MediaPlayer | Audio playback |
| `9` | SoundPool | Short audio clips |
| `10` | Firebase Database | Realtime Database |
| `11` | Firebase Storage | File cloud storage |
| `12` | MediaController | Media controls UI |
| `36` | AsyncTask | Background thread operations |

### Component JSON Format

```json
{
  "componentId": "myFirebaseDb",
  "param1": "",
  "param2": "",
  "param3": "https://my-project-default-rtdb.firebaseio.com",
  "type": 10
}
```

---

## 9. Library System

### Built-in Library JSON Format (inside `data/library`)

```
@firebaseDB
{"adUnits":[],"data":"https://project-rtdb.firebaseio.com","libType":0,"reserved1":"","reserved2":"","reserved3":"https://project-rtdb.firebaseio.com","testDevices":[],"useYn":"Y"}
@compat
{"adUnits":[],"data":"","libType":1,"reserved1":"","reserved2":"","reserved3":"","testDevices":[],"useYn":"Y"}
@admob
{"adUnits":[{"adSize":"BANNER","adUnitId":"ca-app-pub-xxx/xxx"}],"data":"","libType":2,"reserved1":"","reserved2":"","reserved3":"","testDevices":[],"useYn":"N"}
@googleMap
{"adUnits":[],"data":"API_KEY","libType":3,"reserved1":"","reserved2":"","reserved3":"","testDevices":[],"useYn":"N"}
```

| `libType` | Library | `useYn` | Required Field |
|---|---|---|---|
| `0` | Firebase Database | Y/N | `data` = DB URL |
| `1` | AppCompat (compat) | Y (always) | none |
| `2` | AdMob | Y/N | `adUnits` array |
| `3` | Google Maps | Y/N | `data` = API key |

### Local Library JSON Format (`data/local_library`)

```json
[
  {
    "name": "Firebase Database",
    "groupId": "com.google.firebase",
    "artifactId": "firebase-database",
    "version": "20.3.0",
    "jdkVersion": "1.8",
    "classpath": ""
  },
  {
    "name": "Glide",
    "groupId": "com.github.bumptech.glide",
    "artifactId": "glide",
    "version": "4.16.0",
    "jdkVersion": "1.8",
    "classpath": ""
  }
]
```

### Built-in Libraries (from `BuiltInLibraries.java`)

These are always available without adding to `local_library`:

| Category | Libraries | Version |
|---|---|---|
| **AndroidX Core** | `appcompat`, `core`, `core-ktx`, `constraintlayout` | 1.7.1 / 1.17.0 / 2.2.1 |
| **AndroidX UI** | `cardview`, `recyclerview`, `viewpager`, `coordinatorlayout` | 1.0.0 / 1.4.0 |
| **Material Design** | `material` | 1.13.0 |
| **Firebase** | `firebase-database`, `firebase-auth`, `firebase-storage`, `firebase-messaging` | 19.x |
| **Google** | `gson`, `okhttp-android`, `glide` | 2.13.1 / 5.1.0 / 5.0.4 |
| **Kotlin** | `kotlin-stdlib`, `kotlinx-coroutines-android` | 2.2.0 / 1.8.1 |

### Library Dependency Rule

```
⚠️ If a library is already BUILT-IN (BuiltInLibraries.java), 
   do NOT add it to local_library — causes duplicate class conflict.

Safe to add to local_library:
  ✅ OkHttp3 (com.squareup.okhttp3:okhttp:4.11.0)     ← older API
  ✅ CircleImageView (de.hdodenhof:circleimageview)
  ✅ Picasso, Retrofit, Room, etc.
  ✅ Any library NOT listed in BuiltInLibraries.java

Do NOT add to local_library (already built-in):
  ❌ firebase-database (built-in v19.3.1)
  ❌ gson (built-in v2.13.1)
  ❌ material (built-in v1.13.0)
  ❌ appcompat (built-in)
  ❌ recyclerview (built-in)
```

---

## 10. Custom Blocks System

### Custom Block JSON Format (`extra_block` or `custom_blocks`)

```json
[
  {
    "name": "ShowToast",
    "spec": "Show toast %s.message in %m.activity",
    "spec2": "",
    "code": "android.widget.Toast.makeText(%2$s, %1$s, android.widget.Toast.LENGTH_SHORT).show();",
    "imports": "import android.widget.Toast;",
    "color": "#F44336",
    "palette": "9",
    "type": " ",
    "typeName": ""
  }
]
```

### Custom Block Field Reference

| Field | Required | Rules | Description |
|---|---|---|---|
| `name` | ✅ | Must be `String` type. Cannot be empty | Block identifier (used internally) |
| `spec` | ✅ | String | Display text with param placeholders |
| `spec2` | ❌ | String | Secondary spec (optional) |
| `code` | ✅ | String | Java code template with `%1$s`, `%2$s`... placeholders |
| `imports` | ❌ | String | Import statements (newline separated) |
| `color` | ✅ | Hex string `#RRGGBB` | Block color |
| `palette` | ✅ | String number | Index in palette array |
| `type` | ✅ | One of: `" "`,`"c"`,`"e"`,`"d"`,`"b"`,`"s"`,`"l"`,`"a"`,`"f"`,`"h"` | Block return type |
| `typeName` | ❌ | String | Variable type for returns |

### ⚠️ Custom Block Validation Rules (CRITICAL)

```
From BlockLoader.java (v6.3.0+):

Rule 1: `name` field MUST be of type String
        → If null or non-String: "Invalid name entry in Custom Block #N"

Rule 2: `name` field MUST NOT be empty string
        → Empty name causes load failure

Rule 3: For header blocks (type="h"), name MUST match:
        [A-Za-z][A-Za-z0-9_]*  (no spaces, no special chars)
        → Spaces/dots/special chars = "has an invalid name" error

Rule 4: `color` field MUST be valid hex color (#RRGGBB or #AARRGGBB)
        → Invalid color: "Invalid hex color" error

Rule 5: `palette` field MUST be valid integer string
        → Invalid palette: "Invalid palette entry in block #N"
```

### Custom Palette JSON Format

```json
[
  { "name": "MyCustomCategory", "color": "#F44336" },
  { "name": "Firebase_Utils",   "color": "#FF9800" },
  { "name": "UI_Helpers",       "color": "#4CAF50" }
]
```

**Palette Name Rules:**
- Must be a `String` type (not null)
- No spaces (use underscores: `My_Category`)
- Only letters, digits, underscores: `[A-Za-z0-9_]+`
- Must be unique (no duplicates)

Source: `BlocksManagerDetailsActivity.java` line 205

---

## 11. File Index — Source Code Map

### Critical Files (Must Read for AI Training)

| File | Package | What AI Learns |
|---|---|---|
| `BackupFactory.java` | `mod.hey.studios.project.backup` | SWB ZIP format, AES encryption, file structure, restore logic |
| `BlockLoader.java` | `mod.hey.studios.editor.manage.block.v2` | Custom block validation rules, error messages, loading logic |
| `BlocksHandler.java` | `mod.hilal.saif.blocks` | ALL 200+ built-in blocks with their name, spec, code, color, type |
| `EventsHandler.java` | `mod.hilal.saif.events` | All activity events, component events, custom events system |
| `ComponentsHandler.java` | `mod.hilal.saif.components` | All component types, IDs, validation |
| `ViewPropertyItems.java` | `com.besome.sketch.editor.property` | All view properties per view type |
| `BuiltInLibraries.java` | `mod.jbk.build` | All built-in library names + versions + dependencies |
| `BlocksManagerCreatorActivity.java` | `mod.agus.jcoderz.editor.manage.block` | Block creation/editing UI, name validation |
| `BlocksManagerDetailsActivity.java` | `mod.agus.jcoderz.editor.manage.block` | Palette validation, block-palette relationship |
| `CustomBlocksManager.java` | `mod.hey.studios.project.custom_blocks` | Per-project custom blocks file management |
| `CommandBlock.java` | (mod package) | Special command block types |
| `AndroidManifestInjection.java` | `pro.sketchware` | AndroidManifest injection system |

### Build System Files

| File | What AI Learns |
|---|---|
| `AppBundleCompiler.java` | APK/AAB build process |
| `ResourceCompiler.java` | Resource compilation (aapt) |
| `DexCompiler.java` | DEX compilation (D8/R8) |
| `DependencyResolver.kt` | Gradle dependency resolution |
| `BuildSettings.java` | Build configuration options |
| `ExportProjectActivity.java` | Full project export flow |

### Editor UI Files

| File | What AI Learns |
|---|---|
| `AddViewActivity.java` | How views are added to layouts |
| `AddViewActivity.java` constants | VIEW_TYPE_ACTIVITY=0, FRAGMENT=1, DIALOG=2, BOTTOMDIALOG=3 |
| `SrcCodeEditor.java` | Source code editor features |
| `CodeEditorLayout.java` | Code editor layout system |
| `ResourcesEditorActivity.java` | Image/font/sound resource management |

### app/src/main/assets Contents

```
assets/
├── anim/
│     ├── guide_create.json      ← Lottie animation for "Create" tutorial
│     ├── guide_imagine.json     ← Lottie animation for "Imagine" tutorial
│     ├── guide_share.json       ← Lottie animation for "Share" tutorial
│     ├── loading_3balls.json    ← Loading animation
│     ├── loading_cloud.json     ← Loading animation
│     ├── loading_simple_gray.json ← Simple loading
│     ├── login_lock.json        ← Lock animation for login
│     ├── preloader.json         ← Preloader animation
│     └── sketchware_logo.json   ← Sketchware logo animation
│
├── debug/
│     ├── DebugActivity.java     ← Debug overlay for compiled apps
│     ├── SketchApplication.java ← Application class for compiled apps
│     └── SketchLogger.java      ← Logger for compiled apps
│
└── fonts/
      ├── droid_sans_mono.ttf    ← Code editor font
      └── jetbrainsmono-regular.ttf ← Modern code editor font
```

---

## 12. Data Format Reference

### `project` file JSON Structure

```json
{
  "custom_icon": false,
  "sc_id": "700",
  "sc_ver_code": "1",
  "sc_ver_name": "1.0.0",
  "my_ws_name": "MyApp",
  "my_app_name": "My App",
  "my_sc_pkg_name": "com.example.myapp",
  "my_sc_reg_dt": "20260101000000",
  "sketchware_ver": 150,
  "color_primary": -16316134,
  "color_primary_dark": -15659547,
  "color_accent": -32,
  "color_control_highlight": -32,
  "color_control_normal": -32
}
```

### `data/file` JSON Structure

```
@activity
{"fileName":"splash","fileType":0,"keyboardSetting":0,"options":8,"orientation":1,"theme":-1}
{"fileName":"auth","fileType":0,"keyboardSetting":1,"options":8,"orientation":1,"theme":-1}
{"fileName":"main","fileType":0,"keyboardSetting":0,"options":8,"orientation":1,"theme":-1}
@customview
{"fileName":"item_skin","fileType":1,"keyboardSetting":0,"options":0,"orientation":2,"theme":-1}
```

| Field | Values | Description |
|---|---|---|
| `fileName` | String | Screen name (no Activity suffix, lowercase) |
| `fileType` | `0`=Activity, `1`=CustomView | File type |
| `keyboardSetting` | `0`=none, `1`=resize, `2`=pan | Keyboard behavior |
| `orientation` | `0`=landscape, `1`=portrait, `2`=both | Screen orientation |
| `options` | Integer bitmask | Various options |
| `theme` | `-1`=default | Activity theme |

### `data/permission` JSON Structure

```json
[
  "android.permission.INTERNET",
  "android.permission.READ_EXTERNAL_STORAGE",
  "android.permission.WRITE_EXTERNAL_STORAGE",
  "android.permission.ACCESS_NETWORK_STATE",
  "android.permission.CAMERA",
  "android.permission.ACCESS_FINE_LOCATION"
]
```

### `data/build_config` JSON Structure

```json
{
  "dexer": "D8",
  "classpath": "",
  "no_http_legacy": "false",
  "android_jar": "",
  "no_warn": "true",
  "java_ver": "1.8"
}
```

### `data/resource` JSON Structure

```
@images
{"resFullName":"icon.png","resName":"icon","resType":1}
{"resFullName":"banner.jpg","resName":"banner","resType":1}
@sounds
{"resFullName":"click.mp3","resName":"click","resType":2}
@fonts
{"resFullName":"opensans.ttf","resName":"opensans","resType":3}
```

---

## 13. Error Messages Reference

### Custom Block Errors (from `BlockLoader.java`)

| Error Message | Cause | Fix |
|---|---|---|
| `Invalid name entry in Custom Block #N` | `name` field is null or not a String | Ensure `name` is always a non-null String |
| `Custom Block #N in current palette has an invalid name` | `name` contains invalid chars (spaces, dots, special chars) for header blocks | Replace spaces with `_`, remove special chars |
| `Invalid palette entry in block #N` | `palette` field is not a valid integer string | Ensure `palette` is `"0"`, `"1"`, etc. |

### Palette Errors (from `BlocksManagerDetailsActivity.java`)

| Error Message | Cause | Fix |
|---|---|---|
| `Invalid name of palette #N` | palette `name` is null or not a String | Set `name` to valid String |
| `Invalid color of palette #N` | palette `color` is not valid hex | Use `#RRGGBB` format |
| `Failed to parse JSON` | palette file is corrupt | Validate JSON syntax |

### Block Creator Errors (from `BlocksManagerCreatorActivity.java`)

| Error Message | Cause | Fix |
|---|---|---|
| `Block name already in use` | Two blocks share same `name` | Use unique names |
| `Invalid hex color` | Color not in `#RRGGBB` format | Use valid hex color |
| `Invalid block params` | Parameters malformed | Check `%1$s`, `%2$s` format |
| `Invalid name block data` | `name` not a String in stored data | Fix JSON data type |

---

## Contributing / Usage

This repository is maintained for **AI skill training** for Sketchware Pro V7 project generation.

### How to Use This Repo for AI Training

1. **Architecture understanding**: Read section 2 + File Index (section 11)
2. **Generate a .swb file**: Read sections 3, 4, 12 for exact file formats
3. **Debug block errors**: Read sections 10 + 13
4. **Add custom libraries**: Read section 9
5. **Generate UI layouts**: Read section 5
6. **Add logic/events**: Read sections 6 + 7

### Source Code Context

All Java/Kotlin files in this repository are extracted from the Sketchware Pro V7 source code. Files are from these open-source packages:
- `mod.*` packages: Community contributions
- `pro.sketchware.*` packages: Core modern refactors
- `com.besome.sketch.*` packages: Original Sketchware UI classes
- `app/src/main/assets/`: Runtime assets embedded in the APK

The core obfuscated package (`a.a.a.*`) is **not included** as it contains proprietary business logic.

---

*Last updated: 2026-08-04 | Sketchware Pro V7.0.0 Stable*
