# CSR DFU parser

_010 Editor_ utilities for parsing the CSR DFU (Device Firmware Upgrade) file format of CSR Bluetooth chips.

## Contents

* An 010 Editor template for parsing the binary structure of a CSR DFU file.
* An 010 Editor script for extracting the files from the File System area of CSR DFU files.

Note that extracted audio _.pcm_/_.raw_ files may be converted to WAV using the following command:

```sh
ffmpeg -f s16be -ar 16k -ac 1 -i example.pcm example.wav
```

## Resources

### DFU file format

* [CSR tools](https://web.archive.org/web/20120719094238/http://darkircop.org/bt/) by Andrea Bittau

* [BlueCore01 DFU File Format Specification](https://web.archive.org/web/20201020004425/https://read.pudn.com/downloads330/sourcecode/embedded/1450690/AN093.pdf)

* An incomplete [list](https://github.com/ramikg/csr-dfu-parser/discussions/1) of devices using CSR DFU

### Disassembly

After using the parser to extract the firmware's text section from the DFU's Stack Software area, you may disassemble it using one of the following disassemblers:

* Radare2's XAP disassembler, also by Andrea Bittau

* IDA, using [this](https://github.com/comex/xap) processor module
