# The Neotron Project

This is the Github organisation for the Neotron Project. Neotron is a family of 1980's style home computers, powered by ARM Cortex-M processors, with a ROM written in Rust, and a fully open-source design.

## Components

### Neotron BIOS

The Neotron BIOS is a similar concept to the IBM PC BIOS, or the BIOS used on CP/M systems. It boots the system and provides hardware abstraction.

### Neotron OS

The Neotron OS runs on all Neotron machines. It expects to access RAM starting at `0x2000_0000`, and gets all other information about the system from the BIOS.

### Neotron Shell

The Neotron Shell is a cross between `COMMAND.COM` on MS-DOS, and the BASIC interpreter you get on something like a Commodore 64 or ZX Spectrum.

### Neotron Applications

The Neotron Shell can ask the OS to load an application, which will then run. A well-behaved application should run on any system running the Neotron OS, provided it has enough RAM available. You can also get (perfectly valid) badly-behaved applications which reach out and touch the hardware directly - like MS-DOS, there's no memory protection here!

## Developers

* [thejpster](https://github.com/thejpster)
* [segfault](https://github.com/IGBC)

## General Project Repos

* *The Neotron Book* ([Github](https://github.com/neotron-compute/neotron-book)) ([Rendered](https://neotron-compute.github.io/Neotron-Book/))
   - Our book covering the Neotron Project, the ideas behind it, and introducing the important concepts
* *Neotron OS* ([Github](https://github.com/neotron-compute/neotron-os))
   - The Neotron OS runs on any computer with a Neotron BIOS implementation
* *Neotron Common BIOS* ([Github](https://github.com/neotron-compute/neotron-common-bios))
   - Code and API shared between the Neotron OS and every Neotron BIOS implementation
* *Neotron BMC* ([Github](https://github.com/neotron-compute/neotron-bmc))
   - Firmware for the Board Management Controller (BMC) fitted to various Neotron computers 
* *Neotron SDK* ([Github](https://github.com/Neotron-Compute/Neotron-SDK))
  - Software Development Kit for writing applications that run on Neotron OS
* *Neotron API* ([Github](https://github.com/Neotron-Compute/Neotron-API))
  - The low-level API shared by the Neotron OS and the Neotron SDK
* *Neotron FFI* ([Github](https://github.com/neotron-compute/neotron-ffi))
   - FFI safe types used by Neotron Common BIOS and Neotron API
* *Neotron Common Hardware* ([Github](https://github.com/neotron-compute/neotron-common-hardware))
  - KiCAD Schematics, Footprints and Symbols shared between different Neotron computer designs
* *Neotron Expansion Template* ([Github](https://github.com/Neotron-Compute/Neotron-Expansion-Template))
  - Template Design for an Expansion Card that will fit in a Neotron Pico and other computers with a Neotron Bus

## Neotron Computers

### Neotron Pico

A microATX form-factor computer powered by the Raspberry Pi Pico (or rather its RP2040 Microcontroller)

* *Neotron Pico* ([Github](https://github.com/neotron-compute/neotron-pico))
   - Schematics and PCB designs for the Neotron Pico
* *Neotron Pico BIOS* ([Github](https://github.com/neotron-compute/neotron-pico-bios))
   - A Neotron BIOS for the Neotron Pico

### Neotron Desktop

A Neotron BIOS that runs as a GUI application on Linux, macOS and Windows, and can run a natively compiled version of Neotron OS in a window. Unfortunately, because Neotron OS is compiled for your host machine, you cannot execute Neotron applications in this build - for perfectly understandable reasons, modern OSes have security restrictions that stop you load some data from disk and blindly executing it.

* *Neotron Desktop BIOS* ([Github](https://github.com/neotron-compute/neotron-desktop-bios))

### Neotron QEMU

A Neotron BIOS that runs inside the QEMU ARM system emulator, using QEMU's serial emulation as the console instead of video output. QEMU should be configured to emulate the Arm MPS3-AN547, which is their FPGA based Cortex-M55 developer kit.

* *Neotron QEMU BIOS* ([Github](https://github.com/neotron-compute/neotron-qemu-bios))

### Neotron 32

A small form-factor computer powered by an Texas Instruments Tiva-C Launchpad. No longer updated.

* *Neotron 32* ([Github](https://github.com/neotron-compute/neotron-32-hardware))
   - Schematics and PCB designs for the Neotron 32
* *Neotron 32 BIOS* ([Github](https://github.com/neotron-compute/neotron-32-bios))
   - A Neotron BIOS for the Neotron 32
