# Preparing your PC

## Software to download

* Visual Studio Code: [VSCode](https://code.visualstudio.com/download)
* Distributed version control system: [Git](https://git-scm.com/downloads)
* USB driver installation made easy: [Zadig](https://github.com/pbatard/libwdi/releases/download/v1.5.0/zadig-2.8.exe)

## Installation Sequence

* Open *Regedit*
  * Go to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem in regedit and then set LongPathsEnabled to 1.

* Install Git
   * Open *Git CMD*
   * Run the command **git config --global core.longpaths true**
   * Reboot

* Install VSCode
  
* If you are using Linux, before instaling the PlatformIO extension you must install the package python3-venv. If you are using a Debian based distribution:

    sudo apt install python3-venv

* Open VSCode and click the extensions Icon

  * Search for "PlatformIO"
  * Install PlatformIO
  * VSCode will ask to restart

## Compiling the Project

* In VSCode choose **File->Open Folder...** and select the folder where the project is.
* If it is the first time, the next step can take a long time because PlatformIO wil have to download the compiler, the tools and the libraries. It will happen just for the first time if the process completes without errors. When everything is installed the icon with a checkmark in the bottom must be clicked to build the firmware.

## Flash for the first time

* Drag the file named “firmware.uf2”, that is located in the folder “PlatformIO/Projects/<your_prject_name>/.pio/build/pico”, and drop it on the USB Mass Storage device corresponding to the Raspberry Pi Pico.

##  Install Drivers (Windows)

* Run Zadig and select RP2 Boot (Interface 1) from the dropdown box and select WinUSB as the driver
* Click the "Install Driver" button. Wait for the installation to complete - this may take a few minutes.

