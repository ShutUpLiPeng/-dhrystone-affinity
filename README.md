# Description
Test the DMIPS info on all cpu cores.

Slightly modify the Dhrystone(by Reinhold P. Weicker) for the purpose to set thread affinity to specified cpu core;

Only support Linux and Windows now.
```
|-- README.md
|-- bin
|   |-- linux-aarch64
|   |   `-- a.out
|   `-- win64
|       `-- dhrystone.exe
|-- src
    |-- dhry.h
    |-- dhry_1.c
    `-- dhry_2.c
```

## For linux
Compile the source code in src folder.

Build cmd:
```
gcc dhry_1.c dhry_2.c -O3 -pthread -D_GNU_SOURCE
```
For linux aarch64 version, you may run a.out in bin/linux-aarch64.
## For win64
(1) You can run dhrystone.exe in bin/win64.

(2) Compile the source code in src folder for release version

Add dhry_1.c dhry_2.c dhry.h into Visual Studio project and compile for release version