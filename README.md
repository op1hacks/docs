# Firmware Docs for the OP-1

Documentation and research for creating custom firmware for the OP-1.

## Firmware Description

The firmware update files that TE distribute contain the full firmware needed to run the synth. The files are named something like 'op1_218.op1' and begin with a 4 byte CRC32 checksum. The rest of the file is the actual firmware compressed with LZMA. The checksum is used to verify that the entire file got transfered to the OP-1 and that it's contents haven't changed during the transfer.

    |    CRC32 (4 bytes)    |    LZMA compressed data (the rest of the file size)    |

Decompressing the LZMA data yields a TAR archive, which can be unpacked to reveal all files in the firmware.
The directory structure is shown below.

    ├── content
    │   ├── audio
    │   │   ├── drum [.raw files]
    │   │   │   └── [all drum samples for preset slots 1-8]
    │   │   ├── factory_drum [.raw files]
    │   │   │   └── [all drum samples used for factory presets]
    │   │   ├── factory_synth [.raw files]
    │   │   │   └── [all synth samples used for factory presets]
    │   │   ├── preset_drum
    │   │   │   └── [empty]
    │   │   ├── preset_synth
    │   │   │   └── [empty]
    │   │   ├── speech
    │   │   │   └── op1patch.raw [audio that's added in all non-sample .aif patch files]
    │   │   └── synth [.raw files]
    │   │       └── [synth samples for presets slots that use the sampler synth]
    │   ├── display [.svg files]
    │   │   └── [all the graphics for the UI]
    │   ├── kerntable.db [font kerning data]
    │   ├── op1.db
    │   ├── op1_factory.db [factory presets/factory reset data]
    │   └── tape.db [tape clips, loop points etc]
    ├── OP1_vdk.ldr [firmware code]
    └── te-boot.ldr [bootloader]


# Databases (specifically op1_factory.db)
TODO: Table descriptions, synth & drum table data descriptions, 16 preset limit, etc.

# Graphics (SVG)
TODO: How the svg ID's are used, how the file format should be preserved and recommended svg editors etc.

# Preset Files (AIF)
TODO: How the preset data is embedded, how to extract it, etc.

