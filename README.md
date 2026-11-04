# 待办清单 Todo App

一个纯前端实现的待办清单，单文件（`index.html`），无需构建、无需依赖，双击即可运行。

## 功能

- 添加 / 编辑（双击任务文字或按 Enter）/ 删除任务
- 勾选完成，完成的会被划线
- 三档优先级（高 / 中 / 低），点击圆点循环切换
- 筛选：全部 / 未完成 / 已完成
- 一键清除所有已完成任务
- 数据保存在浏览器 `localStorage`，刷新不丢
- 导出 / 导入 JSON 备份，换设备可迁移
- 深色模式：手动切换并记忆，首次访问跟随系统偏好

## 如何运行

直接双击 `index.html`，或在 VS Code 中右键选择「Open with Live Server」。

## 技术说明

原生 HTML + CSS + JavaScript，无框架、无构建步骤。

- 主题通过 CSS 变量 + `<html data-theme>` 切换，配色集中在 `:root` 与 `:root[data-theme="dark"]` 两处
- 列表渲染用 `document.createElement` 构建，避免拼接 HTML 字符串带来的注入风险
- 导入的 JSON 会做字段与类型校验，校验失败不会覆盖现有数据

## 目录

```
index.html    # 全部代码（结构 / 样式 / 逻辑）
.gitignore    # 忽略本地备份副本
```

## 作者

[Jia-J1a](https://github.com/Jia-J1a)