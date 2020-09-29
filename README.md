# SSD1306 OLED MakeCode Package [![Build Status](https://travis-ci.org/Tinkertanker/pxt-oled-ssd1306.svg?branch=master)](https://travis-ci.org/Tinkertanker/pxt-oled-ssd1306)

This is the MakeCode Package for SSD1306 OLED controller, based on the Adafruit Arduino library available [here](https://github.com/adafruit/Adafruit_SSD1306).

## Hardware Setup
1. Insert the OLED display into the I2C ports on the break out board.

## Blocks
### Initialize OLED Display
Initializes the OLED display.

Sets up the OLED display and prepares it for use by the micro:bit.

```sig
ssd1306.init(128, 64,DigitalPin.P2,0x3D);

```

This block must be placed before any of the ``show`` blocks.

### Show String Without Newline
Displays a string on the OLED module without a newline.

```sig
ssd1306.showString1("hello, micro:bit!")
```

The ``init`` block must be placed before this.

### Show String With Newline
Displays a string on the OLED module with a newline.

```sig
ssd1306.showString2("hello, micro:bit!")
```

The ``init`` block must be placed before this.


### Show Number Without newline
Displays a number on the OLED module without a newline.

```sig
ssd1306.showNumber1(123)
```

The ``init`` block must be placed before this.


### Show Number With Newline
Displays a number on the OLED module with a newline.

```sig
ssd1306.showNumber2(123)
```

The ``init`` block must be placed before this.


### Clear Display
Clears the display.

```sig
ssd1306.clear()
```

The ``init`` block must be placed before this.

### Draw Outlined Rectangle
Displays an outline of a rectangle.

```sig
ssd1306.drawRectangle(x,y,w,h)
```

The ``init`` block must be placed before this.


### Draw Outlined Circle
Displays an outline of a circle.

```sig
ssd1306.drawCircle(x,y,r)
```

The ``init`` block must be placed before this.


### Draw Line
Displays a line.

```sig
ssd1306.drawLine(x1,y1,x2,y2)
```

The ``init`` block must be placed before this.


### Progress bar
Displays a progress bar with a specified percentage of progress.

```sig
ssd1306.drawLoadingBar(percent)
```

The ``init`` block must be placed before this.


## Example: Counter
The following code is a simple counter that displays an increasing number every second.

```blocks
ssd1306.init(64, 128)
let item = 0
basic.forever(() => {
    basic.pause(1000)
    item += 1
    ssd1306.showNumber(item)
})
```

## Supported targets

* for PXT/microbit

## Footnotes

1.  Datasheet https://cdn-shop.adafruit.com/datasheets/SSD1306.pdf



> Ouvrir cette page à [https://schoumi.github.io/ssd1306-with-reset/](https://schoumi.github.io/ssd1306-with-reset/)

## Utiliser comme extension

Ce dépôt peut être ajouté en tant qu'**extension** dans MakeCode.

* ouvrir [https://makecode.microbit.org/](https://makecode.microbit.org/)
* cliquez sur **Nouveau projet**
* cliquez sur **Extensions** dans le menu engrenage
* recherchez **https://github.com/schoumi/ssd1306-with-reset** et importez

## Éditer ce projet ![Badge du statut de la compilation](https://github.com/schoumi/ssd1306-with-reset/workflows/MakeCode/badge.svg)

Éditer ce dépôt dans MakeCode.

* ouvrir [https://makecode.microbit.org/](https://makecode.microbit.org/)
* cliquez sur **Importer** puis cliquez sur **Importer l'URL **
* collez **https://github.com/schoumi/ssd1306-with-reset** et cliquez sur importer

## Aperçu des blocs

Cette section montre le code des blocs du dernier commit dans la branche master.
Cette image peut prendre quelques minutes pour être actualisée.

![Un rendu de la vue des blocs](https://github.com/schoumi/ssd1306-with-reset/raw/master/.github/makecode/blocks.png)

#### Métadonnées (utilisées pour la recherche, le rendu)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
