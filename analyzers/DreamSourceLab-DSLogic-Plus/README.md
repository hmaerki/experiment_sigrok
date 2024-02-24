# DreamSourceLab DSLogic Plus

## Links

https://sigrok.org/wiki/DreamSourceLab_DSLogic_Plus
https://sigrok.org/wiki/DreamSourceLab_DSLogic
https://www.zzzconsulting.se/2020/04/25/sigrok-usb-dev.html

###

```bash
$ dmesg --follow
[17863.083088] usb 3-1: new high-speed USB device number 30 using xhci_hcd
[17863.684290] usb 3-1: New USB device found, idVendor=2a0e, idProduct=0030, bcdDevice= 0.01
[17863.684302] usb 3-1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[17863.684306] usb 3-1: Product: USB-based DSL Instrument v2
[17863.684309] usb 3-1: Manufacturer: DreamSourceLab
```

https://sigrok.org/wiki/DreamSourceLab_DSLogic_Plus

New hardware variant received early 2023, enumerates as 2a0e:0030, and uses a different vendor's FPGA. Currently incompatible with sigrok.

**Very frustrating: Currently incompatible with sigrok!!!**

## Simplest use

## AppImage

https://sigrok.org/wiki/Downloads#Binaries_and_distribution_packages

```bash
wget https://sigrok.org/download/binary/sigrok-cli/sigrok-cli-NIGHTLY-x86_64.AppImage
wget https://sigrok.org/download/binary/pulseview/PulseView-NIGHTLY-x86_64.AppImage
chmod a+x *.AppImage
sudo ./PulseView-NIGHTLY-x86_64.AppImage
```

![](screenshots/select_device.png)


```bash
sudo ./sigrok-cli-NIGHTLY-x86_64.AppImage --scan
The following devices were found:
demo - Demo device with 13 channels: D0 D1 D2 D3 D4 D5 D6 D7 A0 A1 A2 A3 A4
fx2lafw - Saleae Logic with 8 channels: D0 D1 D2 D3 D4 D5 D6 D7
```

