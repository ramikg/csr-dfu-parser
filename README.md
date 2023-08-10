# CSR DFU parser

An _010 Editor_ template for parsing the CSR DFU (Device Firmware Upgrade) file format for CSR's Bluetooth chips.

The parser was tested on version 2.3 of the format, and so  may require adjustments for other versions.

## Resources

### DFU file format

* [CSR tools](https://web.archive.org/web/20120719094238/http://darkircop.org/bt/) by Andrea Bittau

* [BlueCore01 DFU File Format Specification](https://web.archive.org/web/20201020004425/https://read.pudn.com/downloads330/sourcecode/embedded/1450690/AN093.pdf)

### Disassembly

After using the parser to extract the firmware's text section from the DFU's Stack Software area, you may disassemble it using one of the following disassemblers:

* Radare2's XAP disassembler, also written by Andrea Bittau

* IDA, using [this](https://github.com/comex/xap) processor module
