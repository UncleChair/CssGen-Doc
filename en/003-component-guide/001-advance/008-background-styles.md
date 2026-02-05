---
id: background-styles
title: Background
description: Set the background color or decorative image
parent: advance-component
previous: font-styles
next: position-styles
order: 8
demos:
  - key: background-editor
    title: Background Example
    component: BackgroundEditor
    sticky: true
    props:
      unique: true
---

# Background Style Component

_Fill the layer with color or add decorative images to make the layer more beautiful._

<!-- demo:background-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

## Set Background Color

Clicking the color block will pop up the color selector, you can use the color palette, color picker or color code to select the color.

The color code mode allows switching, currently supports:

- RGB(A)
- HSL(A)
- HEX(A)

## Add Background Image

After checking the `Add Picture` option, you can select the background image in the newly added picture list.

### Upload Image

The image needs to be uploaded through the upload image option in the project settings, or added directly by clicking the add button in the list. The image addition supports two modes:

- Local file: Upload local image
- Online image bed: Input the online image bed link and image name

After setting, the image will automatically appear in the optional list of the add button.

### List Functions

**Image Order and Layer**

When you add a new background image, it will be automatically added to the end of the image list. The image at the top of the list will be displayed at the top layer, and the image at the bottom will be displayed at the bottom layer. This means that if there are overlapping areas between multiple images, the image at the top will cover the image at the bottom.

**Preview and Selection**

After clicking the selected image in the image list, the detailed information and real-time preview of the image will be displayed in the preview area below the list. This allows you to easily view the effect of the currently selected image and make corresponding adjustments. You can also quickly preview the image information on the right side of each image.

**Lock Mode Switch**

The image list provides a lock/unlock function, you can switch between different editing modes by clicking the lock button at the top of the list: 

- Lock mode: You can only adjust the size and position of the image that has been set, and cannot delete or replace it.

- Unlock mode: In addition to the size and position, you can also delete or replace the image added to the list.

### Adjust Image

In the preview area, you can adjust the display mode of the image in detail, including: 

- **Horizontal Stretch**: Stretch the image horizontally to the background width
- **Vertical Stretch**: Stretch the image vertically to the background height
- **Scale**: Adjust the display size of the image, the maximum value is `100%`, the minimum value is `0%`
- **Horizontal Anchor**: Adjust the horizontal alignment anchor of the image, the optional values are `Left` , `Center` , `Right` , you can also input a number, the unit of the number mode is `%`
- **Vertical Anchor**: Adjust the vertical alignment anchor of the image, the optional values are `Top` , `Center` , `Bottom` , you can also input a number, the unit of the number mode is `%`
- **Horizontal Position**: Adjust the position of the image in the horizontal direction, the unit is `px`
- **Vertical Position**: Adjust the position of the image in the vertical direction, the unit is `px`
- **Repeat**: Set whether the image is repeated and the repeat mode

You can also enable the drag mode to directly drag the image to adjust the position, after enabling the drag mode, the layer will be fully highlighted and displayed at the layer level.