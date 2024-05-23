# Java Architecture


### Overview of how Java Works internally
- The source code gets converted into Byte Code by Java Compiler.
- The Byte Code gets converted into machine code by the JVM.
- The the machine (os) directly runs the machine code.

```mermaid
graph TD
    A[Source Code] --> B[Java Compiler]
    B --> C[Byte Code]
    C --> D[Java Virtual Machine (JVM)]
    D --> E[Operating System (OS)]
    D --> F[Java Virtual Machine (JVM)]
```