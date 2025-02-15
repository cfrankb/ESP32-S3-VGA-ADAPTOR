# Encoding

Colors are encoded as unsigned 16bits integer (B5G6R5).

The five (5) lowest bits are red and in accending order of brigtness. The next six (6) bits are green and the last five (5) bits are blue.


# Hardware

## ESP32-S3

Recommended ESP32S3 DevKit.

https://vi.aliexpress.com/item/1005006418608267.html

## Dupont cables

https://www.aliexpress.com/item/1005004611997111.html


## VGA Adaptor

An adaptor is needed to communicate with the VGA Hardware.

![Image](images/20250202_211146-crop.jpg "icon")

![Image](images/vga_test.jpg "icon")



### Manually assembled


![Image](images/20241221_100637-crop.jpg "icon")

Create a resistor ladder wire. Connect all the pins of the same color together.


| GPIO Pin | Role  | Resistor | VGA Pin |
| -------- | ----- | -------- | ------- |
| 1        | hsync | 47R      | 13      |
| 2        | vsync | 47R      | 14      |
| 4        | red   | 8k       | 1       |
| 5        | red   | 4k       |
| 6        | red   | 2k       |
| 7        | red   | 1k       |
| 8        | red   | 512R     |
| 9        | green | 16k  *   | 2       |
| 10       | green | 8k       |
| 11       | green | 4k       |
| 12       | green | 2k       |
| 13       | green | 1k       |
| 14       | green | 512R     |
| 15       | blue  | 8k       | 3       |
| 16       | blue  | 4k       |
| 17       | blue  | 2k       |
| 18       | blue  | 1k       |
| 21       | blue  | 512R     |
| GND      | -     | -        | 5, 10   |

\* If you don't have any 16k Resistor. You can use a similar value such as 20k. The smallest resistor is the most significant and should be roughtly ~500R or higher.

VGA Connector: [DB15 to Dip 2.54mm interface ](https://vi.aliexpress.com/item/1005005279582020.html)

## Demo Project

![Image](images/20241221_100753-crop.jpg "icon")

Gameplay: https://www.youtube.com/watch?v=SPQwWkzFRpU

Source code: [cfrankb/ESP32-S3-VGA-CS3](https://github.com/cfrankb/ESP32-S3-VGA-CS3) 


