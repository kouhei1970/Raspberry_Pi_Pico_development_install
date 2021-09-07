# Raspberry Pi Picoの開発環境のインストール手順

## WIndows10＋WSL2＋Ubuntu20.04の場合
UbuntuやMacで環境を整える場合は、SDKとEXAMPLEのCloneから作業を行ってください。

- Windows10を最新版にアップデートする　
- PowerShell管理者で以下を実行

```
wsl --install -d Ubuntu
```

## SDKとEXAMPLEのClone
```
cd ~/ 
mkdir pico
cd pico
git clone -b master https://github.com/raspberrypi/pico-sdk.git
cd pico-sdk
git submodule update --init
cd ..
git clone -b master https://github.com/raspberrypi/pico-examples.git
```

## Toolchainインストール 

```
sudo apt update
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential 
```
