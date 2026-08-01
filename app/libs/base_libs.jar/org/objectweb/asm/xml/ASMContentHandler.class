.class public Lorg/objectweb/asm/xml/ASMContentHandler;
.super Lorg/xml/sax/helpers/DefaultHandler;

# interfaces
.implements Lorg/objectweb/asm/Opcodes;


# static fields
.field private static final BASE:Ljava/lang/String; = "class"

.field static final OPCODES:Ljava/util/HashMap;

.field static final TYPES:Ljava/util/HashMap;


# instance fields
.field private final RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

.field protected cv:Lorg/objectweb/asm/ClassVisitor;

.field protected labels:Ljava/util/Map;

.field match:Ljava/lang/String;

.field private final stack:Ljava/util/ArrayList;


# direct methods
.method static constructor <clinit>()V
    .registers 8

    const/4 v7, 0x4

    const/4 v6, 0x3

    const/4 v5, 0x2

    const/4 v4, 0x6

    const/4 v0, 0x0

    invoke-static {}, Lorg/objectweb/asm/xml/ASMContentHandler;->_clinit_()V

    new-instance v1, Ljava/util/HashMap;

    invoke-direct {v1}, Ljava/util/HashMap;-><init>()V

    sput-object v1, Lorg/objectweb/asm/xml/ASMContentHandler;->OPCODES:Ljava/util/HashMap;

    const-string v1, "NOP"

    invoke-static {v1, v0, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ACONST_NULL"

    const/4 v2, 0x1

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_M1"

    invoke-static {v1, v5, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_0"

    invoke-static {v1, v6, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_1"

    invoke-static {v1, v7, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_2"

    const/4 v2, 0x5

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_3"

    invoke-static {v1, v4, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_4"

    const/4 v2, 0x7

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ICONST_5"

    const/16 v2, 0x8

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LCONST_0"

    const/16 v2, 0x9

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LCONST_1"

    const/16 v2, 0xa

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FCONST_0"

    const/16 v2, 0xb

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FCONST_1"

    const/16 v2, 0xc

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FCONST_2"

    const/16 v2, 0xd

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DCONST_0"

    const/16 v2, 0xe

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DCONST_1"

    const/16 v2, 0xf

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "BIPUSH"

    const/16 v2, 0x10

    const/4 v3, 0x1

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "SIPUSH"

    const/16 v2, 0x11

    const/4 v3, 0x1

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LDC"

    const/16 v2, 0x12

    const/4 v3, 0x7

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ILOAD"

    const/16 v2, 0x15

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LLOAD"

    const/16 v2, 0x16

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FLOAD"

    const/16 v2, 0x17

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DLOAD"

    const/16 v2, 0x18

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ALOAD"

    const/16 v2, 0x19

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IALOAD"

    const/16 v2, 0x2e

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LALOAD"

    const/16 v2, 0x2f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FALOAD"

    const/16 v2, 0x30

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DALOAD"

    const/16 v2, 0x31

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "AALOAD"

    const/16 v2, 0x32

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "BALOAD"

    const/16 v2, 0x33

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "CALOAD"

    const/16 v2, 0x34

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "SALOAD"

    const/16 v2, 0x35

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ISTORE"

    const/16 v2, 0x36

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LSTORE"

    const/16 v2, 0x37

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FSTORE"

    const/16 v2, 0x38

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DSTORE"

    const/16 v2, 0x39

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ASTORE"

    const/16 v2, 0x3a

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IASTORE"

    const/16 v2, 0x4f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LASTORE"

    const/16 v2, 0x50

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FASTORE"

    const/16 v2, 0x51

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DASTORE"

    const/16 v2, 0x52

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "AASTORE"

    const/16 v2, 0x53

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "BASTORE"

    const/16 v2, 0x54

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "CASTORE"

    const/16 v2, 0x55

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "SASTORE"

    const/16 v2, 0x56

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "POP"

    const/16 v2, 0x57

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "POP2"

    const/16 v2, 0x58

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP"

    const/16 v2, 0x59

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP_X1"

    const/16 v2, 0x5a

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP_X2"

    const/16 v2, 0x5b

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP2"

    const/16 v2, 0x5c

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP2_X1"

    const/16 v2, 0x5d

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DUP2_X2"

    const/16 v2, 0x5e

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "SWAP"

    const/16 v2, 0x5f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IADD"

    const/16 v2, 0x60

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LADD"

    const/16 v2, 0x61

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FADD"

    const/16 v2, 0x62

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DADD"

    const/16 v2, 0x63

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ISUB"

    const/16 v2, 0x64

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LSUB"

    const/16 v2, 0x65

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FSUB"

    const/16 v2, 0x66

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DSUB"

    const/16 v2, 0x67

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IMUL"

    const/16 v2, 0x68

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LMUL"

    const/16 v2, 0x69

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FMUL"

    const/16 v2, 0x6a

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DMUL"

    const/16 v2, 0x6b

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IDIV"

    const/16 v2, 0x6c

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LDIV"

    const/16 v2, 0x6d

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FDIV"

    const/16 v2, 0x6e

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DDIV"

    const/16 v2, 0x6f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IREM"

    const/16 v2, 0x70

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LREM"

    const/16 v2, 0x71

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FREM"

    const/16 v2, 0x72

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DREM"

    const/16 v2, 0x73

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INEG"

    const/16 v2, 0x74

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LNEG"

    const/16 v2, 0x75

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FNEG"

    const/16 v2, 0x76

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DNEG"

    const/16 v2, 0x77

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ISHL"

    const/16 v2, 0x78

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LSHL"

    const/16 v2, 0x79

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ISHR"

    const/16 v2, 0x7a

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LSHR"

    const/16 v2, 0x7b

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IUSHR"

    const/16 v2, 0x7c

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LUSHR"

    const/16 v2, 0x7d

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IAND"

    const/16 v2, 0x7e

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LAND"

    const/16 v2, 0x7f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IOR"

    const/16 v2, 0x80

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LOR"

    const/16 v2, 0x81

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IXOR"

    const/16 v2, 0x82

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LXOR"

    const/16 v2, 0x83

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IINC"

    const/16 v2, 0x84

    const/16 v3, 0x8

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2L"

    const/16 v2, 0x85

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2F"

    const/16 v2, 0x86

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2D"

    const/16 v2, 0x87

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "L2I"

    const/16 v2, 0x88

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "L2F"

    const/16 v2, 0x89

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "L2D"

    const/16 v2, 0x8a

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "F2I"

    const/16 v2, 0x8b

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "F2L"

    const/16 v2, 0x8c

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "F2D"

    const/16 v2, 0x8d

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "D2I"

    const/16 v2, 0x8e

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "D2L"

    const/16 v2, 0x8f

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "D2F"

    const/16 v2, 0x90

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2B"

    const/16 v2, 0x91

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2C"

    const/16 v2, 0x92

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "I2S"

    const/16 v2, 0x93

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LCMP"

    const/16 v2, 0x94

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FCMPL"

    const/16 v2, 0x95

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FCMPG"

    const/16 v2, 0x96

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DCMPL"

    const/16 v2, 0x97

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DCMPG"

    const/16 v2, 0x98

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFEQ"

    const/16 v2, 0x99

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFNE"

    const/16 v2, 0x9a

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFLT"

    const/16 v2, 0x9b

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFGE"

    const/16 v2, 0x9c

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFGT"

    const/16 v2, 0x9d

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFLE"

    const/16 v2, 0x9e

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPEQ"

    const/16 v2, 0x9f

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPNE"

    const/16 v2, 0xa0

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPLT"

    const/16 v2, 0xa1

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPGE"

    const/16 v2, 0xa2

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPGT"

    const/16 v2, 0xa3

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ICMPLE"

    const/16 v2, 0xa4

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ACMPEQ"

    const/16 v2, 0xa5

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IF_ACMPNE"

    const/16 v2, 0xa6

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "GOTO"

    const/16 v2, 0xa7

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "JSR"

    const/16 v2, 0xa8

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "RET"

    const/16 v2, 0xa9

    invoke-static {v1, v2, v5}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IRETURN"

    const/16 v2, 0xac

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "LRETURN"

    const/16 v2, 0xad

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "FRETURN"

    const/16 v2, 0xae

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "DRETURN"

    const/16 v2, 0xaf

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ARETURN"

    const/16 v2, 0xb0

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "RETURN"

    const/16 v2, 0xb1

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "GETSTATIC"

    const/16 v2, 0xb2

    invoke-static {v1, v2, v7}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "PUTSTATIC"

    const/16 v2, 0xb3

    invoke-static {v1, v2, v7}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "GETFIELD"

    const/16 v2, 0xb4

    invoke-static {v1, v2, v7}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "PUTFIELD"

    const/16 v2, 0xb5

    invoke-static {v1, v2, v7}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INVOKEVIRTUAL"

    const/16 v2, 0xb6

    const/4 v3, 0x5

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INVOKESPECIAL"

    const/16 v2, 0xb7

    const/4 v3, 0x5

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INVOKESTATIC"

    const/16 v2, 0xb8

    const/4 v3, 0x5

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INVOKEINTERFACE"

    const/16 v2, 0xb9

    const/4 v3, 0x5

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "NEW"

    const/16 v2, 0xbb

    invoke-static {v1, v2, v6}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "NEWARRAY"

    const/16 v2, 0xbc

    const/4 v3, 0x1

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ANEWARRAY"

    const/16 v2, 0xbd

    invoke-static {v1, v2, v6}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ARRAYLENGTH"

    const/16 v2, 0xbe

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "ATHROW"

    const/16 v2, 0xbf

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "CHECKCAST"

    const/16 v2, 0xc0

    invoke-static {v1, v2, v6}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "INSTANCEOF"

    const/16 v2, 0xc1

    invoke-static {v1, v2, v6}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "MONITORENTER"

    const/16 v2, 0xc2

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "MONITOREXIT"

    const/16 v2, 0xc3

    invoke-static {v1, v2, v0}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "MULTIANEWARRAY"

    const/16 v2, 0xc5

    const/16 v3, 0x9

    invoke-static {v1, v2, v3}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFNULL"

    const/16 v2, 0xc6

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    const-string v1, "IFNONNULL"

    const/16 v2, 0xc7

    invoke-static {v1, v2, v4}, Lorg/objectweb/asm/xml/ASMContentHandler;->addOpcode(Ljava/lang/String;II)V

    new-instance v1, Ljava/util/HashMap;

    invoke-direct {v1}, Ljava/util/HashMap;-><init>()V

    sput-object v1, Lorg/objectweb/asm/xml/ASMContentHandler;->TYPES:Ljava/util/HashMap;

    sget-object v1, Lorg/objectweb/asm/xml/SAXCodeAdapter;->TYPES:[Ljava/lang/String;

    :goto_44d
    array-length v2, v1

    if-ge v0, v2, :cond_45f

    sget-object v2, Lorg/objectweb/asm/xml/ASMContentHandler;->TYPES:Ljava/util/HashMap;

    aget-object v3, v1, v0

    new-instance v4, Ljava/lang/Integer;

    invoke-direct {v4, v0}, Ljava/lang/Integer;-><init>(I)V

    invoke-virtual {v2, v3, v4}, Ljava/util/HashMap;->put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;

    add-int/lit8 v0, v0, 0x1

    goto :goto_44d

    :cond_45f
    return-void
.end method

.method public constructor <init>(Lorg/objectweb/asm/ClassVisitor;)V
    .registers 5

    invoke-direct {p0}, Lorg/xml/sax/helpers/DefaultHandler;-><init>()V

    new-instance v0, Ljava/util/ArrayList;

    invoke-direct {v0}, Ljava/util/ArrayList;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    const-string v0, ""

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    new-instance v0, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    invoke-direct {v0}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$ClassRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$ClassRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/interfaces/interface"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InterfaceRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InterfaceRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/interfaces"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InterfacesRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InterfacesRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/outerclass"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$OuterClassRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$OuterClassRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/innerclass"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InnerClassRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InnerClassRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/source"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$SourceRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$SourceRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/field"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$FieldRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$FieldRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$MethodRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$MethodRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/exceptions/exception"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$ExceptionRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$ExceptionRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/exceptions"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$ExceptionsRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$ExceptionsRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/parameter"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$MethodParameterRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$MethodParameterRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/annotationDefault"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationDefaultRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationDefaultRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/*"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$OpcodesRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$OpcodesRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/frame"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$FrameRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$FrameRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/frame/local"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$FrameTypeRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$FrameTypeRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/frame/stack"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$FrameTypeRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$FrameTypeRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/TABLESWITCH"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$TableSwitchRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$TableSwitchRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/TABLESWITCH/label"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$TableSwitchLabelRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$TableSwitchLabelRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/LOOKUPSWITCH"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LookupSwitchRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LookupSwitchRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/LOOKUPSWITCH/label"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LookupSwitchLabelRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LookupSwitchLabelRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/INVOKEDYNAMIC"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InvokeDynamicRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InvokeDynamicRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/INVOKEDYNAMIC/bsmArg"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InvokeDynamicBsmArgumentsRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InvokeDynamicBsmArgumentsRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/Label"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LabelRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LabelRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/TryCatch"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$TryCatchRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$TryCatchRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/LineNumber"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LineNumberRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LineNumberRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/LocalVar"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LocalVarRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LocalVarRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "class/method/code/Max"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$MaxRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$MaxRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/annotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/typeAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$TypeAnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$TypeAnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/parameterAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationParameterRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationParameterRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/insnAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$InsnAnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$InsnAnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/tryCatchAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$TryCatchAnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$TryCatchAnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/localVariableAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$LocalVariableAnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$LocalVariableAnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/annotationValue"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/annotationValueAnnotation"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueAnnotationRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueAnnotationRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/annotationValueEnum"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueEnumRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueEnumRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    const-string v1, "*/annotationValueArray"

    new-instance v2, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueArrayRule;

    invoke-direct {v2, p0}, Lorg/objectweb/asm/xml/ASMContentHandler$AnnotationValueArrayRule;-><init>(Lorg/objectweb/asm/xml/ASMContentHandler;)V

    invoke-virtual {v0, v1, v2}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->add(Ljava/lang/String;Ljava/lang/Object;)V

    iput-object p1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->cv:Lorg/objectweb/asm/ClassVisitor;

    return-void
.end method

.method static _clinit_()V
    .registers 0

    return-void
.end method

.method private static addOpcode(Ljava/lang/String;II)V
    .registers 5

    sget-object v0, Lorg/objectweb/asm/xml/ASMContentHandler;->OPCODES:Ljava/util/HashMap;

    new-instance v1, Lorg/objectweb/asm/xml/ASMContentHandler$Opcode;

    invoke-direct {v1, p1, p2}, Lorg/objectweb/asm/xml/ASMContentHandler$Opcode;-><init>(II)V

    invoke-virtual {v0, p0, v1}, Ljava/util/HashMap;->put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;

    return-void
.end method


# virtual methods
.method public final endElement(Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;)V
    .registers 7
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/xml/sax/SAXException;
        }
    .end annotation

    if-eqz p2, :cond_8

    invoke-virtual {p2}, Ljava/lang/String;->length()I

    move-result v0

    if-nez v0, :cond_9

    :cond_8
    move-object p2, p3

    :cond_9
    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    invoke-virtual {v0, v1}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->match(Ljava/lang/String;)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/xml/ASMContentHandler$Rule;

    if-eqz v0, :cond_18

    invoke-virtual {v0, p2}, Lorg/objectweb/asm/xml/ASMContentHandler$Rule;->end(Ljava/lang/String;)V

    :cond_18
    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    const/16 v1, 0x2f

    invoke-virtual {v0, v1}, Ljava/lang/String;->lastIndexOf(I)I

    move-result v0

    if-ltz v0, :cond_2c

    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    const/4 v2, 0x0

    invoke-virtual {v1, v2, v0}, Ljava/lang/String;->substring(II)Ljava/lang/String;

    move-result-object v0

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    :goto_2b
    return-void

    :cond_2c
    const-string v0, ""

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    goto :goto_2b
.end method

.method final peek()Ljava/lang/Object;
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    invoke-virtual {v0}, Ljava/util/ArrayList;->size()I

    move-result v0

    if-nez v0, :cond_a

    const/4 v0, 0x0

    :goto_9
    return-object v0

    :cond_a
    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    add-int/lit8 v0, v0, -0x1

    invoke-virtual {v1, v0}, Ljava/util/ArrayList;->get(I)Ljava/lang/Object;

    move-result-object v0

    goto :goto_9
.end method

.method final pop()Ljava/lang/Object;
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    invoke-virtual {v0}, Ljava/util/ArrayList;->size()I

    move-result v0

    if-nez v0, :cond_a

    const/4 v0, 0x0

    :goto_9
    return-object v0

    :cond_a
    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    add-int/lit8 v0, v0, -0x1

    invoke-virtual {v1, v0}, Ljava/util/ArrayList;->remove(I)Ljava/lang/Object;

    move-result-object v0

    goto :goto_9
.end method

.method final push(Ljava/lang/Object;)V
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->stack:Ljava/util/ArrayList;

    invoke-virtual {v0, p1}, Ljava/util/ArrayList;->add(Ljava/lang/Object;)Z

    return-void
.end method

.method public final startElement(Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;Lorg/xml/sax/Attributes;)V
    .registers 7
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/xml/sax/SAXException;
        }
    .end annotation

    if-eqz p2, :cond_8

    invoke-virtual {p2}, Ljava/lang/String;->length()I

    move-result v0

    if-nez v0, :cond_9

    :cond_8
    move-object p2, p3

    :cond_9
    new-instance v0, Ljava/lang/StringBuffer;

    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    invoke-direct {v0, v1}, Ljava/lang/StringBuffer;-><init>(Ljava/lang/String;)V

    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    invoke-virtual {v1}, Ljava/lang/String;->length()I

    move-result v1

    if-lez v1, :cond_1d

    const/16 v1, 0x2f

    invoke-virtual {v0, v1}, Ljava/lang/StringBuffer;->append(C)Ljava/lang/StringBuffer;

    :cond_1d
    invoke-virtual {v0, p2}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    invoke-virtual {v0}, Ljava/lang/StringBuffer;->toString()Ljava/lang/String;

    move-result-object v0

    iput-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    iget-object v0, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->RULES:Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;

    iget-object v1, p0, Lorg/objectweb/asm/xml/ASMContentHandler;->match:Ljava/lang/String;

    invoke-virtual {v0, v1}, Lorg/objectweb/asm/xml/ASMContentHandler$RuleSet;->match(Ljava/lang/String;)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/xml/ASMContentHandler$Rule;

    if-eqz v0, :cond_35

    invoke-virtual {v0, p2, p4}, Lorg/objectweb/asm/xml/ASMContentHandler$Rule;->begin(Ljava/lang/String;Lorg/xml/sax/Attributes;)V

    :cond_35
    return-void
.end method
