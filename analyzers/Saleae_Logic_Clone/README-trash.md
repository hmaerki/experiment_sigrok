# Experiment without success


## Tests

```bash
# dmesg --follow
[ 2430.583782] usb 3-1: new high-speed USB device number 6 using xhci_hcd
[ 2430.736077] usb 3-1: New USB device found, idVendor=0925, idProduct=3881, bcdDevice= 0.01
[ 2430.736089] usb 3-1: New USB device strings: Mfr=0, Product=0, SerialNumber=0
```

```bash
# sudo sigrok-cli --scan
```

## Compile

https://sigrok.org/wiki/Fx2lafw

```bash
$ git clone git://sigrok.org/sigrok-firmware-fx2lafw
$ cd sigrok-firmware-fx2lafw
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
$ ls -l /usr/local/share/sigrok-firmware
-rw-r--r-- 1 root root 341436 Feb 23 21:55 dreamsourcelab-dscope-fpga.fw
-rw-r--r-- 1 root root   8120 Feb 23 21:55 dreamsourcelab-dscope-fx2.fw
-rw-r--r-- 1 root root 341160 Feb 23 21:55 dreamsourcelab-dslogic-basic-fpga.fw
-rw-r--r-- 1 root root   8120 Feb 23 21:55 dreamsourcelab-dslogic-basic-fx2.fw
-rw-r--r-- 1 root root 341160 Feb 23 21:55 dreamsourcelab-dslogic-fpga-3v3.fw
-rw-r--r-- 1 root root 341160 Feb 23 21:55 dreamsourcelab-dslogic-fpga-5v.fw
-rw-r--r-- 1 root root   8120 Feb 23 21:55 dreamsourcelab-dslogic-fx2.fw
-rw-r--r-- 1 root root 341160 Feb 23 21:55 dreamsourcelab-dslogic-plus-fpga.fw
-rw-r--r-- 1 root root   8120 Feb 23 21:55 dreamsourcelab-dslogic-plus-fx2.fw
-rw-r--r-- 1 root root 341436 Feb 23 21:55 dreamsourcelab-dslogic-pro-fpga.fw
-rw-r--r-- 1 root root   8120 Feb 23 21:55 dreamsourcelab-dslogic-pro-fx2.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-braintechnology-usb-lps.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-cwav-usbeeax.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-cwav-usbeedx.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-cwav-usbeesx.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-cwav-usbeezx.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-cypress-fx2.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-hantek-6022be.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-hantek-6022bl.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-hantek-pso2020.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-instrustar-isds205b.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-sainsmart-dds120.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-saleae-logic.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-sigrok-fx2-16ch.fw
-rw-r--r-- 1 root root   8120 Feb 24 11:27 fx2lafw-sigrok-fx2-8ch.fw
-rw-r--r-- 1 root root  16312 Feb 24 11:27 fx2lafw-yixingdianzi-mdso.fw
```

```bash
$ sudo sigrok-cli -L | grep fx2
```
