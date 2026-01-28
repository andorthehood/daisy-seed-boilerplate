# daisy-seed-boilerplate

This repository provides a simple starting point for hardware DSP projects using the Daisy Seed platform.

It includes a minimal example firmware that bypasses the audio input directly to the output, and the Daisy library needed to build and run your projects.

## Prerequisites

The Daisy toolchain must be installed to build and program the Daisy Seed. Follow the appropriate guide for your operating system:

- [macOS Toolchain](https://daisy.audio/tutorials/toolchain-mac/)
- [Windows Toolchain](https://daisy.audio/tutorials/toolchain-windows/)
- [Linux Toolchain](https://daisy.audio/tutorials/toolchain-linux/)

## Building

- `make build_libs` - Build the libraries (libDaisy)
- `make build_and_program` - Clean, build, and program the device
- `make build_and_program_dfu` - Clean, build, and program the device via DFU

## Notes

This boilerplate is intentionally kept minimal. The DaisySP DSP library is not included by default, but can be easily added as a git submodule with:

```bash
git submodule add https://github.com/electro-smith/DaisySP libs/DaisySP
```

Once added, uncomment the DaisySP lines in the `build_libs` target in the Makefile to build it alongside libDaisy.