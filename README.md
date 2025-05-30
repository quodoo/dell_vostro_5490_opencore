# Dell Vostro 5490 (Comet Lake U) Hackintosh
[![](https://img.shields.io/badge/EFI-Release-informational?style=flat&logo=apple&logoColor=white&color=9debeb)](https://github.com/Lorys89/DELL_VOSTRO_5490/releases)



EFI for Dell Vostro 5490 with OpenCore bootloader

![descrizione](./Screenshot/pc.png)

### Computer Spec:

| Component        | Brank                              |
| ---------------- | ---------------------------------- |
| CPU              | Intel i5 10510U (4C-8T 6MB CML-U)  |
| iGPU             | Intel® UHD Graphics                |
| DGPU.            | Nvidia MX250 2GB GDDR5             |
| Lan              | Realtek 8168                       |
| Audio            | Realtek ALC236                     |
| Ram              | 16 GB DDR4 2667 Mhz                |
| Wifi + Bluetooth | BCM94360ng (OCLP patching)         |
| NVMe             | Samsung 970 evo pluss GB (MACOS)   |
| SSD SATA         | Silicon Power A55 256 GB (WIN 11)  |
| SmBios           | MacBookPro 16,3                    |
| BootLoader       | OpenCore 1.0.1                     |
| macOS            | Sequoia 15.0                       |


![infomac](./Screenshot/info_Sequoia.png)

### What works and What doesn't or WIP:

- [x] Intel UHD iGPU eDP with Backlight Output
- [x] Intel UHD iGPU HDMI Output
- [x] Intel UHD iGPU Type-C to HDMI Output
- [x] Intel UHD iGPU - H264 & HEVC
- [ ] DGPU Nvidia MX250 2GB GDDR5 (Not Support)
- [x] ALC236 Internal Speakers
- [ ] Intel SST DMIC Internal microphone (Not Support)
- [x] ALC236 Combojack headphones
- [ ] ALC236 Combojack microphone (WIP)
- [x] ALC236 HDMI Audio Output
- [x] ALC236 TYPE-C to HDMI Audio Output (Not supported at the moment)
- [x] All USB-A 3.1 Ports (TYPE-C 3.2 Included)
- [x] SpeedStep / Sleep / Wake
- [x] HID Key PWRB & SLPB 
- [x] I2C Touchpad with gesture
- [x] Keyboard (PS2-Internal) with backlight
- [x] F6 & F7 Brightness Key
- [x] F10 Print Screen Key
- [x] F1 & F2 & F3 Sound Key
- [x] Wi-Fi and Bluetooth BCM94360ng Module (OCLP patching)
- [x] Realtek RTL8168 LAN
- [x] SSD NVME Slot-1 PciE Gen3x4
- [x] Sata Slot AHCI
- [x] Micro SD Cardreader (USB-Internal)
- [x] WebCam (USB-Internal)
- [x] All Sensors CPU, IGPU, BATTERY, NVME, SATA, FAN
- [x] ACPI Battery
- [x] NVRAM (Native)
- [x] Recovery (macOS) boot from OpenCore
- [x] Windows 11 boot from OpenCore

## Peripherals & TouchPad Setting & Benchmarks

![infohack](./Screenshot/periferiche.png)
![infodp2](./Screenshot/pci-list.png)
![Temp-Fan-Control](./Screenshot/Temp-Fan-Control.png)
![speedtest](./Screenshot/speedtest.png)
![touchpad](./Screenshot/touchpad.png)
![trascinamento](./Screenshot/trascinamento.png)
![videoproc](./Screenshot/videoproc.png)


### Special Config:

- Usb port mapping performed
- SSDT-Hack Essential patch

See [ioreg](./ioreg%20MacBook%20Pro%2016%2C3.ioreg) for more clarification


### MacOS bootable USB creation:
- Read the Dortania guide for creating your USB from Windows or macOS
- [Guide Dortania](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) - USB creation


## Bios settings
### Enable :
* SATA Operation : AHCI
* Fastboot : Thorough
* Integrated NIC : Enable


### Disable : 
* Secure Boot
* Absolute
* Intel SGX
* SMM Security Migration
* Wake on AC
* Wake on Dell USB-C Dock
* Power On Lid Open
* Enable UEFI Network Stack
* Sign Of Life : Early Logo Display / Early keyboard backlight
* cfg lock and DVMT: It is essential to set it up to start with this EFI


 ![CFG-Lock](./Screenshot/CFG-Lock.png)
 ![DVMT](./Screenshot/DVMT.png)
 
Create a usb in FAT with MBR map and put [ru.efi](https://github.com/Lorys89/DELL_VOSTRO_5401-ICE-LAKE/raw/main/TOOLS%20EFI%20MOD/RU.efi) in it 
then go to the bios, and create an entry with the path of the usb and setting the ru.efi file and the name of 
your choice startup and then send and finally click apply.

Restart and press f12 among the entries you will have the last created, click any key, then click alt + ì a menu will appear and
scroll to CpuSetup and click enter, in the new screen go with the arrows on the value 003E and change to 00 and click 
enter and then ctrl + w to save and then alt + q to exit. proceed to check if your CFG LOCK is unlocked.

![CpuSetup](./TOOLS%20EFI%20MOD/CpuSetup.png)

For the 2 DVMT values you have to go to the SaSetup menu and enter and look for 00F5 and set it to 02 and then move 
next to 00F6 and set it to 03 then save with ctrl + w and to exit alt + q and you will have the suitable DVMT values to the igpu ice lake. 

![SaSetup](./TOOLS%20EFI%20MOD/SaSetup.png)


### Working all NATIVE-SHORTCUTS-APPLE:

![APPLE-NATIVE-SHORTCUTS](./Screenshot/APPLE-NATIVE-SHORTCUTS.png)

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
# dell_vostro_5490_opencore
# dell_vostro_5490_opencore
# dell_vostro_5490_opencore
