.class public Lorg/objectweb/asm/tree/analysis/Analyzer;
.super Ljava/lang/Object;

# interfaces
.implements Lorg/objectweb/asm/Opcodes;


# instance fields
.field private frames:[Lorg/objectweb/asm/tree/analysis/Frame;

.field private handlers:[Ljava/util/List;

.field private insns:Lorg/objectweb/asm/tree/InsnList;

.field private final interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

.field private n:I

.field private queue:[I

.field private queued:[Z

.field private subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

.field private top:I


# direct methods
.method public constructor <init>(Lorg/objectweb/asm/tree/analysis/Interpreter;)V
    .registers 2

    invoke-direct {p0}, Ljava/lang/Object;-><init>()V

    iput-object p1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    return-void
.end method

.method private findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V
    .registers 9
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/objectweb/asm/tree/analysis/AnalyzerException;
        }
    .end annotation

    :goto_0
    if-ltz p1, :cond_6

    iget v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    if-lt p1, v0, :cond_f

    :cond_6
    new-instance v0, Lorg/objectweb/asm/tree/analysis/AnalyzerException;

    const/4 v1, 0x0

    const-string v2, "Execution can fall off end of the code"

    invoke-direct {v0, v1, v2}, Lorg/objectweb/asm/tree/analysis/AnalyzerException;-><init>(Lorg/objectweb/asm/tree/AbstractInsnNode;Ljava/lang/String;)V

    throw v0

    :cond_f
    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v0, v0, p1

    if-eqz v0, :cond_16

    :pswitch_15  #0xa7, 0xa9, 0xaa, 0xab, 0xac, 0xad, 0xae, 0xaf, 0xb0, 0xb1, 0xbf
    return-void

    :cond_16
    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    invoke-virtual {p2}, Lorg/objectweb/asm/tree/analysis/Subroutine;->copy()Lorg/objectweb/asm/tree/analysis/Subroutine;

    move-result-object v1

    aput-object v1, v0, p1

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v0, p1}, Lorg/objectweb/asm/tree/InsnList;->get(I)Lorg/objectweb/asm/tree/AbstractInsnNode;

    move-result-object v1

    instance-of v0, v1, Lorg/objectweb/asm/tree/JumpInsnNode;

    if-eqz v0, :cond_65

    invoke-virtual {v1}, Lorg/objectweb/asm/tree/AbstractInsnNode;->getOpcode()I

    move-result v0

    const/16 v2, 0xa8

    if-ne v0, v2, :cond_56

    invoke-interface {p3, v1}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    :cond_33
    :goto_33
    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    aget-object v3, v0, p1

    if-eqz v3, :cond_c9

    const/4 v0, 0x0

    move v2, v0

    :goto_3b
    invoke-interface {v3}, Ljava/util/List;->size()I

    move-result v0

    if-ge v2, v0, :cond_c9

    invoke-interface {v3, v2}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/TryCatchBlockNode;

    iget-object v4, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v0, v0, Lorg/objectweb/asm/tree/TryCatchBlockNode;->handler:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v4, v0}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v0

    invoke-direct {p0, v0, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    add-int/lit8 v0, v2, 0x1

    move v2, v0

    goto :goto_3b

    :cond_56
    move-object v0, v1

    check-cast v0, Lorg/objectweb/asm/tree/JumpInsnNode;

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v0, v0, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v2, v0}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v0

    invoke-direct {p0, v0, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    goto :goto_33

    :cond_65
    instance-of v0, v1, Lorg/objectweb/asm/tree/TableSwitchInsnNode;

    if-eqz v0, :cond_97

    move-object v0, v1

    check-cast v0, Lorg/objectweb/asm/tree/TableSwitchInsnNode;

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v3, v0, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->dflt:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v2, v3}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    iget-object v2, v0, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2}, Ljava/util/List;->size()I

    move-result v2

    add-int/lit8 v2, v2, -0x1

    move v3, v2

    :goto_80
    if-ltz v3, :cond_33

    iget-object v2, v0, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v2

    check-cast v2, Lorg/objectweb/asm/tree/LabelNode;

    iget-object v4, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v4, v2}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    add-int/lit8 v2, v3, -0x1

    move v3, v2

    goto :goto_80

    :cond_97
    instance-of v0, v1, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;

    if-eqz v0, :cond_33

    move-object v0, v1

    check-cast v0, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v3, v0, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->dflt:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v2, v3}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    iget-object v2, v0, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2}, Ljava/util/List;->size()I

    move-result v2

    add-int/lit8 v2, v2, -0x1

    move v3, v2

    :goto_b2
    if-ltz v3, :cond_33

    iget-object v2, v0, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v2

    check-cast v2, Lorg/objectweb/asm/tree/LabelNode;

    iget-object v4, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v4, v2}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, p2, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    add-int/lit8 v2, v3, -0x1

    move v3, v2

    goto :goto_b2

    :cond_c9
    invoke-virtual {v1}, Lorg/objectweb/asm/tree/AbstractInsnNode;->getOpcode()I

    move-result v0

    packed-switch v0, :pswitch_data_d4

    :pswitch_d0  #0xa8, 0xb2, 0xb3, 0xb4, 0xb5, 0xb6, 0xb7, 0xb8, 0xb9, 0xba, 0xbb, 0xbc, 0xbd, 0xbe
    add-int/lit8 p1, p1, 0x1

    goto/16 :goto_0

    :pswitch_data_d4
    .packed-switch 0xa7
        :pswitch_15  #000000a7
        :pswitch_d0  #000000a8
        :pswitch_15  #000000a9
        :pswitch_15  #000000aa
        :pswitch_15  #000000ab
        :pswitch_15  #000000ac
        :pswitch_15  #000000ad
        :pswitch_15  #000000ae
        :pswitch_15  #000000af
        :pswitch_15  #000000b0
        :pswitch_15  #000000b1
        :pswitch_d0  #000000b2
        :pswitch_d0  #000000b3
        :pswitch_d0  #000000b4
        :pswitch_d0  #000000b5
        :pswitch_d0  #000000b6
        :pswitch_d0  #000000b7
        :pswitch_d0  #000000b8
        :pswitch_d0  #000000b9
        :pswitch_d0  #000000ba
        :pswitch_d0  #000000bb
        :pswitch_d0  #000000bc
        :pswitch_d0  #000000bd
        :pswitch_d0  #000000be
        :pswitch_15  #000000bf
    .end packed-switch
.end method

.method private merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;[Z)V
    .registers 10
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/objectweb/asm/tree/analysis/AnalyzerException;
        }
    .end annotation

    const/4 v1, 0x1

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    aget-object v0, v0, p1

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v2, v2, p1

    invoke-virtual {p3, p2, p5}, Lorg/objectweb/asm/tree/analysis/Frame;->merge(Lorg/objectweb/asm/tree/analysis/Frame;[Z)Z

    if-nez v0, :cond_37

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    invoke-virtual {p0, p3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newFrame(Lorg/objectweb/asm/tree/analysis/Frame;)Lorg/objectweb/asm/tree/analysis/Frame;

    move-result-object v3

    aput-object v3, v0, p1

    move v0, v1

    :goto_17
    if-eqz v2, :cond_20

    if-eqz p4, :cond_20

    invoke-virtual {v2, p4}, Lorg/objectweb/asm/tree/analysis/Subroutine;->merge(Lorg/objectweb/asm/tree/analysis/Subroutine;)Z

    move-result v2

    or-int/2addr v0, v2

    :cond_20
    if-eqz v0, :cond_36

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    aget-boolean v0, v0, p1

    if-nez v0, :cond_36

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    aput-boolean v1, v0, p1

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queue:[I

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    add-int/lit8 v2, v1, 0x1

    iput v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    aput p1, v0, v1

    :cond_36
    return-void

    :cond_37
    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    invoke-virtual {v0, p3, v3}, Lorg/objectweb/asm/tree/analysis/Frame;->merge(Lorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Interpreter;)Z

    move-result v0

    goto :goto_17
.end method

.method private merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V
    .registers 8
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/objectweb/asm/tree/analysis/AnalyzerException;
        }
    .end annotation

    const/4 v1, 0x1

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    aget-object v0, v0, p1

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v2, v2, p1

    if-nez v0, :cond_38

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    invoke-virtual {p0, p2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newFrame(Lorg/objectweb/asm/tree/analysis/Frame;)Lorg/objectweb/asm/tree/analysis/Frame;

    move-result-object v3

    aput-object v3, v0, p1

    move v0, v1

    :goto_14
    if-nez v2, :cond_3f

    if-eqz p3, :cond_21

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    invoke-virtual {p3}, Lorg/objectweb/asm/tree/analysis/Subroutine;->copy()Lorg/objectweb/asm/tree/analysis/Subroutine;

    move-result-object v2

    aput-object v2, v0, p1

    move v0, v1

    :cond_21
    :goto_21
    if-eqz v0, :cond_37

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    aget-boolean v0, v0, p1

    if-nez v0, :cond_37

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    aput-boolean v1, v0, p1

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queue:[I

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    add-int/lit8 v2, v1, 0x1

    iput v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    aput p1, v0, v1

    :cond_37
    return-void

    :cond_38
    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    invoke-virtual {v0, p2, v3}, Lorg/objectweb/asm/tree/analysis/Frame;->merge(Lorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Interpreter;)Z

    move-result v0

    goto :goto_14

    :cond_3f
    if-eqz p3, :cond_21

    invoke-virtual {v2, p3}, Lorg/objectweb/asm/tree/analysis/Subroutine;->merge(Lorg/objectweb/asm/tree/analysis/Subroutine;)Z

    move-result v2

    or-int/2addr v0, v2

    goto :goto_21
.end method


# virtual methods
.method public analyze(Ljava/lang/String;Lorg/objectweb/asm/tree/MethodNode;)[Lorg/objectweb/asm/tree/analysis/Frame;
    .registers 17
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/objectweb/asm/tree/analysis/AnalyzerException;
        }
    .end annotation

    move-object/from16 v0, p2

    iget v1, v0, Lorg/objectweb/asm/tree/MethodNode;->access:I

    and-int/lit16 v1, v1, 0x500

    if-eqz v1, :cond_12

    const/4 v1, 0x0

    new-array v1, v1, [Lorg/objectweb/asm/tree/analysis/Frame;

    check-cast v1, [Lorg/objectweb/asm/tree/analysis/Frame;

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    :goto_11
    return-object v1

    :cond_12
    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->instructions:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v1}, Lorg/objectweb/asm/tree/InsnList;->size()I

    move-result v1

    iput v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->instructions:Lorg/objectweb/asm/tree/InsnList;

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    new-array v1, v1, [Ljava/util/List;

    check-cast v1, [Ljava/util/List;

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    new-array v1, v1, [Lorg/objectweb/asm/tree/analysis/Frame;

    check-cast v1, [Lorg/objectweb/asm/tree/analysis/Frame;

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    new-array v1, v1, [Lorg/objectweb/asm/tree/analysis/Subroutine;

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    new-array v1, v1, [Z

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    new-array v1, v1, [I

    iput-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queue:[I

    const/4 v1, 0x0

    iput v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    const/4 v1, 0x0

    move v2, v1

    :goto_49
    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->tryCatchBlocks:Ljava/util/List;

    invoke-interface {v1}, Ljava/util/List;->size()I

    move-result v1

    if-ge v2, v1, :cond_8a

    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->tryCatchBlocks:Ljava/util/List;

    invoke-interface {v1, v2}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v1

    check-cast v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;

    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v4, v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;->start:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v3, v4}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v3

    iget-object v4, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v5, v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;->end:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v4, v5}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v5

    move v4, v3

    :goto_6e
    if-ge v4, v5, :cond_86

    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    aget-object v3, v3, v4

    if-nez v3, :cond_7f

    new-instance v3, Ljava/util/ArrayList;

    invoke-direct {v3}, Ljava/util/ArrayList;-><init>()V

    iget-object v6, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    aput-object v3, v6, v4

    :cond_7f
    invoke-interface {v3, v1}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    add-int/lit8 v3, v4, 0x1

    move v4, v3

    goto :goto_6e

    :cond_86
    add-int/lit8 v1, v2, 0x1

    move v2, v1

    goto :goto_49

    :cond_8a
    new-instance v1, Lorg/objectweb/asm/tree/analysis/Subroutine;

    const/4 v2, 0x0

    move-object/from16 v0, p2

    iget v3, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    const/4 v4, 0x0

    invoke-direct {v1, v2, v3, v4}, Lorg/objectweb/asm/tree/analysis/Subroutine;-><init>(Lorg/objectweb/asm/tree/LabelNode;ILorg/objectweb/asm/tree/JumpInsnNode;)V

    new-instance v3, Ljava/util/ArrayList;

    invoke-direct {v3}, Ljava/util/ArrayList;-><init>()V

    new-instance v4, Ljava/util/HashMap;

    invoke-direct {v4}, Ljava/util/HashMap;-><init>()V

    const/4 v2, 0x0

    invoke-direct {p0, v2, v1, v3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    :goto_a3
    invoke-interface {v3}, Ljava/util/List;->isEmpty()Z

    move-result v1

    if-nez v1, :cond_dd

    const/4 v1, 0x0

    invoke-interface {v3, v1}, Ljava/util/List;->remove(I)Ljava/lang/Object;

    move-result-object v1

    move-object v2, v1

    check-cast v2, Lorg/objectweb/asm/tree/JumpInsnNode;

    iget-object v1, v2, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    invoke-interface {v4, v1}, Ljava/util/Map;->get(Ljava/lang/Object;)Ljava/lang/Object;

    move-result-object v1

    check-cast v1, Lorg/objectweb/asm/tree/analysis/Subroutine;

    if-nez v1, :cond_d7

    new-instance v1, Lorg/objectweb/asm/tree/analysis/Subroutine;

    iget-object v5, v2, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    move-object/from16 v0, p2

    iget v6, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    invoke-direct {v1, v5, v6, v2}, Lorg/objectweb/asm/tree/analysis/Subroutine;-><init>(Lorg/objectweb/asm/tree/LabelNode;ILorg/objectweb/asm/tree/JumpInsnNode;)V

    iget-object v5, v2, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    invoke-interface {v4, v5, v1}, Ljava/util/Map;->put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object;

    iget-object v5, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v2, v2, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v5, v2}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, v1, v3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->findSubroutine(ILorg/objectweb/asm/tree/analysis/Subroutine;Ljava/util/List;)V

    goto :goto_a3

    :cond_d7
    iget-object v1, v1, Lorg/objectweb/asm/tree/analysis/Subroutine;->callers:Ljava/util/List;

    invoke-interface {v1, v2}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    goto :goto_a3

    :cond_dd
    const/4 v1, 0x0

    :goto_de
    iget v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->n:I

    if-ge v1, v2, :cond_f8

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v2, v2, v1

    if-eqz v2, :cond_f5

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v2, v2, v1

    iget-object v2, v2, Lorg/objectweb/asm/tree/analysis/Subroutine;->start:Lorg/objectweb/asm/tree/LabelNode;

    if-nez v2, :cond_f5

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    const/4 v3, 0x0

    aput-object v3, v2, v1

    :cond_f5
    add-int/lit8 v1, v1, 0x1

    goto :goto_de

    :cond_f8
    move-object/from16 v0, p2

    iget v1, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    move-object/from16 v0, p2

    iget v2, v0, Lorg/objectweb/asm/tree/MethodNode;->maxStack:I

    invoke-virtual {p0, v1, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newFrame(II)Lorg/objectweb/asm/tree/analysis/Frame;

    move-result-object v4

    move-object/from16 v0, p2

    iget v1, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    move-object/from16 v0, p2

    iget v2, v0, Lorg/objectweb/asm/tree/MethodNode;->maxStack:I

    invoke-virtual {p0, v1, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newFrame(II)Lorg/objectweb/asm/tree/analysis/Frame;

    move-result-object v10

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    move-object/from16 v0, p2

    iget-object v2, v0, Lorg/objectweb/asm/tree/MethodNode;->desc:Ljava/lang/String;

    invoke-static {v2}, Lorg/objectweb/asm/Type;->getReturnType(Ljava/lang/String;)Lorg/objectweb/asm/Type;

    move-result-object v2

    invoke-virtual {v1, v2}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v1

    invoke-virtual {v4, v1}, Lorg/objectweb/asm/tree/analysis/Frame;->setReturn(Lorg/objectweb/asm/tree/analysis/Value;)V

    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->desc:Ljava/lang/String;

    invoke-static {v1}, Lorg/objectweb/asm/Type;->getArgumentTypes(Ljava/lang/String;)[Lorg/objectweb/asm/Type;

    move-result-object v5

    move-object/from16 v0, p2

    iget v1, v0, Lorg/objectweb/asm/tree/MethodNode;->access:I

    and-int/lit8 v1, v1, 0x8

    if-nez v1, :cond_3c1

    invoke-static {p1}, Lorg/objectweb/asm/Type;->getObjectType(Ljava/lang/String;)Lorg/objectweb/asm/Type;

    move-result-object v2

    const/4 v1, 0x1

    const/4 v3, 0x0

    iget-object v6, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    invoke-virtual {v6, v2}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v2

    invoke-virtual {v4, v3, v2}, Lorg/objectweb/asm/tree/analysis/Frame;->setLocal(ILorg/objectweb/asm/tree/analysis/Value;)V

    :goto_140
    const/4 v2, 0x0

    move v3, v1

    :goto_142
    array-length v1, v5

    if-ge v2, v1, :cond_16b

    add-int/lit8 v1, v3, 0x1

    iget-object v6, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    aget-object v7, v5, v2

    invoke-virtual {v6, v7}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v6

    invoke-virtual {v4, v3, v6}, Lorg/objectweb/asm/tree/analysis/Frame;->setLocal(ILorg/objectweb/asm/tree/analysis/Value;)V

    aget-object v3, v5, v2

    invoke-virtual {v3}, Lorg/objectweb/asm/Type;->getSize()I

    move-result v3

    const/4 v6, 0x2

    if-ne v3, v6, :cond_3be

    add-int/lit8 v3, v1, 0x1

    iget-object v6, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    const/4 v7, 0x0

    invoke-virtual {v6, v7}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v6

    invoke-virtual {v4, v1, v6}, Lorg/objectweb/asm/tree/analysis/Frame;->setLocal(ILorg/objectweb/asm/tree/analysis/Value;)V

    :goto_167
    add-int/lit8 v1, v2, 0x1

    move v2, v1

    goto :goto_142

    :cond_16b
    :goto_16b
    move-object/from16 v0, p2

    iget v1, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    if-ge v3, v1, :cond_17e

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    const/4 v2, 0x0

    invoke-virtual {v1, v2}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v1

    invoke-virtual {v4, v3, v1}, Lorg/objectweb/asm/tree/analysis/Frame;->setLocal(ILorg/objectweb/asm/tree/analysis/Value;)V

    add-int/lit8 v3, v3, 0x1

    goto :goto_16b

    :cond_17e
    const/4 v1, 0x0

    const/4 v2, 0x0

    invoke-direct {p0, v1, v4, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    invoke-virtual/range {p0 .. p2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->init(Ljava/lang/String;Lorg/objectweb/asm/tree/MethodNode;)V

    :cond_186
    iget v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    if-lez v1, :cond_3ba

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queue:[I

    iget v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    add-int/lit8 v2, v2, -0x1

    iput v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->top:I

    aget v11, v1, v2

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    aget-object v12, v1, v11

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v8, v1, v11

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->queued:[Z

    const/4 v2, 0x0

    aput-boolean v2, v1, v11

    const/4 v7, 0x0

    :try_start_1a2
    move-object/from16 v0, p2

    iget-object v1, v0, Lorg/objectweb/asm/tree/MethodNode;->instructions:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v1, v11}, Lorg/objectweb/asm/tree/InsnList;->get(I)Lorg/objectweb/asm/tree/AbstractInsnNode;

    move-result-object v7

    invoke-virtual {v7}, Lorg/objectweb/asm/tree/AbstractInsnNode;->getOpcode()I

    move-result v2

    invoke-virtual {v7}, Lorg/objectweb/asm/tree/AbstractInsnNode;->getType()I

    move-result v1

    const/16 v3, 0x8

    if-eq v1, v3, :cond_1be

    const/16 v3, 0xf

    if-eq v1, v3, :cond_1be

    const/16 v3, 0xe

    if-ne v1, v3, :cond_20a

    :cond_1be
    add-int/lit8 v1, v11, 0x1

    invoke-direct {p0, v1, v12, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    add-int/lit8 v1, v11, 0x1

    invoke-virtual {p0, v11, v1}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    :cond_1c8
    :goto_1c8
    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    aget-object v5, v1, v11

    if-eqz v5, :cond_186

    const/4 v1, 0x0

    move v3, v1

    :goto_1d0
    invoke-interface {v5}, Ljava/util/List;->size()I

    move-result v1

    if-ge v3, v1, :cond_186

    invoke-interface {v5, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v1

    check-cast v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;

    iget-object v2, v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;->type:Ljava/lang/String;

    if-nez v2, :cond_3b2

    const-string v2, "java/lang/Throwable"

    invoke-static {v2}, Lorg/objectweb/asm/Type;->getObjectType(Ljava/lang/String;)Lorg/objectweb/asm/Type;

    move-result-object v2

    :goto_1e6
    iget-object v6, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v9, v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;->handler:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v6, v9}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v6

    invoke-virtual {p0, v11, v1}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowExceptionEdge(ILorg/objectweb/asm/tree/TryCatchBlockNode;)Z

    move-result v1

    if-eqz v1, :cond_206

    invoke-virtual {v10, v12}, Lorg/objectweb/asm/tree/analysis/Frame;->init(Lorg/objectweb/asm/tree/analysis/Frame;)Lorg/objectweb/asm/tree/analysis/Frame;

    invoke-virtual {v10}, Lorg/objectweb/asm/tree/analysis/Frame;->clearStack()V

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    invoke-virtual {v1, v2}, Lorg/objectweb/asm/tree/analysis/Interpreter;->newValue(Lorg/objectweb/asm/Type;)Lorg/objectweb/asm/tree/analysis/Value;

    move-result-object v1

    invoke-virtual {v10, v1}, Lorg/objectweb/asm/tree/analysis/Frame;->push(Lorg/objectweb/asm/tree/analysis/Value;)V

    invoke-direct {p0, v6, v10, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    :cond_206
    add-int/lit8 v1, v3, 0x1

    move v3, v1

    goto :goto_1d0

    :cond_20a
    invoke-virtual {v4, v12}, Lorg/objectweb/asm/tree/analysis/Frame;->init(Lorg/objectweb/asm/tree/analysis/Frame;)Lorg/objectweb/asm/tree/analysis/Frame;

    move-result-object v1

    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->interpreter:Lorg/objectweb/asm/tree/analysis/Interpreter;

    invoke-virtual {v1, v7, v3}, Lorg/objectweb/asm/tree/analysis/Frame;->execute(Lorg/objectweb/asm/tree/AbstractInsnNode;Lorg/objectweb/asm/tree/analysis/Interpreter;)V

    if-nez v8, :cond_27b

    const/4 v1, 0x0

    move-object v8, v1

    :goto_217
    nop

    instance-of v1, v7, Lorg/objectweb/asm/tree/JumpInsnNode;

    if-eqz v1, :cond_2ad

    move-object v0, v7

    check-cast v0, Lorg/objectweb/asm/tree/JumpInsnNode;

    move-object v1, v0

    const/16 v3, 0xa7

    if-eq v2, v3, :cond_232

    const/16 v3, 0xa8

    if-eq v2, v3, :cond_232

    add-int/lit8 v3, v11, 0x1

    invoke-direct {p0, v3, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    add-int/lit8 v3, v11, 0x1

    invoke-virtual {p0, v11, v3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    :cond_232
    iget-object v3, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v5, v1, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v3, v5}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v3

    const/16 v5, 0xa8

    if-ne v2, v5, :cond_281

    new-instance v2, Lorg/objectweb/asm/tree/analysis/Subroutine;

    iget-object v5, v1, Lorg/objectweb/asm/tree/JumpInsnNode;->label:Lorg/objectweb/asm/tree/LabelNode;

    move-object/from16 v0, p2

    iget v6, v0, Lorg/objectweb/asm/tree/MethodNode;->maxLocals:I

    invoke-direct {v2, v5, v6, v1}, Lorg/objectweb/asm/tree/analysis/Subroutine;-><init>(Lorg/objectweb/asm/tree/LabelNode;ILorg/objectweb/asm/tree/JumpInsnNode;)V

    invoke-direct {p0, v3, v4, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    :goto_24c
    invoke-virtual {p0, v11, v3}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V
    :try_end_24f
    .catch Lorg/objectweb/asm/tree/analysis/AnalyzerException; {:try_start_1a2 .. :try_end_24f} :catch_251
    .catch Ljava/lang/Exception; {:try_start_1a2 .. :try_end_24f} :catch_285

    goto/16 :goto_1c8

    :catch_251
    move-exception v1

    new-instance v2, Lorg/objectweb/asm/tree/analysis/AnalyzerException;

    iget-object v3, v1, Lorg/objectweb/asm/tree/analysis/AnalyzerException;->node:Lorg/objectweb/asm/tree/AbstractInsnNode;

    new-instance v4, Ljava/lang/StringBuffer;

    invoke-direct {v4}, Ljava/lang/StringBuffer;-><init>()V

    const-string v5, "Error at instruction "

    invoke-virtual {v4, v5}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v4

    invoke-virtual {v4, v11}, Ljava/lang/StringBuffer;->append(I)Ljava/lang/StringBuffer;

    move-result-object v4

    const-string v5, ": "

    invoke-virtual {v4, v5}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v4

    invoke-virtual {v1}, Lorg/objectweb/asm/tree/analysis/AnalyzerException;->getMessage()Ljava/lang/String;

    move-result-object v5

    invoke-virtual {v4, v5}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v4

    invoke-virtual {v4}, Ljava/lang/StringBuffer;->toString()Ljava/lang/String;

    move-result-object v4

    invoke-direct {v2, v3, v4, v1}, Lorg/objectweb/asm/tree/analysis/AnalyzerException;-><init>(Lorg/objectweb/asm/tree/AbstractInsnNode;Ljava/lang/String;Ljava/lang/Throwable;)V

    throw v2

    :cond_27b
    :try_start_27b
    invoke-virtual {v8}, Lorg/objectweb/asm/tree/analysis/Subroutine;->copy()Lorg/objectweb/asm/tree/analysis/Subroutine;

    move-result-object v1

    move-object v8, v1

    goto :goto_217

    :cond_281
    invoke-direct {p0, v3, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V
    :try_end_284
    .catch Lorg/objectweb/asm/tree/analysis/AnalyzerException; {:try_start_27b .. :try_end_284} :catch_251
    .catch Ljava/lang/Exception; {:try_start_27b .. :try_end_284} :catch_285

    goto :goto_24c

    :catch_285
    move-exception v1

    new-instance v2, Lorg/objectweb/asm/tree/analysis/AnalyzerException;

    new-instance v3, Ljava/lang/StringBuffer;

    invoke-direct {v3}, Ljava/lang/StringBuffer;-><init>()V

    const-string v4, "Error at instruction "

    invoke-virtual {v3, v4}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v3

    invoke-virtual {v3, v11}, Ljava/lang/StringBuffer;->append(I)Ljava/lang/StringBuffer;

    move-result-object v3

    const-string v4, ": "

    invoke-virtual {v3, v4}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v3

    invoke-virtual {v1}, Ljava/lang/Exception;->getMessage()Ljava/lang/String;

    move-result-object v4

    invoke-virtual {v3, v4}, Ljava/lang/StringBuffer;->append(Ljava/lang/String;)Ljava/lang/StringBuffer;

    move-result-object v3

    invoke-virtual {v3}, Ljava/lang/StringBuffer;->toString()Ljava/lang/String;

    move-result-object v3

    invoke-direct {v2, v7, v3, v1}, Lorg/objectweb/asm/tree/analysis/AnalyzerException;-><init>(Lorg/objectweb/asm/tree/AbstractInsnNode;Ljava/lang/String;Ljava/lang/Throwable;)V

    throw v2

    :cond_2ad
    :try_start_2ad
    instance-of v1, v7, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;

    if-eqz v1, :cond_2e5

    move-object v0, v7

    check-cast v0, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;

    move-object v1, v0

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v3, v1, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->dflt:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v2, v3}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    invoke-virtual {p0, v11, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    const/4 v2, 0x0

    move v3, v2

    :goto_2c5
    iget-object v2, v1, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2}, Ljava/util/List;->size()I

    move-result v2

    if-ge v3, v2, :cond_1c8

    iget-object v2, v1, Lorg/objectweb/asm/tree/LookupSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v2

    check-cast v2, Lorg/objectweb/asm/tree/LabelNode;

    iget-object v5, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v5, v2}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    invoke-virtual {p0, v11, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    add-int/lit8 v2, v3, 0x1

    move v3, v2

    goto :goto_2c5

    :cond_2e5
    instance-of v1, v7, Lorg/objectweb/asm/tree/TableSwitchInsnNode;

    if-eqz v1, :cond_31d

    move-object v0, v7

    check-cast v0, Lorg/objectweb/asm/tree/TableSwitchInsnNode;

    move-object v1, v0

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v3, v1, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->dflt:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v2, v3}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    invoke-virtual {p0, v11, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    const/4 v2, 0x0

    move v3, v2

    :goto_2fd
    iget-object v2, v1, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2}, Ljava/util/List;->size()I

    move-result v2

    if-ge v3, v2, :cond_1c8

    iget-object v2, v1, Lorg/objectweb/asm/tree/TableSwitchInsnNode;->labels:Ljava/util/List;

    invoke-interface {v2, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v2

    check-cast v2, Lorg/objectweb/asm/tree/LabelNode;

    iget-object v5, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v5, v2}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v2

    invoke-direct {p0, v2, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    invoke-virtual {p0, v11, v2}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    add-int/lit8 v2, v3, 0x1

    move v3, v2

    goto :goto_2fd

    :cond_31d
    const/16 v1, 0xa9

    if-ne v2, v1, :cond_362

    if-nez v8, :cond_32b

    new-instance v1, Lorg/objectweb/asm/tree/analysis/AnalyzerException;

    const-string v2, "RET instruction outside of a sub routine"

    invoke-direct {v1, v7, v2}, Lorg/objectweb/asm/tree/analysis/AnalyzerException;-><init>(Lorg/objectweb/asm/tree/AbstractInsnNode;Ljava/lang/String;)V

    throw v1

    :cond_32b
    const/4 v1, 0x0

    move v9, v1

    :goto_32d
    iget-object v1, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->callers:Ljava/util/List;

    invoke-interface {v1}, Ljava/util/List;->size()I

    move-result v1

    if-ge v9, v1, :cond_1c8

    iget-object v1, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->callers:Ljava/util/List;

    invoke-interface {v1, v9}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v1

    check-cast v1, Lorg/objectweb/asm/tree/JumpInsnNode;

    iget-object v2, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    invoke-virtual {v2, v1}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v13

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    aget-object v1, v1, v13

    if-eqz v1, :cond_35e

    add-int/lit8 v2, v13, 0x1

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    aget-object v3, v1, v13

    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->subroutines:[Lorg/objectweb/asm/tree/analysis/Subroutine;

    aget-object v5, v1, v13

    iget-object v6, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->access:[Z

    move-object v1, p0

    invoke-direct/range {v1 .. v6}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;[Z)V

    add-int/lit8 v1, v13, 0x1

    invoke-virtual {p0, v11, v1}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    :cond_35e
    add-int/lit8 v1, v9, 0x1

    move v9, v1

    goto :goto_32d

    :cond_362
    const/16 v1, 0xbf

    if-eq v2, v1, :cond_1c8

    const/16 v1, 0xac

    if-lt v2, v1, :cond_36e

    const/16 v1, 0xb1

    if-le v2, v1, :cond_1c8

    :cond_36e
    if-eqz v8, :cond_396

    instance-of v1, v7, Lorg/objectweb/asm/tree/VarInsnNode;

    if-eqz v1, :cond_3a2

    move-object v0, v7

    check-cast v0, Lorg/objectweb/asm/tree/VarInsnNode;

    move-object v1, v0

    iget v1, v1, Lorg/objectweb/asm/tree/VarInsnNode;->var:I

    iget-object v3, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->access:[Z

    const/4 v5, 0x1

    aput-boolean v5, v3, v1

    const/16 v3, 0x16

    if-eq v2, v3, :cond_38f

    const/16 v3, 0x18

    if-eq v2, v3, :cond_38f

    const/16 v3, 0x37

    if-eq v2, v3, :cond_38f

    const/16 v3, 0x39

    if-ne v2, v3, :cond_396

    :cond_38f
    iget-object v2, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->access:[Z

    add-int/lit8 v1, v1, 0x1

    const/4 v3, 0x1

    aput-boolean v3, v2, v1

    :cond_396
    :goto_396
    add-int/lit8 v1, v11, 0x1

    invoke-direct {p0, v1, v4, v8}, Lorg/objectweb/asm/tree/analysis/Analyzer;->merge(ILorg/objectweb/asm/tree/analysis/Frame;Lorg/objectweb/asm/tree/analysis/Subroutine;)V

    add-int/lit8 v1, v11, 0x1

    invoke-virtual {p0, v11, v1}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowEdge(II)V

    goto/16 :goto_1c8

    :cond_3a2
    instance-of v1, v7, Lorg/objectweb/asm/tree/IincInsnNode;

    if-eqz v1, :cond_396

    move-object v0, v7

    check-cast v0, Lorg/objectweb/asm/tree/IincInsnNode;

    move-object v1, v0

    iget v1, v1, Lorg/objectweb/asm/tree/IincInsnNode;->var:I

    iget-object v2, v8, Lorg/objectweb/asm/tree/analysis/Subroutine;->access:[Z

    const/4 v3, 0x1

    aput-boolean v3, v2, v1

    goto :goto_396

    :cond_3b2
    iget-object v2, v1, Lorg/objectweb/asm/tree/TryCatchBlockNode;->type:Ljava/lang/String;

    invoke-static {v2}, Lorg/objectweb/asm/Type;->getObjectType(Ljava/lang/String;)Lorg/objectweb/asm/Type;
    :try_end_3b7
    .catch Lorg/objectweb/asm/tree/analysis/AnalyzerException; {:try_start_2ad .. :try_end_3b7} :catch_251
    .catch Ljava/lang/Exception; {:try_start_2ad .. :try_end_3b7} :catch_285

    move-result-object v2

    goto/16 :goto_1e6

    :cond_3ba
    iget-object v1, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    goto/16 :goto_11

    :cond_3be
    move v3, v1

    goto/16 :goto_167

    :cond_3c1
    const/4 v1, 0x0

    goto/16 :goto_140
.end method

.method public getFrames()[Lorg/objectweb/asm/tree/analysis/Frame;
    .registers 2

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->frames:[Lorg/objectweb/asm/tree/analysis/Frame;

    return-object v0
.end method

.method public getHandlers(I)Ljava/util/List;
    .registers 3

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->handlers:[Ljava/util/List;

    aget-object v0, v0, p1

    return-object v0
.end method

.method protected init(Ljava/lang/String;Lorg/objectweb/asm/tree/MethodNode;)V
    .registers 3
    .annotation system Ldalvik/annotation/Throws;
        value = {
            Lorg/objectweb/asm/tree/analysis/AnalyzerException;
        }
    .end annotation

    return-void
.end method

.method protected newControlFlowEdge(II)V
    .registers 3

    return-void
.end method

.method protected newControlFlowExceptionEdge(II)Z
    .registers 4

    const/4 v0, 0x1

    return v0
.end method

.method protected newControlFlowExceptionEdge(ILorg/objectweb/asm/tree/TryCatchBlockNode;)Z
    .registers 5

    iget-object v0, p0, Lorg/objectweb/asm/tree/analysis/Analyzer;->insns:Lorg/objectweb/asm/tree/InsnList;

    iget-object v1, p2, Lorg/objectweb/asm/tree/TryCatchBlockNode;->handler:Lorg/objectweb/asm/tree/LabelNode;

    invoke-virtual {v0, v1}, Lorg/objectweb/asm/tree/InsnList;->indexOf(Lorg/objectweb/asm/tree/AbstractInsnNode;)I

    move-result v0

    invoke-virtual {p0, p1, v0}, Lorg/objectweb/asm/tree/analysis/Analyzer;->newControlFlowExceptionEdge(II)Z

    move-result v0

    return v0
.end method

.method protected newFrame(II)Lorg/objectweb/asm/tree/analysis/Frame;
    .registers 4

    new-instance v0, Lorg/objectweb/asm/tree/analysis/Frame;

    invoke-direct {v0, p1, p2}, Lorg/objectweb/asm/tree/analysis/Frame;-><init>(II)V

    return-object v0
.end method

.method protected newFrame(Lorg/objectweb/asm/tree/analysis/Frame;)Lorg/objectweb/asm/tree/analysis/Frame;
    .registers 3

    new-instance v0, Lorg/objectweb/asm/tree/analysis/Frame;

    invoke-direct {v0, p1}, Lorg/objectweb/asm/tree/analysis/Frame;-><init>(Lorg/objectweb/asm/tree/analysis/Frame;)V

    return-object v0
.end method
