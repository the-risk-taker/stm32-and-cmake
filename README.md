# STM32 & CMake

Project generated with STM32CubeMX ported to CMake. Tested on [NUCLEO-L476RG](https://www.st.com/en/evaluation-tools/nucleo-l476rg.html). Good [Reference](https://stackoverflow.com/a/43836115) on StackOverflow.

## Requirements

- [Arm GNU Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads)
- [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html)
- CMake
- Ninja

All in PATH.

## Setup, building and programming

Setup project by calling:

```shell
cmake -DCMAKE_TOOLCHAIN_FILE=cmake/arm-none-eabi-gcc.cmake -DCMAKE_BUILD_TYPE=Release -S. -B build -G Ninja
```

Build project:

```shell
ninja -C build
```

Write the program:

```shell
ninja -C program
```
