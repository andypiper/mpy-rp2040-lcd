# MicroPython code for the Waveshare RP2040-LCD 0.96"

- [product page](https://www.waveshare.com/rp2040-lcd-0.96.htm)
- [wiki](https://www.waveshare.com/wiki/RP2040-LCD-0.96)

The board is similar to a Raspberry Pi Pico: same dimensions, with USB-C and a 0.96" 160x80 LCD (ST7735) mounted on the front, and a MX1.25 battery header.

## LCD pins

```mermaid
graph LR
    p1(GP8):::gpio  --> l1(LCD_DC):::lcd
    p2(GP9):::gpio  --> l2(LCD_CS):::lcd
    p3(GP10):::gpio --> l3(LCD_CLK):::lcd
    p4(GP11):::gpio --> l4(LCD_DIN):::lcd
    p5(GP12):::gpio --> l5(LCD_RST):::lcd
    p6(GP25):::gpio --> l6(LCD_BL):::lcd
    classDef gpio fill:#7BC942;
    classDef lcd fill:#C0C0C0;
```

## Code

- Initial experiment using the [MicroPython-ST7735 driver](https://github.com/boochow/MicroPython-ST7735) seems to work well. Modified the bitmap sample to match the appropriate pins.
