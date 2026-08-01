.class public abstract Lorg/objectweb/asm/tree/AbstractInsnNode;
.super Ljava/lang/Object;


# static fields
.field public static final FIELD_INSN:I = 0x4

.field public static final FRAME:I = 0xe

.field public static final IINC_INSN:I = 0xa

.field public static final INSN:I = 0x0

.field public static final INT_INSN:I = 0x1

.field public static final INVOKE_DYNAMIC_INSN:I = 0x6

.field public static final JUMP_INSN:I = 0x7

.field public static final LABEL:I = 0x8

.field public static final LDC_INSN:I = 0x9

.field public static final LINE:I = 0xf

.field public static final LOOKUPSWITCH_INSN:I = 0xc

.field public static final METHOD_INSN:I = 0x5

.field public static final MULTIANEWARRAY_INSN:I = 0xd

.field public static final TABLESWITCH_INSN:I = 0xb

.field public static final TYPE_INSN:I = 0x3

.field public static final VAR_INSN:I = 0x2


# instance fields
.field index:I

.field public invisibleTypeAnnotations:Ljava/util/List;

.field next:Lorg/objectweb/asm/tree/AbstractInsnNode;

.field protected opcode:I

.field prev:Lorg/objectweb/asm/tree/AbstractInsnNode;

.field public visibleTypeAnnotations:Ljava/util/List;


# direct methods
.method protected constructor <init>(I)V
    .registers 3

    invoke-direct {p0}, Ljava/lang/Object;-><init>()V

    iput p1, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->opcode:I

    const/4 v0, -0x1

    iput v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->index:I

    return-void
.end method

.method static clone(Lorg/objectweb/asm/tree/LabelNode;Ljava/util/Map;)Lorg/objectweb/asm/tree/LabelNode;
    .registers 3

    invoke-interface {p1, p0}, Ljava/util/Map;->get(Ljava/lang/Object;)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/LabelNode;

    return-object v0
.end method

.method static clone(Ljava/util/List;Ljava/util/Map;)[Lorg/objectweb/asm/tree/LabelNode;
    .registers 5

    invoke-interface {p0}, Ljava/util/List;->size()I

    move-result v0

    new-array v2, v0, [Lorg/objectweb/asm/tree/LabelNode;

    const/4 v0, 0x0

    move v1, v0

    :goto_8
    array-length v0, v2

    if-ge v1, v0, :cond_1b

    invoke-interface {p0, v1}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    invoke-interface {p1, v0}, Ljava/util/Map;->get(Ljava/lang/Object;)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/LabelNode;

    aput-object v0, v2, v1

    add-int/lit8 v0, v1, 0x1

    move v1, v0

    goto :goto_8

    :cond_1b
    return-object v2
.end method


# virtual methods
.method public abstract accept(Lorg/objectweb/asm/MethodVisitor;)V
.end method

.method protected final acceptAnnotations(Lorg/objectweb/asm/MethodVisitor;)V
    .registers 10

    const/4 v2, 0x0

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    if-nez v0, :cond_23

    move v1, v2

    :goto_6
    move v3, v2

    :goto_7
    if-ge v3, v1, :cond_2b

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    iget v4, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typeRef:I

    iget-object v5, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typePath:Lorg/objectweb/asm/TypePath;

    iget-object v6, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->desc:Ljava/lang/String;

    const/4 v7, 0x1

    invoke-virtual {p1, v4, v5, v6, v7}, Lorg/objectweb/asm/MethodVisitor;->visitInsnAnnotation(ILorg/objectweb/asm/TypePath;Ljava/lang/String;Z)Lorg/objectweb/asm/AnnotationVisitor;

    move-result-object v4

    invoke-virtual {v0, v4}, Lorg/objectweb/asm/tree/TypeAnnotationNode;->accept(Lorg/objectweb/asm/AnnotationVisitor;)V

    add-int/lit8 v0, v3, 0x1

    move v3, v0

    goto :goto_7

    :cond_23
    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    move v1, v0

    goto :goto_6

    :cond_2b
    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    if-nez v0, :cond_4c

    move v1, v2

    :goto_30
    move v3, v2

    :goto_31
    if-ge v3, v1, :cond_54

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v3}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    iget v4, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typeRef:I

    iget-object v5, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typePath:Lorg/objectweb/asm/TypePath;

    iget-object v6, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->desc:Ljava/lang/String;

    invoke-virtual {p1, v4, v5, v6, v2}, Lorg/objectweb/asm/MethodVisitor;->visitInsnAnnotation(ILorg/objectweb/asm/TypePath;Ljava/lang/String;Z)Lorg/objectweb/asm/AnnotationVisitor;

    move-result-object v4

    invoke-virtual {v0, v4}, Lorg/objectweb/asm/tree/TypeAnnotationNode;->accept(Lorg/objectweb/asm/AnnotationVisitor;)V

    add-int/lit8 v0, v3, 0x1

    move v3, v0

    goto :goto_31

    :cond_4c
    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    move v1, v0

    goto :goto_30

    :cond_54
    return-void
.end method

.method public abstract clone(Ljava/util/Map;)Lorg/objectweb/asm/tree/AbstractInsnNode;
.end method

.method protected final cloneAnnotations(Lorg/objectweb/asm/tree/AbstractInsnNode;)Lorg/objectweb/asm/tree/AbstractInsnNode;
    .registers 9

    const/4 v2, 0x0

    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    if-eqz v0, :cond_34

    new-instance v0, Ljava/util/ArrayList;

    invoke-direct {v0}, Ljava/util/ArrayList;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    move v1, v2

    :goto_d
    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    if-ge v1, v0, :cond_34

    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v1}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    new-instance v3, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    iget v4, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typeRef:I

    iget-object v5, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typePath:Lorg/objectweb/asm/TypePath;

    iget-object v6, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->desc:Ljava/lang/String;

    invoke-direct {v3, v4, v5, v6}, Lorg/objectweb/asm/tree/TypeAnnotationNode;-><init>(ILorg/objectweb/asm/TypePath;Ljava/lang/String;)V

    invoke-virtual {v0, v3}, Lorg/objectweb/asm/tree/TypeAnnotationNode;->accept(Lorg/objectweb/asm/AnnotationVisitor;)V

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->visibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v3}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    add-int/lit8 v0, v1, 0x1

    move v1, v0

    goto :goto_d

    :cond_34
    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    if-eqz v0, :cond_65

    new-instance v0, Ljava/util/ArrayList;

    invoke-direct {v0}, Ljava/util/ArrayList;-><init>()V

    iput-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    :goto_3f
    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0}, Ljava/util/List;->size()I

    move-result v0

    if-ge v2, v0, :cond_65

    iget-object v0, p1, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v2}, Ljava/util/List;->get(I)Ljava/lang/Object;

    move-result-object v0

    check-cast v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    new-instance v1, Lorg/objectweb/asm/tree/TypeAnnotationNode;

    iget v3, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typeRef:I

    iget-object v4, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->typePath:Lorg/objectweb/asm/TypePath;

    iget-object v5, v0, Lorg/objectweb/asm/tree/TypeAnnotationNode;->desc:Ljava/lang/String;

    invoke-direct {v1, v3, v4, v5}, Lorg/objectweb/asm/tree/TypeAnnotationNode;-><init>(ILorg/objectweb/asm/TypePath;Ljava/lang/String;)V

    invoke-virtual {v0, v1}, Lorg/objectweb/asm/tree/TypeAnnotationNode;->accept(Lorg/objectweb/asm/AnnotationVisitor;)V

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->invisibleTypeAnnotations:Ljava/util/List;

    invoke-interface {v0, v1}, Ljava/util/List;->add(Ljava/lang/Object;)Z

    add-int/lit8 v2, v2, 0x1

    goto :goto_3f

    :cond_65
    return-object p0
.end method

.method public getNext()Lorg/objectweb/asm/tree/AbstractInsnNode;
    .registers 2

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->next:Lorg/objectweb/asm/tree/AbstractInsnNode;

    return-object v0
.end method

.method public getOpcode()I
    .registers 2

    iget v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->opcode:I

    return v0
.end method

.method public getPrevious()Lorg/objectweb/asm/tree/AbstractInsnNode;
    .registers 2

    iget-object v0, p0, Lorg/objectweb/asm/tree/AbstractInsnNode;->prev:Lorg/objectweb/asm/tree/AbstractInsnNode;

    return-object v0
.end method

.method public abstract getType()I
.end method
