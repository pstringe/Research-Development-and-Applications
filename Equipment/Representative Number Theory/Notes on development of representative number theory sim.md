---
creation date:		2023-08-18 20:22
modification date:	2023-08-18 20:22
title: 				Notes on development of representative number theory sim
tags:
---
```C
#include "foundation.h"
#include <stdio.h>

int main (int argc, char **argv) {
    char    *num;
    int     i;
    int     base;
    int     digit;
    int     n = 0;

    if (argc < 2){
        return 0;
    }
    
    num = argv[1];
    base = f_strlen(num) * 10;
    i = 0;
    while (base && *(num + i)) {
        digit = (int)(num[i] - 48);
        f_putnbr(digit);

        n += base * digit;
        base /= 10;
        i++;
    }

    f_putnbr(n);
    return (0);
}
```

TRACE
TEST : -1 : Input : 10 : Expected : 10 : Actual : 20
PROP : 0.0 : (num == undefined)
PROP : 0.1 : (i == undefined)
PROP : 0.2 : (base == undefined)
PROP : 0.3 : (digit == undefined)
PROP : 0.4 : (n == 0)                [instanciaiton]
PROP : 0.5 : (argc == 2)            [There should be two args on cmd]
PROP : 0.6 : (num = argv[1])
PROP : 0.6 : (a = f_strlen(num)) 
PROP : 0.7 : (a = f_strlen('10')) [-1 : Input]
PROP : 0.8 : (a = 2)                 [0.7]
PROP : 0.9 : (base = (a * 10)).   [0.8]
NOTE : In the future implement a rule similar to detatchment from prop calc for lines of code that involve operators
PROP : 1.0 : (base = 20)            [0.9]
NOTE : Instead of multiplying the 10 by the length of the string, a; We ought to multiply 10 by itself, a times. 
NOTE : We've made the following change:

```C
	base = 1;
    i = f_strlen(num);

    while (i--) {
        base *= 10;
    } 
```

TEST : -1 : Input : 10 : Expected : 10 : Actual : 10100
PROP : 0.0 : (num == undefined)
PROP : 0.1 : (i == undefined)
PROP : 0.2 : (base == undefined)
PROP : 0.3 : (digit == undefined)
PROP : 0.4 : (n == 0) : [instanciaiton]
PROP : 0.5 : (argc == 2) : [There should be two args on cmd]
PROP : 0.6 : (num = argv[1])
PROP : 0.6 : (a = f_strlen(num))
PROP : 0.7 : (a = f_strlen('10')) : [-1 : Input]
PROP : 0.8 : (a = 2) : [0.7]
PROP : 0.9 : (base = 1) 
PROP : 1.0 : (i = f_strlen(num))
PROP : 1.1 : (i = 2) : [-1, 1]
PROP : 1.2 : (base = 10) : `base *= 10` : [0.9]
PROP : 1.3 : (i = i - 1) : `while (i--){`
PROP : 1.4 : (i = 1) [1.1, 1.3]
PROP : 1.5 : (base = 10 * 10) [19]
PROP : 1.6 : (base = 100) [1.4]
PROP : 1.7 : (i = i - 1) : `while (i--){`
PROP : 1.8 : (i = 0) [1.7, 1.4]
PROP : 1.9 : (base ^ ("10")[i]) : `while (base && *(num + i)) {`
PROP : 2.0 : (base ^ ("10")[0]) 
PROP : 2.1 : (base ^ ('1'))
PROP : 2.2 : ((100 ^ ('1'))
PROP : 2.3 : (digit = (num[i] - 48)) 
PROP : 2.4 : (digit = ('1' - 48)) 
PROP : 2.5 : (digit = 1) : `see man ascii` : [2.3, 2.4]
NOTE : Comming up on a print statement, I think out failed test may ust be stray chars being printed. Cleaning up and re-testing. 
NOTE : We've made the changes. There is one stray zero, we will identify and fix
PROP : 2.5.1 : (n = n +  base * digit)
PROP : 2.5.2 : (n = 100 )
PROP : 2.6 : (base = base / 10)
PROP : 2.7 : (base = 100 / 10) : [1.6]
PROP : 2.8 : (base = 10) : [2.7]
PROP : 2.9 : (i = i + 1)
PROP : 3.0 : (i = 0 + 1)
PROP : 3.1 :  1
PROP : 1.9 : (base ^ ("10")[i]) : `while (base && *(num + i)) {`
PROP : 2.0 : (base ^ ("10")[1]) 
PROP : 2.1 : (base ^ ('0'))
PROP : 2.2 : ((100 ^ ('0'))
PROP : 2.3 : (digit = (num[1] - 48)) 
PROP : 2.4 : (digit = ('0' - 48)) 
PROP : 2.5 : (digit = 0) : `see man ascii` : [2.3, 2.4]
PROP : 2.6 : (n = (n +  base * digit))
PROP : 2.6 : (n = (100 +  10 * 0))
PROP : 2.7 : (n = 100)
NOTE : 2.8 :  ought to be (n = 10) not (n = 100)
NOTE : 2.8 :  when building up the base, we itterate 1 too many times. We can fix this with minimal effort by switching from post-incrementation to pre-incrementation.

[[2023-08-22]]
PROP : 3.0 : We have a function intended to succeed an expression in [[Representative Number Theory]]
PROP : 3.1 : We have an undeclared identifier, digit
TEST : 3.2 : Input : p 10 : Expected : m(p) : Actual : m(
PROP : 3.3 : We allocate a string for dst, the length of the src + 3 (4)
PROP : 3.4 : We set the first index to 'm', the second to '('

---
PROP : TEST : 3.2 : Input : p 10 : Expected : m(p) : Actual : m( 
Prop : Test : 3.3 : Input : p 10 : 

PROP : 3.5 : When we run the debug command and set a breakpoint to main we expect the interface to point to our file. 

Instead we see the following:
```
Breakpoint 1: where = main`main + 22 at main.c:86:14, address = 0x0000000100003c36
```

```
rm -f  ./src/main.o
rm -f *.o
gcc -Wall -Werror -Wextra -I./includes/foundation/ -g -g -c src/main.c -o src/main.o
gcc  ./src/main.o -L./includes/foundation/ -lfoundation -o main
ld: library not found for -lfoundation
clang: error: linker command failed with exit code 1 (use -v to see invocation)
make: *** [main] Error 1
```

OBSD : 3.5 : In the makefile, we've added a debug rule.  

PROP : 3.6 : R : P does not recall how the debug rule in the make file affects execution of the command

PROP : 3.7 : R : P does not remember the High-Level function of a linker

PROP : 3.8 : A : If P remembers the high-level function of a linker and how debug-able executables are compiled, P will fix the current bug.

IMP : 3.9 : P : SBE : P describes the high-level function of a linker 

IMP : 4.0 : P : SBE : P describes the procedure for compiling debuggable executables

IMP : 4.1 : P : NOTE : The linker is responsible for linking object files by resolving symbolic addresses. 

IMP : 4.1.1 : P : NOTE : The linker stores "load addresses, used to resolve symbols.

PROP : 4.1.0 : P : NOTE : To compile debuggable executables, the user adds the -g flag to the compilation command. 

NOTE : 4.1.1 : P : 
```
rm -f  ./src/main.o
rm -f *.o
gcc -Wall -Werror -Wextra -I./includes/foundation/ -g -v -g -v -c src/main.c -o src/main.o
Apple clang version 12.0.0 (clang-1200.0.32.29)
Target: x86_64-apple-darwin21.6.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
 "/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/clang" -cc1 -triple x86_64-apple-macosx11.1.0 -Wdeprecated-objc-isa-usage -Werror=deprecated-objc-isa-usage -Werror=implicit-function-declaration -emit-obj -mrelax-all -disable-free -disable-llvm-verifier -discard-value-names -main-file-name main.c -mrelocation-model pic -pic-level 2 -mthread-model posix -mframe-pointer=all -fno-strict-return -masm-verbose -munwind-tables -target-sdk-version=11.1 -target-cpu penryn -dwarf-column-info -debug-info-kind=standalone -dwarf-version=4 -debugger-tuning=lldb -target-linker-version 609.8 -v -v -resource-dir /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/clang/12.0.0 -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk -I ./includes/foundation/ -I/usr/local/include -internal-isystem /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/usr/local/include -internal-isystem /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/clang/12.0.0/include -internal-externc-isystem /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/usr/include -internal-externc-isystem /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/include -Wall -Werror -Wextra -Wno-reorder-init-list -Wno-implicit-int-float-conversion -Wno-c99-designator -Wno-final-dtor-non-final-class -Wno-extra-semi-stmt -Wno-misleading-indentation -Wno-quoted-include-in-framework-header -Wno-implicit-fallthrough -Wno-enum-enum-conversion -Wno-enum-float-conversion -fdebug-compilation-dir /Users/poitier/Documents/Projects/development/representative_number_theory_sim -ferror-limit 19 -fmessage-length 51 -stack-protector 1 -fstack-check -mdarwin-stkchk-strong-link -fblocks -fencode-extended-block-signature -fregister-global-dtors-with-atexit -fgnuc-version=4.2.1 -fobjc-runtime=macosx-11.1.0 -fmax-type-align=16 -fdiagnostics-show-option -fcolor-diagnostics -o src/main.o -x c src/main.c
clang -cc1 version 12.0.0 (clang-1200.0.32.29) default target x86_64-apple-darwin21.6.0
ignoring nonexistent directory "/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/usr/local/include"
ignoring nonexistent directory "/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/Library/Frameworks"
#include "..." search starts here:
#include <...> search starts here:
 ./includes/foundation
 /usr/local/include
 /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/clang/12.0.0/include
 /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/usr/include
 /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/include
 /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks (framework directory)
End of search list.
gcc  ./src/main.o -L./includes/foundation/ -lfoundation -o main
ld: library not found for -lfoundation
clang: error: linker command failed with exit code 1 (use -v to see invocation)
make: *** [main] Error 1
```

NOTE : 4.1.2 : According to the invocation, the foundation library is not found
*Resources*

NOTE : 42
https://riptutorial.com/c/example/4360/the-linkerhttps://riptutorial.com/c/example/4360/the-linker




---
[1]:: [[Notes on development of representative number theory sim]]