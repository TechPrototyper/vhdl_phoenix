# Phoenix ROMs

This directory contains the ROM files for the Phoenix arcade game (Amstar, 1981).

## Copyright Notice

These ROM files are copyrighted by Amstar and cannot be distributed.
They are included here for educational purposes only.

## Obtaining ROMs

To build the Phoenix FPGA bitstream, you need to obtain the ROM files yourself:

1. Download `phoenix.zip` from a MAME ROM set (MAME 0.37b or later)
2. Extract the contents to this directory

## Required Files

| File | Description | Size |
|------|-------------|------|
| b1-ic39.3b | Foreground tile ROM (IC39) | 2048 bytes |
| b2-ic40.4b | Foreground tile ROM (IC40) | 2048 bytes |
| ic23.3d | Background tile ROM (IC23) | 2048 bytes |
| ic24.4d | Background tile ROM (IC24) | 2048 bytes |
| ic45 | Program ROM (IC45) | 2048 bytes |
| ic46 | Program ROM (IC46) | 2048 bytes |
| ic47 | Program ROM (IC47) | 2048 bytes |
| ic48 | Program ROM (IC48) | 2048 bytes |
| h5-ic49.5a | Program ROM (IC49) | 2048 bytes |
| h6-ic50.6a | Program ROM (IC50) | 2048 bytes |
| h7-ic51.7a | Program ROM (IC51) | 2048 bytes |
| h8-ic52.8a | Program ROM (IC52) | 2048 bytes |
| mmi6301.ic40 | Palette PROM (IC40) | 256 bytes |
| mmi6301.ic41 | Palette PROM (IC41) | 256 bytes |

## Verification

Use the MAME CRC checksums to verify your ROM files:

```
b1-ic39.3b:   CRC 53413e8f
b2-ic40.4b:   CRC 0be2ba91
ic23.3d:      CRC 3c7e623f
ic24.4d:      CRC 59916d3b
ic45:         CRC 9f68086b
ic46:         CRC 273a4a82
ic47:         CRC 3d4284b9
ic48:         CRC cb5d9915
h5-ic49.5a:   CRC a105e4e7
h6-ic50.6a:   CRC ac5e9ec1
h7-ic51.7a:   CRC 2eab35b4
h8-ic52.8a:   CRC aff8e9c5
mmi6301.ic40: CRC 79350b25
mmi6301.ic41: CRC e176b768
```

## Building

Once the ROMs are in place, run:

```bash
cd proj/lattice/ulx3s
make
```

This will generate the VHDL PROM files and build the bitstream.

## License

The VHDL source code is licensed under the terms of the original repository.
The ROM files are copyrighted by Amstar and are not included in this repository.

## References

- Original game: Phoenix (Amstar, 1981)
- MAME driver: src/mame/phoenix/phoenix.cpp
- Original FPGA project: https://github.com/emard/vhdl_phoenix
- Fork with ULX3S-85F support: https://github.com/TechPrototyper/vhdl_phoenix
