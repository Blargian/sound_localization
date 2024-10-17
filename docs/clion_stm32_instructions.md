# How to setup development for STM32 with CLion on Ubuntu

Download [AArch32 bare-metal target (arm-none-eabi)](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads). Run the following command from the download location:

```
sudo tar xJf arm-gnu-toolchain-13.3.rel1-x86_64-arm-none-eabi.tar.xz -C /usr/share
```

For CLion to detect the toolchain, it should be presented in system PATH. You can check it by running arm-none-eabi-gcc from the command line - your system should recognize this command. 
