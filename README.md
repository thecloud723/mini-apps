# Mini Apps · 个人小工具集合

用于收纳独立的网页小工具（家庭学习、生活及日常效率），每个工具占用 `apps/` 下自己的子目录，互不干扰。

## 应用目录

| 应用 | 目录 | 访问入口 |
| --- | --- | --- |
| 🎙️ 语文听写播报器 | `apps/dictation/` | https://thecloud723.github.io/mini-apps/apps/dictation/ |

网站首页：https://thecloud723.github.io/mini-apps/

## GitHub Pages 部署

1. 创建公开仓库 `thecloud723/mini-apps`，默认分支 `main`。
2. 将本包内的 **文件与目录** 上传到仓库根目录，确保根目录是 `index.html`，而不是 `mini-apps/index.html`。
3. 在 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**，选择 `main` 和 `/(root)`，保存。
4. 等 GitHub Pages 部署完成，使用上面的 HTTPS 网址访问。

## 添加其他工具

- 新增 `apps/<tool-name>/index.html` 作为独立入口。
- 更新仓库根目录 `index.html`，加一张新工具卡片。
- 如果工具需要 PWA，请把 `manifest.webmanifest`、`sw.js` 和图标放在工具自己的目录里，并让 service worker 只管理当前工具的缓存。

## 数据与权限

- 听写题目保存在当前浏览器的 `localStorage`，更换手机或浏览器不会自动同步。
- 麦克风语音识别与屏幕常亮依赖浏览器能力、HTTPS、安全策略和用户授权。语音识别可能依赖浏览器厂商的在线服务。
- GitHub Pages 是公开网站。请不要向仓库提交学生个人信息或不打算公开的内容。