# Back Engineering Labs Fork

This is a fork of testfloat with softfloat added into the source base. 
This will only compile if you have MSVC or LLVM-MSVC. 
The reason for this repo is to build individual PE files for each float test. 
This way we can compare the execution before and after applying obfuscation. 
The binaries generated will be used in CI so that everytime we push changes to passes we can see if we broke anything.


Only a small subset of all of the testfloat tests are used. Pre-compiled binaries along with their PDB's can be found in this repos releases. Both 32bit and 64bit modules are uploaded.

### How to build

Build 64bit

```
cmake -B .build
cd .build
cmake --build . --config Release
```

Build 32bit

```
cmake -B .build -DCMAKE_GENERATOR_PLATFORM=WIN32
cd .build
cmake --build . --config Release
```