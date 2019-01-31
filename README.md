```
mkdir out
gn gen out/Default
ninja -C out/Default
```

The above will return the following error

```
ninja: Entering directory `out'
[2/5] CXX obj/core/core/main.o
FAILED: obj/core/core/main.o 
clang++ -MMD -MF obj/core/core/main.o.d -D_DEBUG  -fno-strict-aliasing -funwind-tables -fPIC -pipe -fcolor-diagnostics -fdebug-prefix-map=/home/putin/Projects/4004emu=. -m64 -march=x86-64 -fstack-protector-strong -pthread -O0 -fno-omit-frame-pointer -g2 -fvisibility=hidden -fvisibility-inlines-hidden -Wno-undefined-bool-conversion -Wno-tautological-undefined-compare -std=c++11 -frtti -fexceptions -c ../core/main.cc -o obj/core/core/main.o
../core/main.cc:2:10: fatal error: 'cpu.hpp' file not found
#include <cpu.hpp>
         ^~~~~~~~~
1 error generated.
[3/5] AR obj/cpu/libcpu.a
ninja: build stopped: subcommand failed.
```
