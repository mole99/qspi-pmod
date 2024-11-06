# QSPI Pmod

A QSPI Pmod board designed in KiCad with one SPI Flash and two PSRAMs.

![PCB](img/qspi-pmod.png)

# Pinout

| Pmod  | TinyTapeout | Function    | Note |
|-------|-------------|-------------|------|
| PMOD1 | uio[0]      | CS0 (Flash) | Cut trace to disable (see below) |
| PMOD2 | uio[1]      | SD0/MOSI    |      |
| PMOD3 | uio[2]      | SD1/MISO    |      |
| PMOD4 | uio[3]      | SCK         | Short `CK` ("CLOCK cap") pin pair for delay by 22pF cap |
| PMOD5 | uio[4]      | SD2         |      |
| PMOD6 | uio[5]      | SD3         |      |
| PMOD7 | uio[6]      | CS1 (RAM A) | Cut trace to disable (see below) |
| PMOD8 | uio[7]      | CS2 (RAM B) | Cut trace to disable (see below) |

> [!NOTE]
> On the bottom side of the PCB, you can cut the traces for any of the 3 CS pins to disable its respective memory IC. When cut, a 1k resistor pulls up the chip's `/CS` to disable it. In this case, the respective pin could be used (via header thru-hole on the other side of the cut) as either an input or output.
