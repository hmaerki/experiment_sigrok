# Test Sigrok Saleae Clone on UART

## FT232RL
  https://www.aliexpress.com/item/1005006445462581.html

Jumper on 5V

Pins:

(GND)  DTR - RX - TX - VCC - CTS - GND

## Saleae Clone

https://www.aliexpress.com/item/4000146595503.html

## Connection

| FT232RL | Saleae | 
| - | - |
| GND | CND |
| TX | CH1 |

## Testing

```bash
sudo stty -F /dev/ttyUSB0 9600

ls -lR / > /dev/ttyUSB0
```

Now use PluseView, select CH1 and decode UART 9600buad


## Testing on the command line

* Nice video on sigrok-cli: https://www.youtube.com/watch?v=dobU-b0_L1I
* Nice examples: https://sigrok.org/wiki/Getting_started_with_a_logic_analyzer
* https://sigrok.org/wiki/Sigrok-cli

### Using 9600 baud

```bash
sudo ./sigrok-cli-NIGHTLY-x86_64-release.appimage --driver fx2lafw --config samplerate=1m --config captureratio=10 --channels D0,D1 --protocol-decoders uart:rx=D0:baudrate=9600:parity=none:sample_point=50:format=ascii --protocol-decoder-annotations uart=rx_data --triggers D0=f --time=1s

Second terminal:
sudo stty -F /dev/ttyUSB0 9600
echo hallo > /dev/ttyUSB0 

Output in first terminal:
uart-1: h
uart-1: a
uart-1: l
uart-1: l
uart-1: o
uart-1: [0D]
uart-1: [0A]
```

### Using 115200 baud

```bash
sudo ./sigrok-cli-NIGHTLY-x86_64-release.appimage --driver fx2lafw --config samplerate=24m --config captureratio=10 --channels D0,D1 --protocol-decoders uart:rx=D0:baudrate=115200:parity=none:sample_point=50:format=ascii --protocol-decoder-annotations uart=rx_data --triggers D0=f --time=1s

Second terminal:
sudo stty -F /dev/ttyUSB0 115200
echo hallo > /dev/ttyUSB0 
```
