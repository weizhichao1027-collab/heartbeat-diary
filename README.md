# 心跳日记 / Pulse Diary 官方网站

心跳日记 **1.1.1 已于北京时间 2026-10-29 上架**。[App Store 下载](https://apps.apple.com/cn/app/id6761840824)。这是官网、技术支持、隐私政策和服务条款的静态发布目录，由 GitHub Pages 从公开仓库 `weizhichao1027-collab/heartbeat-diary` 的 `main` 根目录发布。

| 页面 | 简体中文 | English |
| --- | --- | --- |
| 官网 | [官网](https://weizhichao1027-collab.github.io/heartbeat-diary/) | [Overview](https://weizhichao1027-collab.github.io/heartbeat-diary/en/) |
| 技术支持 | [支持](https://weizhichao1027-collab.github.io/heartbeat-diary/support/) | [Support](https://weizhichao1027-collab.github.io/heartbeat-diary/en/support/) |
| 隐私政策 | [政策](https://weizhichao1027-collab.github.io/heartbeat-diary/privacy/) | [Privacy](https://weizhichao1027-collab.github.io/heartbeat-diary/en/privacy/) |
| 服务条款 | [条款](https://weizhichao1027-collab.github.io/heartbeat-diary/terms/) | [Terms](https://weizhichao1027-collab.github.io/heartbeat-diary/en/terms/) |

开发与支持：卫智超，281916057@qq.com。App Store 销售方：Shanghai Qishan Cultural Communication Co., Ltd.。App 备案：沪ICP备2026044636号-3A。

## 维护方式

本目录是可直接发布的静态产物，不依赖 Node、构建服务、访问统计或运行时 JavaScript。源内容与构建脚本在主 App 工程（不在公开网站仓库）中维护：

- `Scripts/site/zh/`、`Scripts/site/en/`：主页、支持页介绍、隐私与条款源内容。
- `Scripts/site/release.json`：版本、发布时刻、网站更新日期与客户端政策日期的唯一构建来源。
- `Scripts/site/llms.txt`：辅助事实导航源模板，与页面一起生成。
- `Scripts/site/support.json`：每种语言27条支持问答；同时生成可见正文和 FAQPage，避免两者不一致。
- `Scripts/build-site.py`：公共导航、页脚、元数据、JSON-LD、hreflang、sitemap 和 robots 副本。
- `Scripts/check-site.py`：链接、锚点、图片、SEO 与 FAQ 一致性验证。
- `Scripts/prepare-site-assets.py`：从主工程现有正式素材导出 WebP、触屏图标与社交分享图的 HTML 源。
- `Docs/SiteLaunch-2026-10-29.md`：主工程中的发布、回滚、验证与搜索收录交接。

从主工程执行 `python3 Scripts/build-site.py` 和 `python3 Scripts/check-site.py` 后，将 `Site/` 中的公开文件同步至网站仓库。不要只改生成后的 HTML 而不改源内容。发布前检查网站仓库上游变更；不强推，不同步整个 App 工程。

## SEO 与 GEO 边界

首页含可引用的版本更新与来源说明，支持问题提供永久锚点。8 页均含独立标题、描述、canonical、互返 hreflang、Open Graph、Twitter Card、App Store Smart Banner，以及与可见内容一致的结构化数据。没有虚构评分。`sitemap.xml` 列出所有公开页面及双语互返链接；`llms.txt` 仅作辅助事实导航。

项目站点位于 `/heartbeat-diary/` 子路径。搜索引擎只将主机根路径 `/robots.txt` 视为抓取规则；本目录的副本不能控制主机根规则。最近一次已验证的根 robots 返回 404，没有发现 robots 禁止抓取。可在经验证的 Google Search Console / Bing Webmaster Tools 站点中提交完整 sitemap URL；本次未宣称已完成账号验证或提交，也不保证收录、排名、富结果或 AI 引用。

网站隐私说明更新于 2026-10-29，App 1.1.1 中隐私与条款日期分别仍为 2026-10-13、2026-09-20。本轮为公开网站说明补充，未修改已发布客户端。

新版截图来自已保留的1.1.1原生商店素材（构建14捕获，演示记录），不是AI重绘，也不宣称是构建15运行捕获。源图路径、哈希和说明在主工程 `Scripts/site/asset-sources.json`。
