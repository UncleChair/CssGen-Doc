---
id: border-styles
title: Border
description: Add line or image border
parent: advance-component
previous: advance-component
next: padding-styles
order: 0
demos:
  - key: border-editor
    title: Border Example
    component: BorderEditor
    sticky: true
---

# Border Style Component

_Add line or image border around the layer._

<!-- demo:border-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

## Normal Mode

In normal mode, you can set the basic line border, including border style<sup><a href="#ref1">[1]</a></sup>, border width<sup><a href="#ref2">[2]</a></sup> and border color<sup><a href="#ref3">[3]</a></sup>.

### Border Style

The border style includes:

- Solid: <div style="border-top:solid 4px; width: 100px;"></div>
- Dashed: <div style="border-top:dashed 4px; width: 100px;"></div>
- Dotted: <div style="border-top:dotted 4px; width: 100px;"></div>
- Double: <div style="border-top:double 4px; width: 100px;"></div>

> The border width and border color will not take effect if the border style is not set.

### Border Width

The border width supports numbers and units, the number part can be input directly or dragged with the slider, the supported units include:

- px<sup><a href="#ref4">[4]</a></sup>: Pixel, for ordinary screens, usually a device pixel
- pt<sup><a href="#ref5">[5]</a></sup>: Point
- em<sup><a href="#ref6">[6]</a></sup>: Element font size
- vh<sup><a href="#ref7">[7]</a></sup>: Percentage of viewport height
- vw<sup><a href="#ref8">[8]</a></sup>: Percentage of viewport width

The default unit is px, you can also manually input other units<sup><a href="#ref9">[9]</a></sup>.

### Border Color

Click the border color block to pop up the color selector, you can use the color palette, color picker or color code to select the color.

The color code mode allows switching, currently supports:

- RGB(A)
- HSL(A)
- HEX(A)

## Advanced Mode

In advanced mode, you can add an image as a border<sup><a href="#ref10">[10]</a></sup> to get a richer display effect.

### Select Image

Click the select image button to pop up the project image list, you can select the image or add a new image here.

### Adjust Slice

After selecting the image, you can adjust the slice to divide the border image in the expected mode. We have already used it in [Edit Style](./edit-style), the division modes of the nine regions are as follows<sup><a href="#ref11">[11]</a></sup>: 

||Nine Region Division||
|-|-|-|
|Top-Left Corner|Top Border|Top-Right Corner|
|Left Border|Middle Region|Right Border|
|Bottom-Left Corner|Bottom Border|Bottom-Right Corner|

### Set Scale

After slicing, the size of the image border may not be consistent with the expected size, you can adjust the size of the image border by dragging the `scale` slider, the maximum value is `100%`, the minimum value is `0%`.

> The value greater than `100%` is not provided to avoid blurring or distortion when the image is enlarged.

### Border Style

In advanced mode, you can also set the border style, but unlike normal mode, here controls the display mode of the image border. The options include: 

- Stretch: Stretch the image to fill the border
- Repeat: Repeat the image to fill the border
- Round: Repeat the image, when the image cannot be repeated an integer number of times, enlarge or shrink the image according to the situation
- Space: Repeat the image, when the image cannot be repeated an integer number of times, use blank space to fill around the image (will not enlarge or shrink the image)

If you want the middle region of the border image to also be displayed in the background, you can check the `Display inner` option.

## **Reference**

<span id="ref1">[1]</span> [MDN border-style](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-style)
<span id="ref2">[2]</span> [MDN border-width](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-width)
<span id="ref3">[3]</span> [MDN border-color](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-color)
<span id="ref4">[4]</span> [MDN length unit px](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#px)
<span id="ref5">[5]</span> [MDN length unit pt](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref6">[6]</span> [MDN length unit em](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#em)
<span id="ref7">[7]</span> [MDN length unit vh](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref8">[8]</span> [MDN length unit vw](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref9">[9]</span> [MDN length](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length)
<span id="ref10">[10]</span> [MDN border-image](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-image)
<span id="ref11">[11]</span> [MDN border-image-slice](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-image-slice)