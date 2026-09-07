# Extracting the Firmware from SPI

While attempting to extract the firmware, I ran into some issues that hopefully you can avoid.

A simple chip clip and CH341a programmer was unable to interact with the flash in any meaningful way. This was likely due to the way the chip's power rail is set up. This means that soldering the chip off the board is the next reasonable step towards firmware extraction.

Using a SOP8 to DIP8 chip adapter, we can completely isolate the chip and pull the firmware off with `IMSProg`

<img width="3072" height="4080" alt="SPI Adapter" src="https://github.com/user-attachments/assets/3f8a025c-22a6-4884-a97f-ab67cd014e1d" />

**IMSProg Settings**

