# edc2svd
Convert an MCU register description from the EDC format to the SVD format

This program can be used to generate Peripheral Access Crates to be used in
Rust programs.

First, an EDC file is converted with this tool to an SVD file. Then [`svd2rust`]
can be used to generate the Peripheral Access Crate, e.g. as follows:

    edc2svd input.edc output.svd
    svd2rust --target none -i output.svd

[`svd2rust`]: https://crates.io/crates/svd2rust