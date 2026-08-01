.class public Lcom/github/megatronking/stringfog/plugin/utils/Log;
.super Ljava/lang/Object;


# static fields
.field private static isDebug:Z


# direct methods
.method public constructor <init>()V
    .registers 1

    invoke-direct {p0}, Ljava/lang/Object;-><init>()V

    return-void
.end method

.method public static e(Ljava/lang/String;)V
    .registers 2
    .annotation system Ldalvik/annotation/Signature;
        value = {
            "(",
            "Ljava/lang/String;",
            ")V"
        }
    .end annotation

    sget-boolean v0, Lcom/github/megatronking/stringfog/plugin/utils/Log;->isDebug:Z

    if-eqz v0, :cond_9

    sget-object v0, Ljava/lang/System;->err:Ljava/io/PrintStream;

    invoke-virtual {v0, p0}, Ljava/io/PrintStream;->println(Ljava/lang/String;)V

    :cond_9
    return-void
.end method

.method public static setDebug(Z)V
    .registers 1
    .annotation system Ldalvik/annotation/Signature;
        value = {
            "(Z)V"
        }
    .end annotation

    sput-boolean p0, Lcom/github/megatronking/stringfog/plugin/utils/Log;->isDebug:Z

    return-void
.end method

.method public static v(Ljava/lang/String;)V
    .registers 2
    .annotation system Ldalvik/annotation/Signature;
        value = {
            "(",
            "Ljava/lang/String;",
            ")V"
        }
    .end annotation

    sget-boolean v0, Lcom/github/megatronking/stringfog/plugin/utils/Log;->isDebug:Z

    if-eqz v0, :cond_9

    sget-object v0, Ljava/lang/System;->out:Ljava/io/PrintStream;

    invoke-virtual {v0, p0}, Ljava/io/PrintStream;->println(Ljava/lang/String;)V

    :cond_9
    return-void
.end method
