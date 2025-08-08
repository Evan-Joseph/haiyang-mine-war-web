# 海阳地雷战 · 沉浸式网页

单页静态网站，基于原生 HTML/CSS/JavaScript，聚焦海阳地雷战的沉浸式学习体验。

## 功能

- 背景音乐（仓库内 `bgm.mp3`）
	- 播放/暂停、音量/静音
	- 朗读期间自动压低 BGM（ducking）
	- 预加载并在就绪时提示状态
- 历史声音再现
	- 优先播放仓库内 `history-voice.mp3`
	- 不可用时回退为浏览器 TTS 朗读页面文案
	- 预加载并在就绪/失败时提示状态
- AI 战争诗歌生成与朗读（Web Speech API）
- 历史记忆卡片与地雷类型切换
- 团队信息弹出卡片
- 可访问性与 SEO 增强：aria-live、键盘可达性、OG 元信息、404/robots/sitemap

## 使用

- 本地预览：双击打开 `地雷战网页.html` 即可。
- 替换音频：将根目录下的 `bgm.mp3`、`history-voice.mp3` 替换为同名文件即可生效。
- 线上部署（GitHub Pages，免费）
	- 设置 Pages 来源为 main 分支/根目录；无需 Actions/CI。
	- 仓库 Settings > Pages 查看访问地址。

## 文件结构（节选）

- `地雷战网页.html`：主页面与脚本样式
- `index.html`：重定向到主页面
- `bgm.mp3`：背景音乐
- `history-voice.mp3`：历史声音音频
- `404.html`、`robots.txt`、`sitemap.xml`：站点辅助文件
- `.nojekyll`：禁用 Jekyll 处理

## 更新日志

- 2025-08-08 ff41d77 移除音频上传控件；统一使用仓库内音频并预加载；就绪事件提示；优化历史声音与 BGM 逻辑
- 2025-08-08 b729a47 BGM 与历史声音接线：重命名为 bgm.mp3 与 history-voice.mp3；默认改用本地 BGM；历史声音优先本地，失败回退 TTS；修复脚本语法
- 2025-08-08 228ca28 P0 可访问性与音频体验：新增 SEO 元信息、aria-live、音量/静音控制、朗读期间自动压低 BGM、404/robots/sitemap；增强键盘可达性
- 2025-08-08 cb2a3ef 调整部署：移除 Actions，改用 Pages 从分支部署
- 2025-08-08 8284a7a 初始化：导入原始版网页与部署配置

## 迭代约定

- 后续每次迭代请同步更新本文档的功能说明与“更新日志”。
- 提交信息统一使用中文，简洁明确。
