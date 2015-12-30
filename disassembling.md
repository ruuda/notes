Disassembling
=============

To disassemble all functions in a file:

    $ objdump -Cd a.out | less

Works for ELF binaries, .so files, and raw object files.

Flags:

 * `-d`: disassemble
 * `-C`: demangle C++ ABI
