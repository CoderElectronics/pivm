# PiVM
PiVM is a fully set up virtualization hypervisor for the Raspberry Pi 4B. PiVM is fully headless, and is ready to go, requiring only ethernet and power. This release includes pivmwebui v0.1.0 and Cockpit-machines with full 64-bit KVM Support. 

## Login
The system-wide default login is:
Username: pivmadmin
Password: pivmhost2020

## Hardware
This image is made for a 32gb SD card, and split into multiple files which need to all be downloaded and combined and then unzipped. It will need to be expanded to take full advantage of a larger SD card. <br />
This image is only supported by the Raspberry Pi 4. Since this will virtualize multiple guests, it is recommended to have at least a Pi with 4gb of RAM.

## Software
Go to the releases page of this github to access the pre-made ISOs.
This image is based on Ubuntu Core 20.04, with Cockpit and a fully-featured aarch64 (arm64) KVM setup. This image includes a Debian aarch64 (arm64) installation image in the `/home/pivmadmin/boot-disks` for testing. There is a pre-setup disk pool named `SD - Virtual Disks` residing on the SD card, it is recommended to use a USB disk as the primary location for virtual disks to prevent wear on the SD card. <br />
Once combined, unzipped, and flashed to your Pi, go to the Pi's IP address in your browser and your should see a login screen.
![Login Screen](https://pivm-site.surge.sh/login.png)
<br />
Login with the default username and password, which you can change through your Pi's terminal in Cockpit. Once you are logged in, you can see system information, follow the instructions on the page to go to Cockpit. The default login for Cockpit is the same as the system login.

## Tested ISOs
Debian ARM: Included in the release ISO <br />
Ubuntu ARM: <http://cdimage.ubuntu.com/ubuntu/releases/18.04/release/ubuntu-18.04.4-server-arm64.iso>

### Future Features
- [ ] Add more styling to the PiVM Web UI
- [ ] Create a custom KVM/QEMU Web UI 
- [ ] Add user managment to PiVM Web UI
- [ ] Add WiFi setup to the PiVM Web UI
- [ ] Add NAS functionality to the PiVM Web UI
- [ ] Add external disk setup to the PiVM Web UI
