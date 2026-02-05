---
id: manage-data
title: Manage Data
description: Manage the style data in the editor
order: 2
parent: quick-start
previous: edit-style
demos:
  - key: css-data-check
    component: CssDataCheck
  - key: css-gen-config-mock
    component: CssGenConfigMock
  - key: setting-list-mock
    component: SettingListMock
---

# Manage Data

In the upper right corner of the editor, you can find the following three icons, which are used for:

- Sync configuration
- Shortcut settings
- Project settings

<!-- demo:css-gen-config-mock -->

## Sync configuration

Sync configuration will decide the sync strategy based on the data status of the cloud and local. If your local data is newer than the cloud, it will automatically upload your data to the cloud. If your cloud data is updated, there will be a dialog box to help you decide whether to overwrite the cloud data or synchronize the cloud data to the local.

## Shortcut settings

Shortcut settings can help you customize the keyboard shortcuts to improve your editing efficiency. The configuration will only be saved locally and needs to be re-set after changing devices.

### Local save

Enabled by default, press the `Ctrl + S` key to save the project data to the local cache.

> Note: If you have not saved the project to the local or cloud, the data will be lost after closing the project.

### Undo

Enabled by default, press the `Ctrl + Z` key to undo the previous operation.

### Redo

Enabled by default, press the `Ctrl + Shift + Z` key to redo the previous undo operation.

> The undo and redo have maximum limit of 40 operations.

### Cloud sync

Disabled by default, press the `Ctrl + Alt + S` key to trigger the sync configuration check, the same as the function provided by the button.

## Project settings

<!-- demo:css-data-check -->

Project settings can help you perform some basic operations on the project.

<!-- demo:setting-list-mock -->

### Upload image

Upload image can upload local or online images to the editor, after uploading, it will be automatically loaded to the editor for you to select and use.

### Insert global CSS

This option will open the global CSS insertion dialog box. If you are familiar with CSS and want to use some advanced properties or writing styles, you can insert them here. The inserted CSS will not be managed by the editor, but will take effect as global styles.

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

Preview and Export CSS will pop up a preview dialog before exporting, you can view all the edited CSS styles in this dialog and decide operations.

<div style="margin-top: 48px; padding: 32px; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; text-align: center; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
  <div style="font-size: 36px; font-weight: bold; color: white; margin-bottom: 16px;">
    Congratulations! 🎉
  </div>
  <div style="font-size: 18px; color: rgba(255,255,255,0.95); line-height: 1.8; margin-bottom: 24px;">
    You have successfully completed the quick start tutorial
  </div>
  <div style="display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;">
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      👉 Go to <a href="./page-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">Page Guide</a> to learn about the editor layout
    </div>
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      🔧 Go to <a href="./component-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">Component Guide</a> to learn about the details of each component
    </div>
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      🚀 Go to <a href="./platform-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">Platform Guide</a> to learn about the configuration and usage of specific platforms
    </div>
  </div>
</div>
