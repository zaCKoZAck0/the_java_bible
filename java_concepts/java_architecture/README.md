# Java Architecture


### Overview of how Java Works internally
- The source code gets converted into Byte Code by Java Compiler.
- The Byte Code gets converted into machine code by the JVM.
- Then the machine (os) directly runs the machine code.

```mermaid
graph TD
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
There are three main components of Java language: JVM (Java Virtual Machine), JRE (Java Runtime E), and JDK.
