# 参考设计转可交接 Demo

[English](README.md) · 中文

**把视觉参考转成可操作的界面，并交付设计依据、交互状态和开发说明。**

![参考设计转可交接 Demo](assets/hero.png)

## 得到什么

可运行 Demo、可追溯的设计取舍、样式变量、状态行为与接入边界。

[阅读完整 Skill](skills/reference-to-demo/SKILL.zh-CN.md) · [英文入口](skills/reference-to-demo/SKILL.md)

## 先看案例

Prism Pass 提供两种外观、可取消的本地选择、键盘操作及明确的接入事件。

[案例说明](skills/reference-to-demo/examples/prism-pass/brief.zh-CN.md) · [中文交互示例](skills/reference-to-demo/examples/prism-pass/index.zh-CN.html) · [English demo](skills/reference-to-demo/examples/prism-pass/index.html)

下载仓库后，在浏览器打开示例 HTML。GitHub 的文件预览显示源码，不直接运行 HTML。示例可离线使用，材料均为虚构。

## 安装

把下面的地址交给支持 GitHub Skill 安装的助手，安装整个 Skill 文件夹：

```text
https://github.com/Cynthiawongss/reference-to-demo/tree/main/skills/reference-to-demo
```

保留 `references/`、`examples/` 和存在时的 `scripts/`、`agents/` 子目录。`SKILL.md` 是英文默认入口，`SKILL.zh-CN.md` 是对应中文版。英文入口同样要求按用户指定语言交付。

也可以从 [v0.1.0 发布页](https://github.com/Cynthiawongss/reference-to-demo/releases/tag/v0.1.0) 下载英文或中文 Skill 安装包。两种版本选一种安装即可。

## 使用示例

```text
使用 $reference-to-demo，把这张卡片参考做成适合现有产品的可选择组件，附交互状态、设计取舍和开发交接说明。
```

## 验证

在仓库根目录执行：

```sh
npm install
npx playwright install chromium
node tools/check_browser.cjs
```

[验证范围与限制](validation/README.md)包含浏览器检查方法。Python 检查器仅需 Python 3.10+ 标准库。

## 范围

本地选择不等于服务端保存；小范围参考任务不自动扩大为整个产品重设计。
