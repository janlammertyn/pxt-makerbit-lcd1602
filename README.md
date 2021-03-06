# MakerBit LCD1602

[![Build Status](https://travis-ci.org/1010Technologies/pxt-makerbit-lcd1602.svg?branch=master)](https://travis-ci.org/1010Technologies/pxt-makerbit-lcd1602)

MakeCode extension for I2C LCD 1602 displays.

## MakerBit Board

The MakerBit connects to the BBC micro:bit to provide easy connections to a wide variety of sensors, actuators and other components, for example a LCD display.

http://makerbit.com/

| ![MakerBit](https://github.com/1010Technologies/pxt-makerbit/raw/master/MakerBit.png "MakerBit") | ![MakerBit+R](https://github.com/1010Technologies/pxt-makerbit/raw/master/MakerBit+R.png "MakerBit+R") |
| :----------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------: |
|                                            _MakerBit_                                            |                                   _MakerBit+R with motor controller_                                   |

## LCD

This extension supports printing text and numbers on an I2C LCD 1602.
Displays with I2C address 39 or 63 will work automatically. Use connectLCD to explicitly connect to a different I2C address.

### LCD Example

```blocks
makerbit.setLcdBacklight(LcdBacklight.Off)
makerbit.showStringOnLcd("MakerBit", 0, 9)
makerbit.showNumberOnLcd(42, 16, 18)
basic.pause(2000)
makerbit.clearLcd()
```

### MakerBit showStringOnLcd

Displays a text on the LCD in the given position range. The text will be cropped if it is longer than the provided range. If there is space left, it will be filled with whitespaces.

```sig
makerbit.showStringOnLcd("Hello world", 0, 5)
```

### MakerBit showNumberOnLcd

Displays a number on the LCD in the given position range. The text will be cropped if it is longer than the provided range. If there is space left, it will be filled with whitespaces.

```sig
makerbit.showNumberOnLcd(42, 16, 18)
```

### MakerBit clearLcd

Clears the LCD completely.

```sig
makerbit.clearLcd()
```

### MakerBit setLcdBacklight

Enables or disables the backlight of the LCD.

```sig
makerbit.setLcdBacklight(LcdBacklight.On)
```

### MakerBit connectLcd

Connects to the LCD at a given I2C address. The addresses 39 (PCF8574) or 63 (PCF8574A) seem to be widely used.

```sig
makerbit.connectLcd(39)
```

### MakerBit isLcdConnected

Returns true if a LCD is connected. False otherwise.

```sig
makerbit.isLcdConnected()
```

## License

Licensed under the MIT License (MIT). See LICENSE file for more details.

## Supported targets

- for PXT/microbit
- for PXT/calliope
