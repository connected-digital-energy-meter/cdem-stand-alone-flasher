# CDEM - Stand Alone Flasher

Flash ESP32 HUZZAH32 Feather Boards without the need to install Arduino IDE.

You will need the Arduino IDE to build the firmware package. Or you can download our releases at [Connected Digital Energy Meter - Firmware Releases](https://github.com/connected-digital-energy-meter/cdem_firmware/releases). Look for a release that includes a `stand_alone_cdem_firmware_vx_x_x.tar.gz` package.

All you need is git, python and Internet.

## Install Dependencies

```bash
sudo apt update
sudo apt install git
sudo apt install python-pip
pip install pyserial
```

## Get this repo

```bash
cd ~
git clone https://github.com/connected-digital-energy-meter/cdem-stand-alone-flasher.git
cd cdem-stand-alone-flasher
```

## Building the Release Package

Open the source project in Arduino IDE and hit the build button. This should generate an `arduino_build_xxxxx` directory in `/tmp`.

Now execute the build script in this repo:

```bash
./build
```

It should generate a `stand_alone_cdem_firmware_vx_x_x.tar.gz` file that can be uploaded to GitHub as a stand alone release package.

## Flashing a Stand Alone Release

Download the latest stand alone release package from [Connected Digital Energy Meter - Firmware Releases](https://github.com/connected-digital-energy-meter/cdem_firmware/releases). Look for a release that includes a `stand_alone_cdem_firmware_vx_x_x.tar.gz` package.

Just place the file inside this repository dir as is. **Just make sure that there is only a single stand alone release file in this directory.** Don't rename the file and extract it yourself. Its all automatically done for you.

Now connect the board and execute the `flash` script:

```bash
./flash
```