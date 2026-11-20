# Validation / 验证说明

Checked on 2026-11-20 against this standalone repository.

- Browser: 4 checks passed (English and Chinese, 1280×900 and 390×844).
- External HTTP(S) requests were blocked; no external requests, JavaScript exceptions, or horizontal overflow occurred.
- [Browser evidence](../output/browser/results.json) lists the exercised interactions and screenshots.
- Exercised finish changes, selection/reversal, integration events, keyboard activation, reduced motion, and reload reset.

## Reproduce

Browser checks require Node.js 20+:

```sh
npm install
npx playwright install chromium
npm run check:browser
```

For a separately installed Chromium-compatible browser, set `PLAYWRIGHT_CHROMIUM_EXECUTABLE` to its executable. The local run used Chrome and Playwright 1.62.1. Results and screenshots are saved to `output/browser/`.

## Limits / 限制

These checks cover bundled synthetic examples, not independent agent trials on new user materials. They do not establish automatic invocation accuracy, user comprehension, a complete accessibility audit, or cross-browser compatibility.

本次检查覆盖拆分后的独立仓库：中英文、桌面和手机共 4 组交互页面。检查期间阻断外网；没有外部请求、JavaScript 异常或横向溢出。没有测试新用户材料上的独立任务表现、自动调用准确率或学习／理解效果。

Local selection is not a saved server response. The workflow does not expand a small reference task into a full redesign.

本地选择不等于服务端保存；小范围参考任务不自动扩大为整个产品重设计。

[Package checks](package-checks.txt): both instruction variants, local Markdown links, approved source and cover equality passed. The Chinese mobile screenshot was visually inspected; no clipping or unreadable overlap was observed.
