# experiment_sigrok
Experiments with sigrok


## Remove

```bash
sudo apt remove sigrok-cli sigrok-firmware-fx2lafw pulseview
```

## Compile

```bash
$ sudo apt install -y libgirepository1.0-dev python3-gi python3-numpy swig libgirepository1.0-dev gcc libcairo2-dev pkg-config python3-dev gir1.2-gtk-3.0

$ git clone https://github.com/sigrokproject/libsigrok
$ cd libsigrok
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
```

```bash
$ git clone https://github.com/sigrokproject/sigrok-cli.git
$ cd sigrok-cli
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
```

==> Failed, too complex. Shared library missing

## AppImage

https://sigrok.org/wiki/Linux#Building_(script,_recommended)

https://sigrok.org/wiki/Downloads#Binaries_and_distribution_packages

```bash
wget https://sigrok.org/download/binary/sigrok-cli/sigrok-cli-NIGHTLY-x86_64.AppImage
wget https://sigrok.org/download/binary/pulseview/PulseView-NIGHTLY-x86_64.AppImage
chmod a+x *.AppImage
sudo ./PulseView-NIGHTLY-x86_64.AppImage
```