# LG SPN5B-W Firmware

This repository contains firmware dumps from the LG SPN5B-W subwoofer. Specifically, these firmware dumps were read
from the EEPROM chip of the LG EBR89625801 PCB.

The firmware was read, and subsequently written, using a CH341A programmer (~US$10).

## WARNING

**Replacing the EEPROM on your board requires desoldering, and then soldering a surface mount IC. When working with
components this small, it is very easy to ruin your board entirely.**

**Proceed at your own risk!**

[Disclaimer](#disclaimer)

## Motivation

If your subwoofer is showing indications of being powered on, but will no longer pair to your soundbar, then your
EEPROM may be bad.

A symptom of a bad EEPROM is the green light on the back of your subwoofer constantly blinking, and the subwoofer never
pairing to the soundbar.

**Before attempting an EEPROM replacement, try factory resetting both the soundbar and subwoofer.**

![Blinking Green Light](https://user-images.githubusercontent.com/122238863/211229850-097c9f59-0e2e-41ed-9161-308cbdfa7fc6.gif)

## ROM's

#### `roms/spn5b-w.bin`

This firmware was read from a newer revision board purchased directly from LG Parts. You can identify a newer revision
board via two copper coils near the power input.

**This firmware has been tested with a replacement EEPROM chip on both new and old revision boards.**

<img width="487" alt="New Revision" src="https://user-images.githubusercontent.com/122238863/211227778-1ddf5473-4a3c-4a39-8b77-e67c44fded9f.png">

#### `roms/spn5b-w.bin.old`

This firmware was read from an older revision board from a working subwoofer. You can identify an older revision board
via one copper coil near the power input.

**This firware has not been tested on replacement EEPROM chips.**

## Parts

You can purchase replacement EEPROM chips online relatively cheap (~US$0.50). The chip used during this specific repair
was the [Macronix MX25V8035F](https://media.digikey.com/pdf/Data%20Sheets/Macronix/MX25V8035F.pdf).

**Reference the part number of the chip on your specific board before purchasing a replacement chip.**

## flashrom

There are many ways to interface with a CH341A programmer, depending on your OS. In my specific instance, macOS and
`flashrom` were used.

The specific chip (Macronix MX25V8035F) used for this repair required a modified `flashrom` in order to be
read/written. These modifications are published at 
[https://github.com/engagefactoryreset/flashrom-macos](https://github.com/engagefactoryreset/flashrom-macos).

## LG Replacement Board

For reference, the board in the SPN5B-W subwoofer can be found at 
[https://lgparts.com/products/ebr89625801](https://lgparts.com/products/ebr89625801).

## Disclaimer

The information in this repository is provided "as is" without warranty of any kind, either express or implied.

**Use at your own risk.**

The use of this information is done at your own discretion and risk and with agreement that you will be solely
responsible for any damage to your hardware or loss of data that results from such activities. You are solely
responsible for the use of this information, and we will not be liable for any damages that you may suffer in
connection with using, modifying or distributing any of this information. 

No advice or information, whether oral or written, obtained by you from us or from this repository shall create any
warranty for the information.

We make no warranty that:
* The information will meet your requirements
* The information will be uninterrupted, timely, secure or error-free
* The results that may be obtained from the use of the information will be effective, accurate or reliable
* The quality of the information will meet your expectations
* Any errors in the information obtained from us will be corrected. 
