---
id: font-styles
title: Font
description: Modify the text related style effects
parent: advance-component
previous: border-radius-styles
next: background-styles
order: 7
demos:
  - key: font-editor-simple-demo
    title: Font Example
    component: FontEditorSimpleDemo
    sticky: true
    props:
      unique: true
---

# Font Style Component

_Set the font, size, color, weight, etc. of the text, making the text more readable and beautiful._

<!-- demo:font-editor-simple-demo -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

The font style component affects all sub-layers contained in the layer, if you set the font style at the outermost layer, you don't need to set it for each layer separately.

## Set Font

If your browser supports getting the local font list, after clicking the Get Local Font List button, the font name will appear in the options below. You can also directly input the font name.

> The browser may need to authorize you to get permissions the first time you use this feature. Please follow the browser prompt to operate. If you do not agree to authorize, you need to open the relevant permissions in the browser yourself later.

## Adjust Style

The font style options include `No Style` and `Italic` two options, you can choose according to your needs.

## Select Color

Clicking the text color block will pop up the color selector, you can use the color palette, color picker or color code to select the color.

The color code mode allows switching, currently supports:

- RGB(A)
- HSL(A)
- HEX(A)

## Set Alignment

The text alignment options include `Left` , `Center` , `Right` , `Tiling` four options, you can choose according to your needs.

_Due to browser rules, `Tiling` will only take effect on non-last lines of multiple lines of text._

## Add Decoration

The text decoration options include `Underline` , `Overline` , `Line-through` three options, click to apply. The text decoration can be clicked multiple times to add multiple decorations, or click a single decoration option to remove the decoration.

## Adjust Weight

The text weight options include `Lighter` , `Light` , `Normal` , `Bold` , `Bolder` five options, the weight increases sequentially.

## Set Size

The text size number part can be input directly, the supported unit is only `px`<sup><a href="#ref1">[1]</a></sup>.

## Set Line Height

The text line height number part can be input directly, the supported unit is only `px`<sup><a href="#ref1">[1]</a></sup>. When you increase the text line height, the text size will also change, but it will not be automatically adjusted when you decrease it.

## Set Letter Spacing

The text letter spacing is used to adjust the distance between characters, the number part can be input directly, the supported unit is only `px`<sup><a href="#ref1">[1]</a></sup>.

## Set Stroke

The text stroke will add a unified stroke effect to the text, the stroke effect is composed of stroke width and stroke color, the stroke width number part can be input directly, the supported unit is only `px`<sup><a href="#ref1">[1]</a></sup>. The stroke color part can use the color palette, color picker or color code to select the color.

The color code mode allows switching, currently supports:

- RGB(A)
- HSL(A)
- HEX(A)

## **Reference**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#px)