# LHT00SU1

* https://www.youtube.com/watch?v=KiDDL5xtnG0
* https://sigrok.org/wiki/Noname_LHT00SU1
* https://www.flippermarkt.de/community/forum/threads/logikanalyser-lht00su1-mit-sigrok.257381
  * Auf der Platine des LHT00SU1 befindet sich eine Brücke, die eingelegt einen Schreibschutz für das EEPROM aktiviert und somit verhindert, dass Sigrok den notwendigen Treiber in das Teil schreiben kann. Brücke entfernt ---> läuft


* https://www.aliexpress.com/item/32997787461.html CHF27.16


```bash
sudo dmesg --follow
[  744.819106] usb 3-7: new high-speed USB device number 15 using xhci_hcd
[  744.945435] usb 3-7: New USB device found, idVendor=08a9, idProduct=0014, bcdDevice= 0.00
[  744.945447] usb 3-7: New USB device strings: Mfr=0, Product=0, SerialNumber=0

lsusb
Bus 003 Device 015: ID 08a9:0014 CWAV Inc. USBee AX-Pro
```


## Installation

* Remove jumper H2
* `sudo ./pulseview-NIGHTLY-x86_64-release.appimage`
  * Pluseview starts with
    * `CWAV USBee AX` selected
    * D0 .. D7
    * A0
