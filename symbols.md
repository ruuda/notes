Symbols
=======

To list the defined and undefined symbols in an .so:

    $ objdump -CT lib.so

Flags:

 * `-C`: demangle C++ ABI
 * `-T`: print dynamic symbol table
 * `-t`: print regular symbol table (try readelf if it was stripped)

Alternatives:

    $ readelf -Ws lib.so | c++filt
    $ nm -C lib.so

Readelf flags:

 * `-W`: do not discard output after 80 columns
 * `-s`: list all symbols
 * `--dyn-syms`: list dynamic symbols only

Nm flags:

 * `-C`: demangle C++ ABI
 * `-D`: print dynamic symbol table instead of regular symbol table
