.class public abstract Lorg/objectweb/asm/commons/AdviceAdapter;
.super Lorg/objectweb/asm/commons/GeneratorAdapter;

# interfaces
.implements Lorg/objectweb/asm/Opcodes;


# static fields
.field private static final OTHER:Ljava/lang/Object;

.field private static final THIS:Ljava/lang/Object;


# instance fields
.field private branches:Ljava/util/Map;

.field private constructor:Z

.field protected methodAccess:I

.field protected methodDesc:Ljava/lang/String;

.field private stackFrame:Ljava/util/List;

.field private superInitialized:Z


# direct methods
.method static constructor <clinit>()V
    .registers 1

    invoke-static {}, Lorg/objectweb/asm/commons/AdviceAdapter;->_clinit_()V

    new-instance v0, Ljava/lang/Object;

    invoke-direct {v0}, Ljava/lang/Object;-><init>()V

    sput-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->THIS:Ljava/lang/Object;

    new-instance v0, Ljava/lang/Object;

    invoke-direct {v0}, Ljava/lang/Object;-><init>()V

    sput-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    return-void
.end method

.method protected constructor <init>(ILorg/objectweb/asm/MethodVisitor;ILjava/lang/String;Ljava/lang/String;)V
    .registers 7

    invoke-direct/range {p0 .. p5}, Lorg/objectweb/asm/commons/GeneratorAdapter;-><init>(ILorg/objectweb/asm/MethodVisitor;ILjava/lang/String;Ljava/lang/String;)V

    iput p3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->methodAccess:I

    iput-object p5, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->methodDesc:Ljava/lang/String;

    const-string v0, "<init>"

    invoke-virtual {v0, p4}, Ljava/lang/String;->equals(Ljava/lang/Object;)Z

    move-result v0

    iput-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    return-void
.end method

.method static _clinit_()V
    .registers 0

    return-void
.end method

.method private addBranch(Lorg/objectweb/asm/Label;)V
    .registers 5

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    invoke-interface {v0, p1}, Ljava/util/Map;->containsKey(Ljava/lang/Object;)Z

    move-result v0

    if-eqz v0, :cond_9

    :goto_8
    return-void

    :cond_9
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    new-instance v1, Ljava/util/ArrayList;

    iget-object v2, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-direct {v1, v2}, Ljava/util/ArrayList;-><init>(Ljava/util/Collection;)V

    invoke-interface {v0, p1, v1}, Ljava/util/Map;->put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;

    goto :goto_8
.end method

.method private addBranches(Lorg/objectweb/asm/Label;[Lorg/objectweb/asm/Label;)V
    .registers 5

    invoke-direct {p0, p1}, Lorg/objectweb/asm/commons/AdviceAdapter;->addBranch(Lorg/objectweb/asm/Label;)V

    const/4 v0, 0x0

    :goto_4
    array-length v1, p2

    if-ge v0, v1, :cond_f

    aget-object v1, p2, v0

    invoke-direct {p0, v1}, Lorg/objectweb/asm/commons/AdviceAdapter;->addBranch(Lorg/objectweb/asm/Label;)V

    add-int/lit8 v0, v0, 0x1

    goto :goto_4

    :cond_f
    return-void
.end method

.method private doVisitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V
    .registers 14

    const/4 v7, 0x2

    const/4 v6, 0x0

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    move v1, p1

    move-object v2, p2

    move-object v3, p3

    move-object v4, p4

    move v5, p5

    invoke-virtual/range {v0 .. v5}, Lorg/objectweb/asm/MethodVisitor;->visitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_44

    invoke-static {p4}, Lorg/objectweb/asm/Type;->getArgumentTypes(Ljava/lang/String;)[Lorg/objectweb/asm/Type;

    move-result-object v1

    move v0, v6

    :goto_15
    array-length v2, v1

    if-ge v0, v2, :cond_29

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    aget-object v2, v1, v0

    invoke-virtual {v2}, Lorg/objectweb/asm/Type;->getSize()I

    move-result v2

    if-ne v2, v7, :cond_26

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    :cond_26
    add-int/lit8 v0, v0, 0x1

    goto :goto_15

    :cond_29
    packed-switch p1, :pswitch_data_5e

    :cond_2c
    :goto_2c
    :pswitch_2c  #0xb8
    invoke-static {p4}, Lorg/objectweb/asm/Type;->getReturnType(Ljava/lang/String;)Lorg/objectweb/asm/Type;

    move-result-object v0

    sget-object v1, Lorg/objectweb/asm/Type;->VOID_TYPE:Lorg/objectweb/asm/Type;

    if-eq v0, v1, :cond_44

    sget-object v1, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v1}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    invoke-virtual {v0}, Lorg/objectweb/asm/Type;->getSize()I

    move-result v0

    if-ne v0, v7, :cond_44

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_44
    return-void

    :pswitch_45  #0xb6, 0xb9
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_2c

    :pswitch_49  #0xb7
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    move-result-object v0

    sget-object v1, Lorg/objectweb/asm/commons/AdviceAdapter;->THIS:Ljava/lang/Object;

    if-ne v0, v1, :cond_2c

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->superInitialized:Z

    if-nez v0, :cond_2c

    invoke-virtual {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodEnter()V

    const/4 v0, 0x1

    iput-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->superInitialized:Z

    iput-boolean v6, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    goto :goto_2c

    :pswitch_data_5e
    .packed-switch 0xb6
        :pswitch_45  #000000b6
        :pswitch_49  #000000b7
        :pswitch_2c  #000000b8
        :pswitch_45  #000000b9
    .end packed-switch
.end method

.method private peekValue()Ljava/lang/Object;
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v1}, Ljava/util/List;->size()I

    move-result v1

    add-int/lit8 v1, v1, -0x1

    invoke-interface {v0, v1}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    return-object v0
.end method

.method private popValue()Ljava/lang/Object;
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v1}, Ljava/util/List;->size()I

    move-result v1

    add-int/lit8 v1, v1, -0x1

    invoke-interface {v0, v1}, Ljava/util/List;->remove(I)Ljava/lang/Object;

    move-result-object v0

    return-object v0
.end method

.method private pushValue(Ljava/lang/Object;)V
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0, p1}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    return-void
.end method


# virtual methods
.method protected onMethodEnter()V
    .registers 1

    return-void
.end method

.method protected onMethodExit(I)V
    .registers 2

    return-void
.end method

.method public visitCode()V
    .registers 2

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0}, Lorg/objectweb/asm/MethodVisitor;->visitCode()V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_18

    new-instance v0, Ljava/util/ArrayList;

    invoke-direct {v0}, Ljava/util/ArrayList;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    new-instance v0, Ljava/util/HashMap;

    invoke-direct {v0}, Ljava/util/HashMap;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    :goto_17
    return-void

    :cond_18
    const/4 v0, 0x1

    iput-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->superInitialized:Z

    invoke-virtual {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodEnter()V

    goto :goto_17
.end method

.method public visitFieldInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;)V
    .registers 8

    const/4 v0, 0x0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v1, p1, p2, p3, p4}, Lorg/objectweb/asm/MethodVisitor;->visitFieldInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;)V

    iget-boolean v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v1, :cond_21

    invoke-virtual {p4, v0}, Ljava/lang/String;->charAt(I)C

    move-result v1

    const/16 v2, 0x4a

    if-eq v1, v2, :cond_16

    const/16 v2, 0x44

    if-ne v1, v2, :cond_17

    :cond_16
    const/4 v0, 0x1

    :cond_17
    packed-switch p1, :pswitch_data_44

    :pswitch_1a  #0xb4
    if-eqz v0, :cond_21

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_21
    :goto_21
    return-void

    :pswitch_22  #0xb2
    sget-object v1, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v1}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    if-eqz v0, :cond_21

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_21

    :pswitch_2f  #0xb3
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    if-eqz v0, :cond_21

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_21

    :pswitch_38  #0xb5
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    if-eqz v0, :cond_21

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_21

    :pswitch_data_44
    .packed-switch 0xb2
        :pswitch_22  #000000b2
        :pswitch_2f  #000000b3
        :pswitch_1a  #000000b4
        :pswitch_38  #000000b5
    .end packed-switch
.end method

.method public visitInsn(I)V
    .registers 7

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_118

    packed-switch p1, :pswitch_data_122

    :goto_7
    :pswitch_7  #0x10, 0x11, 0x12, 0x13, 0x14, 0x15, 0x16, 0x17, 0x18, 0x19, 0x1a, 0x1b, 0x1c, 0x1d, 0x1e, 0x1f, 0x20, 0x21, 0x22, 0x23, 0x24, 0x25, 0x26, 0x27, 0x28, 0x29, 0x2a, 0x2b, 0x2c, 0x2d, 0x2f, 0x31, 0x36, 0x37, 0x38, 0x39, 0x3a, 0x3b, 0x3c, 0x3d, 0x3e, 0x3f, 0x40, 0x41, 0x42, 0x43, 0x44, 0x45, 0x46, 0x47, 0x48, 0x49, 0x4a, 0x4b, 0x4c, 0x4d, 0x4e, 0x74, 0x75, 0x76, 0x77, 0x84, 0x86, 0x8a, 0x8b, 0x8f, 0x91, 0x92, 0x93, 0x99, 0x9a, 0x9b, 0x9c, 0x9d, 0x9e, 0x9f, 0xa0, 0xa1, 0xa2, 0xa3, 0xa4, 0xa5, 0xa6, 0xa7, 0xa8, 0xa9, 0xaa, 0xab, 0xb2, 0xb3, 0xb4, 0xb5, 0xb6, 0xb7, 0xb8, 0xb9, 0xba, 0xbb, 0xbc, 0xbd, 0xbe, 0xc0, 0xc1
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1}, Lorg/objectweb/asm/MethodVisitor;->visitInsn(I)V

    return-void

    :pswitch_d  #0xb1
    invoke-virtual {p0, p1}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodExit(I)V

    goto :goto_7

    :pswitch_11  #0xac, 0xae, 0xb0, 0xbf
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-virtual {p0, p1}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodExit(I)V

    goto :goto_7

    :pswitch_18  #0xad, 0xaf
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-virtual {p0, p1}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodExit(I)V

    goto :goto_7

    :pswitch_22  #0x1, 0x2, 0x3, 0x4, 0x5, 0x6, 0x7, 0x8, 0xb, 0xc, 0xd, 0x85, 0x87, 0x8c, 0x8d
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_7

    :pswitch_28  #0x9, 0xa, 0xe, 0xf
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_7

    :pswitch_33  #0x2e, 0x30, 0x32, 0x33, 0x34, 0x35, 0x57, 0x60, 0x62, 0x64, 0x66, 0x68, 0x6a, 0x6c, 0x6e, 0x70, 0x72, 0x78, 0x79, 0x7a, 0x7b, 0x7c, 0x7d, 0x7e, 0x80, 0x82, 0x88, 0x89, 0x8e, 0x90, 0x95, 0x96, 0xc2, 0xc3
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_7

    :pswitch_37  #0x58, 0x61, 0x63, 0x65, 0x67, 0x69, 0x6b, 0x6d, 0x6f, 0x71, 0x73, 0x7f, 0x81, 0x83
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_7

    :pswitch_3e  #0x4f, 0x51, 0x53, 0x54, 0x55, 0x56, 0x94, 0x97, 0x98
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_7

    :pswitch_48  #0x50, 0x52
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_7

    :pswitch_55  #0x59
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->peekValue()Ljava/lang/Object;

    move-result-object v0

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_7

    :pswitch_5d  #0x5a
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x2

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v0, v0, -0x1

    invoke-interface {v3, v0}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {v1, v2, v0}, Ljava/util/List;->add(ILjava/lang/Object;)V

    goto :goto_7

    :pswitch_73  #0x5b
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x3

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v0, v0, -0x1

    invoke-interface {v3, v0}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {v1, v2, v0}, Ljava/util/List;->add(ILjava/lang/Object;)V

    goto/16 :goto_7

    :pswitch_8a  #0x5c
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x2

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v4, v0, -0x1

    invoke-interface {v3, v4}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v3

    invoke-interface {v1, v2, v3}, Ljava/util/List;->add(ILjava/lang/Object;)V

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x2

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v0, v0, -0x1

    invoke-interface {v3, v0}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {v1, v2, v0}, Ljava/util/List;->add(ILjava/lang/Object;)V

    goto/16 :goto_7

    :pswitch_b0  #0x5d
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x3

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v4, v0, -0x1

    invoke-interface {v3, v4}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v3

    invoke-interface {v1, v2, v3}, Ljava/util/List;->add(ILjava/lang/Object;)V

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x3

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v0, v0, -0x1

    invoke-interface {v3, v0}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {v1, v2, v0}, Ljava/util/List;->add(ILjava/lang/Object;)V

    goto/16 :goto_7

    :pswitch_d6  #0x5e
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x4

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v4, v0, -0x1

    invoke-interface {v3, v4}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v3

    invoke-interface {v1, v2, v3}, Ljava/util/List;->add(ILjava/lang/Object;)V

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x4

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v0, v0, -0x1

    invoke-interface {v3, v0}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {v1, v2, v0}, Ljava/util/List;->add(ILjava/lang/Object;)V

    goto/16 :goto_7

    :pswitch_fc  #0x5f
    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v2, v0, -0x2

    iget-object v3, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    add-int/lit8 v4, v0, -0x1

    invoke-interface {v3, v4}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v3

    invoke-interface {v1, v2, v3}, Ljava/util/List;->add(ILjava/lang/Object;)V

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    invoke-interface {v1, v0}, Ljava/util/List;->remove(I)Ljava/lang/Object;

    goto/16 :goto_7

    :cond_118
    sparse-switch p1, :sswitch_data_2ac

    goto/16 :goto_7

    :sswitch_11d
    invoke-virtual {p0, p1}, Lorg/objectweb/asm/commons/AdviceAdapter;->onMethodExit(I)V

    goto/16 :goto_7

    :pswitch_data_122
    .packed-switch 0x1
        :pswitch_22  #00000001
        :pswitch_22  #00000002
        :pswitch_22  #00000003
        :pswitch_22  #00000004
        :pswitch_22  #00000005
        :pswitch_22  #00000006
        :pswitch_22  #00000007
        :pswitch_22  #00000008
        :pswitch_28  #00000009
        :pswitch_28  #0000000a
        :pswitch_22  #0000000b
        :pswitch_22  #0000000c
        :pswitch_22  #0000000d
        :pswitch_28  #0000000e
        :pswitch_28  #0000000f
        :pswitch_7  #00000010
        :pswitch_7  #00000011
        :pswitch_7  #00000012
        :pswitch_7  #00000013
        :pswitch_7  #00000014
        :pswitch_7  #00000015
        :pswitch_7  #00000016
        :pswitch_7  #00000017
        :pswitch_7  #00000018
        :pswitch_7  #00000019
        :pswitch_7  #0000001a
        :pswitch_7  #0000001b
        :pswitch_7  #0000001c
        :pswitch_7  #0000001d
        :pswitch_7  #0000001e
        :pswitch_7  #0000001f
        :pswitch_7  #00000020
        :pswitch_7  #00000021
        :pswitch_7  #00000022
        :pswitch_7  #00000023
        :pswitch_7  #00000024
        :pswitch_7  #00000025
        :pswitch_7  #00000026
        :pswitch_7  #00000027
        :pswitch_7  #00000028
        :pswitch_7  #00000029
        :pswitch_7  #0000002a
        :pswitch_7  #0000002b
        :pswitch_7  #0000002c
        :pswitch_7  #0000002d
        :pswitch_33  #0000002e
        :pswitch_7  #0000002f
        :pswitch_33  #00000030
        :pswitch_7  #00000031
        :pswitch_33  #00000032
        :pswitch_33  #00000033
        :pswitch_33  #00000034
        :pswitch_33  #00000035
        :pswitch_7  #00000036
        :pswitch_7  #00000037
        :pswitch_7  #00000038
        :pswitch_7  #00000039
        :pswitch_7  #0000003a
        :pswitch_7  #0000003b
        :pswitch_7  #0000003c
        :pswitch_7  #0000003d
        :pswitch_7  #0000003e
        :pswitch_7  #0000003f
        :pswitch_7  #00000040
        :pswitch_7  #00000041
        :pswitch_7  #00000042
        :pswitch_7  #00000043
        :pswitch_7  #00000044
        :pswitch_7  #00000045
        :pswitch_7  #00000046
        :pswitch_7  #00000047
        :pswitch_7  #00000048
        :pswitch_7  #00000049
        :pswitch_7  #0000004a
        :pswitch_7  #0000004b
        :pswitch_7  #0000004c
        :pswitch_7  #0000004d
        :pswitch_7  #0000004e
        :pswitch_3e  #0000004f
        :pswitch_48  #00000050
        :pswitch_3e  #00000051
        :pswitch_48  #00000052
        :pswitch_3e  #00000053
        :pswitch_3e  #00000054
        :pswitch_3e  #00000055
        :pswitch_3e  #00000056
        :pswitch_33  #00000057
        :pswitch_37  #00000058
        :pswitch_55  #00000059
        :pswitch_5d  #0000005a
        :pswitch_73  #0000005b
        :pswitch_8a  #0000005c
        :pswitch_b0  #0000005d
        :pswitch_d6  #0000005e
        :pswitch_fc  #0000005f
        :pswitch_33  #00000060
        :pswitch_37  #00000061
        :pswitch_33  #00000062
        :pswitch_37  #00000063
        :pswitch_33  #00000064
        :pswitch_37  #00000065
        :pswitch_33  #00000066
        :pswitch_37  #00000067
        :pswitch_33  #00000068
        :pswitch_37  #00000069
        :pswitch_33  #0000006a
        :pswitch_37  #0000006b
        :pswitch_33  #0000006c
        :pswitch_37  #0000006d
        :pswitch_33  #0000006e
        :pswitch_37  #0000006f
        :pswitch_33  #00000070
        :pswitch_37  #00000071
        :pswitch_33  #00000072
        :pswitch_37  #00000073
        :pswitch_7  #00000074
        :pswitch_7  #00000075
        :pswitch_7  #00000076
        :pswitch_7  #00000077
        :pswitch_33  #00000078
        :pswitch_33  #00000079
        :pswitch_33  #0000007a
        :pswitch_33  #0000007b
        :pswitch_33  #0000007c
        :pswitch_33  #0000007d
        :pswitch_33  #0000007e
        :pswitch_37  #0000007f
        :pswitch_33  #00000080
        :pswitch_37  #00000081
        :pswitch_33  #00000082
        :pswitch_37  #00000083
        :pswitch_7  #00000084
        :pswitch_22  #00000085
        :pswitch_7  #00000086
        :pswitch_22  #00000087
        :pswitch_33  #00000088
        :pswitch_33  #00000089
        :pswitch_7  #0000008a
        :pswitch_7  #0000008b
        :pswitch_22  #0000008c
        :pswitch_22  #0000008d
        :pswitch_33  #0000008e
        :pswitch_7  #0000008f
        :pswitch_33  #00000090
        :pswitch_7  #00000091
        :pswitch_7  #00000092
        :pswitch_7  #00000093
        :pswitch_3e  #00000094
        :pswitch_33  #00000095
        :pswitch_33  #00000096
        :pswitch_3e  #00000097
        :pswitch_3e  #00000098
        :pswitch_7  #00000099
        :pswitch_7  #0000009a
        :pswitch_7  #0000009b
        :pswitch_7  #0000009c
        :pswitch_7  #0000009d
        :pswitch_7  #0000009e
        :pswitch_7  #0000009f
        :pswitch_7  #000000a0
        :pswitch_7  #000000a1
        :pswitch_7  #000000a2
        :pswitch_7  #000000a3
        :pswitch_7  #000000a4
        :pswitch_7  #000000a5
        :pswitch_7  #000000a6
        :pswitch_7  #000000a7
        :pswitch_7  #000000a8
        :pswitch_7  #000000a9
        :pswitch_7  #000000aa
        :pswitch_7  #000000ab
        :pswitch_11  #000000ac
        :pswitch_18  #000000ad
        :pswitch_11  #000000ae
        :pswitch_18  #000000af
        :pswitch_11  #000000b0
        :pswitch_d  #000000b1
        :pswitch_7  #000000b2
        :pswitch_7  #000000b3
        :pswitch_7  #000000b4
        :pswitch_7  #000000b5
        :pswitch_7  #000000b6
        :pswitch_7  #000000b7
        :pswitch_7  #000000b8
        :pswitch_7  #000000b9
        :pswitch_7  #000000ba
        :pswitch_7  #000000bb
        :pswitch_7  #000000bc
        :pswitch_7  #000000bd
        :pswitch_7  #000000be
        :pswitch_11  #000000bf
        :pswitch_7  #000000c0
        :pswitch_7  #000000c1
        :pswitch_33  #000000c2
        :pswitch_33  #000000c3
    .end packed-switch

    :sswitch_data_2ac
    .sparse-switch
        0xac -> :sswitch_11d
        0xad -> :sswitch_11d
        0xae -> :sswitch_11d
        0xaf -> :sswitch_11d
        0xb0 -> :sswitch_11d
        0xb1 -> :sswitch_11d
        0xbf -> :sswitch_11d
    .end sparse-switch
.end method

.method public visitIntInsn(II)V
    .registers 4

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2}, Lorg/objectweb/asm/MethodVisitor;->visitIntInsn(II)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_12

    const/16 v0, 0xbc

    if-eq p1, v0, :cond_12

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_12
    return-void
.end method

.method public varargs visitInvokeDynamicInsn(Ljava/lang/String;Ljava/lang/String;Lorg/objectweb/asm/Handle;[Ljava/lang/Object;)V
    .registers 9

    const/4 v3, 0x2

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2, p3, p4}, Lorg/objectweb/asm/MethodVisitor;->visitInvokeDynamicInsn(Ljava/lang/String;Ljava/lang/String;Lorg/objectweb/asm/Handle;[Ljava/lang/Object;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_3b

    invoke-static {p2}, Lorg/objectweb/asm/Type;->getArgumentTypes(Ljava/lang/String;)[Lorg/objectweb/asm/Type;

    move-result-object v1

    const/4 v0, 0x0

    :goto_f
    array-length v2, v1

    if-ge v0, v2, :cond_23

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    aget-object v2, v1, v0

    invoke-virtual {v2}, Lorg/objectweb/asm/Type;->getSize()I

    move-result v2

    if-ne v2, v3, :cond_20

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    :cond_20
    add-int/lit8 v0, v0, 0x1

    goto :goto_f

    :cond_23
    invoke-static {p2}, Lorg/objectweb/asm/Type;->getReturnType(Ljava/lang/String;)Lorg/objectweb/asm/Type;

    move-result-object v0

    sget-object v1, Lorg/objectweb/asm/Type;->VOID_TYPE:Lorg/objectweb/asm/Type;

    if-eq v0, v1, :cond_3b

    sget-object v1, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v1}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    invoke-virtual {v0}, Lorg/objectweb/asm/Type;->getSize()I

    move-result v0

    if-ne v0, v3, :cond_3b

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_3b
    return-void
.end method

.method public visitJumpInsn(ILorg/objectweb/asm/Label;)V
    .registers 4

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2}, Lorg/objectweb/asm/MethodVisitor;->visitJumpInsn(ILorg/objectweb/asm/Label;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_f

    sparse-switch p1, :sswitch_data_22

    :goto_c
    invoke-direct {p0, p2}, Lorg/objectweb/asm/commons/AdviceAdapter;->addBranch(Lorg/objectweb/asm/Label;)V

    :cond_f
    return-void

    :sswitch_10
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_c

    :sswitch_14
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_c

    :sswitch_1b
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_c

    nop

    :sswitch_data_22
    .sparse-switch
        0x99 -> :sswitch_10
        0x9a -> :sswitch_10
        0x9b -> :sswitch_10
        0x9c -> :sswitch_10
        0x9d -> :sswitch_10
        0x9e -> :sswitch_10
        0x9f -> :sswitch_14
        0xa0 -> :sswitch_14
        0xa1 -> :sswitch_14
        0xa2 -> :sswitch_14
        0xa3 -> :sswitch_14
        0xa4 -> :sswitch_14
        0xa5 -> :sswitch_14
        0xa6 -> :sswitch_14
        0xa8 -> :sswitch_1b
        0xc6 -> :sswitch_10
        0xc7 -> :sswitch_10
    .end sparse-switch
.end method

.method public visitLabel(Lorg/objectweb/asm/Label;)V
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1}, Lorg/objectweb/asm/MethodVisitor;->visitLabel(Lorg/objectweb/asm/Label;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_1e

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    if-eqz v0, :cond_1e

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    invoke-interface {v0, p1}, Ljava/util/Map;->get(Ljava/lang/Object;)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Ljava/util/List;

    if-eqz v0, :cond_1e

    iput-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->stackFrame:Ljava/util/List;

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    invoke-interface {v0, p1}, Ljava/util/Map;->remove(Ljava/lang/Object;)Ljava/lang/Object;

    :cond_1e
    return-void
.end method

.method public visitLdcInsn(Ljava/lang/Object;)V
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1}, Lorg/objectweb/asm/MethodVisitor;->visitLdcInsn(Ljava/lang/Object;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_1b

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    instance-of v0, p1, Ljava/lang/Double;

    if-nez v0, :cond_16

    instance-of v0, p1, Ljava/lang/Long;

    if-eqz v0, :cond_1b

    :cond_16
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_1b
    return-void
.end method

.method public visitLookupSwitchInsn(Lorg/objectweb/asm/Label;[I[Lorg/objectweb/asm/Label;)V
    .registers 5

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2, p3}, Lorg/objectweb/asm/MethodVisitor;->visitLookupSwitchInsn(Lorg/objectweb/asm/Label;[I[Lorg/objectweb/asm/Label;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_f

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0, p1, p3}, Lorg/objectweb/asm/commons/AdviceAdapter;->addBranches(Lorg/objectweb/asm/Label;[Lorg/objectweb/asm/Label;)V

    :cond_f
    return-void
.end method

.method public visitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;)V
    .registers 11

    iget v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->api:I

    const/high16 v1, 0x50000

    if-lt v0, v1, :cond_a

    invoke-super {p0, p1, p2, p3, p4}, Lorg/objectweb/asm/commons/GeneratorAdapter;->visitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;)V

    :goto_9
    return-void

    :cond_a
    const/16 v0, 0xb9

    if-ne p1, v0, :cond_18

    const/4 v5, 0x1

    :goto_f
    move-object v0, p0

    move v1, p1

    move-object v2, p2

    move-object v3, p3

    move-object v4, p4

    invoke-direct/range {v0 .. v5}, Lorg/objectweb/asm/commons/AdviceAdapter;->doVisitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V

    goto :goto_9

    :cond_18
    const/4 v5, 0x0

    goto :goto_f
.end method

.method public visitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V
    .registers 8

    iget v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->api:I

    const/high16 v1, 0x50000

    if-ge v0, v1, :cond_a

    invoke-super/range {p0 .. p5}, Lorg/objectweb/asm/commons/GeneratorAdapter;->visitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V

    :goto_9
    return-void

    :cond_a
    invoke-direct/range {p0 .. p5}, Lorg/objectweb/asm/commons/AdviceAdapter;->doVisitMethodInsn(ILjava/lang/String;Ljava/lang/String;Ljava/lang/String;Z)V

    goto :goto_9
.end method

.method public visitMultiANewArrayInsn(Ljava/lang/String;I)V
    .registers 4

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2}, Lorg/objectweb/asm/MethodVisitor;->visitMultiANewArrayInsn(Ljava/lang/String;I)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_17

    const/4 v0, 0x0

    :goto_a
    if-ge v0, p2, :cond_12

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    add-int/lit8 v0, v0, 0x1

    goto :goto_a

    :cond_12
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_17
    return-void
.end method

.method public varargs visitTableSwitchInsn(IILorg/objectweb/asm/Label;[Lorg/objectweb/asm/Label;)V
    .registers 6

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2, p3, p4}, Lorg/objectweb/asm/MethodVisitor;->visitTableSwitchInsn(IILorg/objectweb/asm/Label;[Lorg/objectweb/asm/Label;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_f

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0, p3, p4}, Lorg/objectweb/asm/commons/AdviceAdapter;->addBranches(Lorg/objectweb/asm/Label;[Lorg/objectweb/asm/Label;)V

    :cond_f
    return-void
.end method

.method public visitTryCatchBlock(Lorg/objectweb/asm/Label;Lorg/objectweb/asm/Label;Lorg/objectweb/asm/Label;Ljava/lang/String;)V
    .registers 7

    invoke-super {p0, p1, p2, p3, p4}, Lorg/objectweb/asm/commons/GeneratorAdapter;->visitTryCatchBlock(Lorg/objectweb/asm/Label;Lorg/objectweb/asm/Label;Lorg/objectweb/asm/Label;Ljava/lang/String;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_1e

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    invoke-interface {v0, p3}, Ljava/util/Map;->containsKey(Ljava/lang/Object;)Z

    move-result v0

    if-nez v0, :cond_1e

    new-instance v0, Ljava/util/ArrayList;

    invoke-direct {v0}, Ljava/util/ArrayList;-><init>()V

    sget-object v1, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-interface {v0, v1}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    iget-object v1, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->branches:Ljava/util/Map;

    invoke-interface {v1, p3, v0}, Ljava/util/Map;->put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;

    :cond_1e
    return-void
.end method

.method public visitTypeInsn(ILjava/lang/String;)V
    .registers 4

    iget-object v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->mv:Lorg/objectweb/asm/MethodVisitor;

    invoke-virtual {v0, p1, p2}, Lorg/objectweb/asm/MethodVisitor;->visitTypeInsn(ILjava/lang/String;)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_12

    const/16 v0, 0xbb

    if-ne p1, v0, :cond_12

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    :cond_12
    return-void
.end method

.method public visitVarInsn(II)V
    .registers 4

    invoke-super {p0, p1, p2}, Lorg/objectweb/asm/commons/GeneratorAdapter;->visitVarInsn(II)V

    iget-boolean v0, p0, Lorg/objectweb/asm/commons/AdviceAdapter;->constructor:Z

    if-eqz v0, :cond_a

    sparse-switch p1, :sswitch_data_32

    :cond_a
    :goto_a
    return-void

    :sswitch_b
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_a

    :sswitch_11
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_a

    :sswitch_1c
    if-nez p2, :cond_24

    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->THIS:Ljava/lang/Object;

    :goto_20
    invoke-direct {p0, v0}, Lorg/objectweb/asm/commons/AdviceAdapter;->pushValue(Ljava/lang/Object;)V

    goto :goto_a

    :cond_24
    sget-object v0, Lorg/objectweb/asm/commons/AdviceAdapter;->OTHER:Ljava/lang/Object;

    goto :goto_20

    :sswitch_27
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_a

    :sswitch_2b
    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    invoke-direct {p0}, Lorg/objectweb/asm/commons/AdviceAdapter;->popValue()Ljava/lang/Object;

    goto :goto_a

    :sswitch_data_32
    .sparse-switch
        0x15 -> :sswitch_b
        0x16 -> :sswitch_11
        0x17 -> :sswitch_b
        0x18 -> :sswitch_11
        0x19 -> :sswitch_1c
        0x36 -> :sswitch_27
        0x37 -> :sswitch_2b
        0x38 -> :sswitch_27
        0x39 -> :sswitch_2b
        0x3a -> :sswitch_27
    .end sparse-switch
.end method
