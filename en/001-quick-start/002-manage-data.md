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
- Manage images
- Project settings

<!-- demo:css-gen-config-mock -->

## Sync configuration

Sync configuration will decide the sync strategy based on the data status of the cloud and local. If your local data is newer than the cloud, it will automatically upload your data to the cloud. If your cloud data is updated, there will be a dialog to help you decide whether to overwrite the cloud data or synchronize the cloud data to the local.

## Manage images

Manage images helps you manage image resources within the project. You can upload, delete, and preview images here.

## Project settings

<!-- demo:css-data-check -->

Project settings helps you perform some basic operations on the project.

<!-- demo:setting-list-mock -->

### Shortcut settings

Shortcut settings helps you customize keyboard shortcuts to improve your editing efficiency. The configuration is saved locally only; you need to set it again after switching devices.

- **Local save**: Enabled by default. Press `Ctrl + S` to save the project data to the local cache.

> Note: If you have not saved the project to the local or cloud, the data will be lost after closing the project.

- **Undo**: Enabled by default. Press `Ctrl + Z` to undo the previous operation.

- **Redo**: Enabled by default. Press `Ctrl + Shift + Z` to redo the previous undo operation.

> Undo and redo can record at most 40 operations.

- **Cloud sync**: Disabled by default. Press `Ctrl + Alt + S` to trigger the sync configuration check, same as the function provided by the button.

> Some shortcuts such as `Ctrl + W` are reserved by your browser (e.g. close tab). Such key combinations cannot be set; if you need them, change your browser shortcuts first.

### Insert global CSS

This option opens the global CSS insertion dialog. If you are familiar with CSS and want to use more advanced properties or syntax, you can insert them here. The inserted CSS will not be managed by the editor but will take effect as global styles.

### Import...

Import includes import config and import local CSS. You can choose what to import here.

> CSS import cannot fully map all operations to the editor. Some unsupported properties will be applied in global CSS, and some will be inserted as `custom code` components into the layer.

### Export...

Export includes export config, export local CSS, and export online CSS link. You can choose what to export here.

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
