# Java Architecture


### Overview of how Java Works internally
- The **Source Code** gets converted into **Byte Code** by *Java Compiler*.
- The **Byte Code** gets converted into **Machine code** by the *JVM*.

```mermaid
graph LR
    A[Source Code]
    B[Java Compiler]
    C[Byte Code]
    D[Java Virtual Machine]
    E[Operating System]
    A-->B
    B-->C
    C-->D
    D-->E
    E-->D

```

## Java Components
There are three main components of Java language: **JVM** (Java Virtual Machine), **JRE** (Java Runtime Environment), and **JDK** (Java Development Kit).

## Java Virtual Machine
The Java Virtual Machine (JVM) is an execution environment that operates independently of the platform. **It translates Java bytecode into machine code and executes it on the host operating system.**

The JVM offers a uniform runtime environment across various platforms, guaranteeing that Java applications can operate on any system equipped with a compatible JVM.

The principle of "Write Once, Run Anywhere" (WORA), a fundamental aspect of Java development, enables this cross-platform compatibility.

## JVM Architecture

```mermaid
graph TD
    subgraph G1[Class Loader]
        Loading
        Linking
        Initialization
    end
    subgraph G2[Runtime Data Area]
        A[Method Area]
        B[Heap Area]
        C[Stack Area]
        D[PC Register]
        E[Native Method Stack]
    end
    subgraph G3[Execution Engine]
        Interpreter
        X[JIT Compiler]
        Y[Garbage Collector]
    end

    JNI["Method Native Interface (JNI)"]

    NML[Native Method Library]

    G1 <--> G2
    G2 <--> G3
    G3<-->JNI
    G2<-->JNI
    NML<-->JNI
```