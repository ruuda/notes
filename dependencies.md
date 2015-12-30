Dependencies
============

To list all transitive dependencies of an ELF executable or shared library:

    $ ldd lib.so

To list only direct dependencies:

    $ objdump -p lib.so | grep NEEDED
    $ readelf -d lib.so | grep NEEDED

Objdump flags:

 * `-p`: list private headers (includes the dynamic section)

Readelf flags:

 * `-d`: print the dynamic section
