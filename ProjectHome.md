PForth is written in 'C' and can be easily ported to new 32 and 64-bit platforms. It only needs character input and output functions to operate and, therefore, does not require an operating system.  This makes it handy for bringing up and testing embedded systems.

PForth also works on desktops including Windows, Mac and Linux and supports command line history. This lets you develop hardware tests on a desktop before trying them on your embedded system. But pForth is not a rich and friendly desktop programming environment. There are no GUI tools for developing desktop applications. PForth is lean and mean and optimized for portability.

PForth has a tool for compiling code on a desktop, then exporting the dictionary in big or little endian format as 'C' source code. This lets you compile tests for an embedded system that does not have file I/O.

PForth is based on ANSI-Forth but is not 100% compatible.