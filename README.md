
# Firmware Docs for the OP-1

     _______________________________________________________________________________________________________________
    |   _____________________________________________________________________________________________________       |
    |  |           |           |                       |           |           |           |           |     |  ::  |
    |  |   ·····   | (_)       |                       |    ___    |    ___    |    ___    |    ___    |  /  |      |
    |  |  ·······  |___________|                       |   |   |   |   |   |   |   |   |   |   |   |   |_____|      |
    |  |  ·······  |     |     |                       |   |___|   |   |___|   |   |___|   |   |___|   |     |      |
    |  |   ·····   |     |     |                       |           |           |           |           |  O  |      |
    |  |___________|_____|_____|_______________________|___________|___________|___________|___________|_____|      |
    |  |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |   .  |
    |  |     |  Ϙ  | ◯_◯ | ||| |  1  |  2  |  3  |  4  |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  | .:..|   :  |
    |  |_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|   :  |
    |  |     |     |     |        |     |        |        |        |        |     |        |        |        |      |
    |  |  ↥  |  ↓  |  >8 |     O  |  O  |  O     |     O  |  O     |     O  |  O  |  O     |     O  |  O     |      |
    |  |_____|_____|_____|________|_____|________|________|________|________|_____|________|________|________|      |
    |  |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |      |
    |  |  ◉  |  ▶  |  ■  |     |     |     |     |     |     |     |     |     |     |     |     |     |     |      |
    |  |_____|_____|_____|     |     |     |     |     |     |     |     |     |     |     |     |     |     |      |
    |  |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |      |
    |  |  ‹  |  ›  |Shift|     |     |     |     |     |     |     |     |     |     |     |     |     |     |      |
    |  |_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|_____|      |
    |_______________________________________________________________________________________________________________|


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

## Encryption of OP1_vdk.ldr
The code blocks of OP1_vdk.ldr are encrypted using the [XTEA algortihm](https://en.wikipedia.org/wiki/XTEA).
In each block of 24 bytes the first 8 bytes are encrypted and the following 16 bytes are unencrypted.
The key is read from the blackfin OTP memory page 0xd0.

# Databases (specifically op1_factory.db)
TODO: Table descriptions, synth & drum table data descriptions, 16 preset limit, etc.

*Notes:*

- The `folder` column in `synth_presets` is actually an arbitrary string, not the synth engine name. This means we could have custom folders that contain any types of synths.

# Graphics (SVG)
TODO: How the svg ID's are used, how the file format should be preserved and recommended svg editors etc.

## Font & Symbols

The OP-1 font is defined in the `opfont.svg` file. It defines the basic alphabet only in upper case and also contains additional UI symbols.
Each character or symbol in the SVG file is mapped to a character by the `id` attribute. For example, the symbol for letter `A` has an `id` of `a`.
During rendering the spacing between characters is determined by the `kerntable.db` database file.

- All alphabetic characters are upper case, but are refered to with a lower case `id`.
- Various UI symbols are refered to with an upper case letter. E.g. the drum symbol has id `D`.
- Special characters that can't validly be used as an id, are instead referenced in a special hex notation. E.g the id for < is `_x3C_`.
- Custom symbols can be added as long as all symbols have unique ids.

*Special symbols:*

- D: Drum icon
- Q: Sequencer icon
- X: FX icon (blue)
- A: Envelope icon (blue)
- L: LFO icon (blue)
- H: FX icon (green)
- E: Envelope icon (green)
- F: LFO icon (green)
- S: Synth icon (blue)
- T: Tape icon (red)
- M: Mixer icon (gray)
- Y: Musical keyboard icon (blue)
- I: FX blend icon (blue)
- J: Blend icon without `FX` text, only the overlapping circles (blue)
- Z: EQ icon (blue)

# Preset Files (AIF)
TODO: How the preset data is embedded, how to extract it, etc.

