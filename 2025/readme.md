# REGIO finale Limburg 2025

Create a new _solder kit_ for a side-activity during the _First LEGO League_ (FLL) contests in regio Limburg.


## Introduction

In 2023, I made the "LEGO man soldering kit" for De Kempel.
Soldering the kit is a side activity during the First LEGO League (FLL) regional finals (I guess region Noord Brabant - East).

We got contacted by the project lead of the FLL for REGIO finale Limburg to make a similar soldering kit.
They asked and got permission to reuse design made for De Kempel, while also replacing the Kempel's logo.


## Concept 1

Two concepts were generated, one replacing the logo with 3 bricks, 
and one replacing the logo with two L's (Limburg LEGO).
The former was selected.

![xx](man-b-b-b.jpg) ![xx](man-l-l.jpg)

Some decisions:
- eyes blinking blue;
- mouth permanent yellow (orange);
- logo permanent red and permanent green and blinking red/green in the middle;
- switch the USB-C [connector](USBC-2Pin-Horizontal-Female__LCSC-C2919656.png);
- make all LEDs bend the same way.


## Design

First step is to make the schematics. I did that in [EasyEda](https://easyeda.com/), 
a Chinese in-browser design tool. The [easyeda source](ElektroClub2025FLL_V2_schem.json) 
as well as the [pdf](ElektroClub2025FLL_V2_schem.pdf) is in this repository.

Next step is to make a pcb layout. Also done with EasyEDA.
I used the artistic drawings `brick*.png` derived from the gimp source [brick.xcf](brick.xcf).
The [easyeda source](ElektroClub2025FLL_V2_pcb.json) 
as well as the [pdf](ElektroClub2025FLL_V2_pcb.pdf) is in this repository.

In the end, the [gerber](ElektroClub2025FLL_V2_gerber.zip) is used for PCB manufacturing.

![render](render-front-back-side.png)


## PCB manufacturing trial run order

I sent the gerber to [jlcpcb](https://jlcpcb.com/).
I did a trial run
- of 5 pieces (FR-4, 2 layers)
- thinner than normal (not 1.6 but 1.0 mm to save on shipping later when ordering 200 boards)
- red PCB with white silk screen
- JLCJLCJLCJLC marks where JlcPcb should put the order number

See [detail](jlcpcb5.png) of my order (€ 11.34).


## Components order

Until now this has been spent.

|item| description                          | quantity |    price |                                                      link |
|:--:|:-------------------------------------|---------:|---------:|:---------------------------------------------------------:|
|  1 | LED blinking blue for eyes           |    2×200 |    13.35 |[🔗](https://www.aliexpress.com/item/1005003630965480.html)|
|  2 | LED permanent yellow mouth           |      200 |     4.28 |[🔗](https://www.aliexpress.com/item/1005006463058075.html)|
|  3 | LED permanent red logo               |      200 |     4.26 |[🔗](https://www.aliexpress.com/item/1005006463058075.html)|
|  4 | LED permanent green go               |      200 |     4.00 |[🔗](https://www.aliexpress.com/item/1005006463058075.html)|
|  5 | LED blinking red/green logo          |      200 |     5.68 |[🔗](https://www.aliexpress.com/item/1005006514757908.html)|
|  6 | Resistors 220 ohm                    |    6×200 |    15.36 |[🔗](https://www.aliexpress.com/item/1005002091320103.html)|
|  7 | USB connector female C               |      200 |    21.50 |[🔗](https://www.aliexpress.com/item/1005004403587119.html)|
|  8 | Zip-lock backs B-8×12 cm             |      200 |     5.16 |[🔗](https://www.aliexpress.com/item/1005005297741601.html)|
|  9 | Trial run 5 PCBs                     |        5 |    11.34 |[🔗](jlcpcb5.png)                                          |
| 10 | Main run 200 PCBs                    |          |     ?.?? |                                                           |
|    |                                      |          |_________+|                                                           |
|    | Total cost (maps to €1.01 per kit)   |          |    84.93 |                                                           |


(end)
