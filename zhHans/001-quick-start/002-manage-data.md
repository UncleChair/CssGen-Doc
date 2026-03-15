---
id: manage-data
title: 数据管理
description: 管理编辑器中的样式数据
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

# 数据管理

在编辑器界面的右上角，您可以找到如下三个图标，他们分别用于：

- 同步配置
- 快捷键设置
- 项目设置

<!-- demo:css-gen-config-mock -->

## 同步配置

同步配置会基于云端和本地数据状态决定同步策略。如果您的本地数据比云端的新，则会自动将您的数据上传至云端，如果您的云端数据更新，则会有对话框帮助您决定是覆盖云端数据还是从将云端数据同步至本地。

## 快捷键设置

快捷键设置能帮助您自定义快捷键以提高您的编辑效率。配置将仅保存在本地，更换设备后需要重新设置。

### 本地保存

默认开启，按下 `Ctrl + S` 键即可将项目数据保存至本地缓存。

> 注意：如果您没有保存项目至本地或云端，关闭项目后数据将会丢失。

### 撤销

默认开启，按下 `Ctrl + Z` 键即可撤销上一步操作。

### 重做

默认开启，按下 `Ctrl + Shift + Z` 键即可重做上一步撤销的操作。

### 云端同步

默认关闭，按下 `Ctrl + Alt + S` 键即可触发同步配置检查，与按钮提供的功能一致。

## 项目设置

<!-- demo:css-data-check -->

项目设置能帮助您对项目进行一些基本操作。

<!-- demo:setting-list-mock -->

### 上传图片

上传图片能够上传本地或在线的图片至编辑器，上传完成后将会自动加载至编辑器供您选择使用。

### 导入 JSON

导入 JSON 能帮助您从 JSON 文件导入项目数据，导入完成后将会自动加载至编辑器并更新样式。

### 导出 JSON

导出 JSON 能帮助您将项目数据导出为 JSON 文件，导出完成后将会自动下载至您的本地文件夹，您可以随时导入该文件以恢复您的项目数据。

### 导出 CSS

导出 CSS 能帮助您将项目数据直接导出为 CSS 文件，导出完成后将会自动下载至您的本地文件夹。

### 预览并导出 CSS

预览并导出 CSS 功能会在导出前弹出预览窗口，您可以在此窗口中查看所有编辑的 CSS 样式，并决定是否导出。

<div style="margin-top: 48px; padding: 32px; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; text-align: center; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
  <div style="font-size: 36px; font-weight: bold; color: white; margin-bottom: 16px;">
    恭喜！🎉
  </div>
  <div style="font-size: 18px; color: rgba(255,255,255,0.95); line-height: 1.8; margin-bottom: 24px;">
    现在您已经成功完成了快速入门教程
  </div>
  <div style="display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;">
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      👉 前往 <a href="./page-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">界面指南</a> 了解编辑器布局
    </div>
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      🔧 前往 <a href="./component-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">组件指南</a> 了解各个组件的细节
    </div>
    <div style="background: rgba(255,255,255,0.2); backdrop-filter: blur(10px); padding: 16px 24px; border-radius: 8px; color: white; font-weight: 500; border: 1px solid rgba(255,255,255,0.3);">
      🚀 前往 <a href="./platform-guide" style="color: #ffd700; text-decoration: underline; font-weight: bold;">平台指南</a> 了解特定平台的配置与使用方法
    </div>
  </div>
</div>
