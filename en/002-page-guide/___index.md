---
id: page-guide
title: Page Guide
description: Learn about the editor layout and functionality
order: 1
demos:
  - key: message-type-selector
    component: MessageTypeSelectorDemo
  - key: message-preview
    component: MessagePreviewDemo
  - key: operation-list
    component: OperationListDemo
  - key: user-setting
    component: UserSettingDemo
next: editor-mode
---

# Editor Introduction

_After opening the editor for the first time, you will enter a simple guide to help you understand the functionality and region division, it is recommended to complete the guide first._

![Editor Interface](./static/editor.png)

The editor is mainly divided into three regions:

- System settings area: The upper right corner of the page is used to perform system settings and project data management
- Preview area: The left side of the page is used to preview the current style in real time
- Edit area: The right side of the page is used to edit the style

The content of the preview and edit areas will be different depending on the mode you selected.

## System settings area

You can manage the project data or perform system settings here.

### Tutorial replay

Tutorial replay can restart the guide tutorial, and will show a hint if there is new guide content.

### Sync configuration

Sync configuration will decide the sync strategy based on the data status of the cloud and local. If your local data is newer than the cloud, it will automatically upload your data to the cloud. If your cloud data is updated, there will be a dialog box to help you decide whether to overwrite the cloud data or synchronize the cloud data to the local.

> Sync configuration may overwrite your local settings, if you are concerned about data consistency, you can export JSON backup first.

### Theme switch

Theme switch can switch the theme color of the editor, support light and dark modes.

### Language setting

Language setting can set the interface language of the editor.

### Shortcut settings

Shortcut settings can open the custom shortcut settings dialog, you can set the shortcuts here.

> Some shortcuts such as `Ctrl + W` will be occupied by your browser default behavior (close tab), please note that these combinations cannot be set; if you need to use these combinations, please change your browser shortcuts first.

### Project settings

Project settings can expand the project related operation list, you can manage the project data here.

### Upload image

Upload image can open the image upload dialog, you can manage the image resources here.

You can upload local or online images to the editor here, after uploading, it will be automatically loaded to the editor for you to select and use.

> Upload or delete image operations will not be recorded in the undo and redo history, please be careful.

### Import JSON Config

Import JSON Config can help you import project data from a JSON file. After importing, it will be automatically loaded to the editor.

### Export JSON Config

Export JSON Config can help you export project data as a JSON file. After exporting, it will be automatically downloaded to your local folder, you can import it anytime to restore your project data.

### Import CSS

Import CSS can help you import any CSS file and convert it to a format that can be used by the editor. The imported CSS will clear the current styles and then be applied.

> CSS import cannot completely map all operations to the editor, some unsupported properties will be placed in the global CSS and take effect, and some will be inserted as `custom css` components into the layer.

### Export CSS

Export CSS can help you export project data directly as a CSS file. After exporting, it will be automatically downloaded to your local folder.

### Preview and Export CSS

Preview and Export CSS option will pop up a preview dialog before exporting, you can view all the edited CSS styles in this dialog and decide operations.

### Mode switch

Style editor provides two modes: editor mode and agent mode, the preview and edit area content will be different depending on the mode you selected, you can switch between them anytime.

- Editor mode: provides rich style editing functions, in this mode you will be able to adjust all available attributes and details. <a href="./editor-mode">Learn more</a>

- Agent mode: integrates the AI assistant editing mode, you can instruct the AI assistant to quickly adjust the style by inputting a prompt. <a href="./agent-mode">Learn more</a>

> Agent mode is still under development, if you have any questions or suggestions, please feel free to contact us.