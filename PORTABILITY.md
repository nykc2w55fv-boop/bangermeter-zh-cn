# Windows → macOS 迁移

- 当前环境为 Windows 上的 Chrome 或 Chromium。目标环境为 Mac Studio 上的 Chrome 或 Chromium。
- 两个平台都在 `chrome://extensions/` 开启开发者模式并加载 `extension/`，或者先解压本地安装包，再加载解压后的目录。扩展无需构建。
- 评分逻辑和配置在 `extension/scoring.js`、`extension/weights.js`，语言表在 `extension/i18n.js`。浏览器使用同一套 Manifest V3 接口。
- 简体中文版没有新增 Windows 专属脚本、绝对路径或运行依赖。中文字体优先使用系统字体，macOS 使用苹方，Windows 可使用微软雅黑。
- 上游商店打包脚本 `store-assets/make-package.ps1` 仍依赖上游维护者的 Windows 盘符。只需在 Chrome 本地安装时可直接加载扩展目录，无需执行该脚本。
- 迁移时复制扩展目录，在 Mac 上重新加载，刷新 X，再确认弹窗、评分徽标、草稿评分和语言设置。若更换扩展 ID 或 Chrome 配置文件，原扩展的本地历史与导入报告不会自动迁移。
- 2026-11-22 添加默认简体中文。两平台继续共用安装入口。Node.js 可运行 `node extension/run-tests.js`、`node store-assets/i18n-coverage.js --zh-CN` 和 `node store-assets/check-versions.js`。
- 2026-11-22 扩展内容脚本增加 X Pro（pro.x.com）匹配范围。两平台安装或更新后均需刷新已打开的 X Pro 页面。
- 2026-11-22 将运行文件和许可文件打包为 GitHub Release 附件。Windows 和 macOS 可用同一份 ZIP。本地源码的入口仍为 `extension/`。
