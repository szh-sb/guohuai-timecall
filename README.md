# 国槐计划｜时空来电 3.5

初中课堂专用历史人物互动网站。十位人物的隐藏身份猜谜、常见问答即时判断、猜不出来时直接揭晓，并继续与同一人物对话。

## 当前发布状态（按文件核对）
- ✅ 已提交 `index.html`、`config.js` 与 GitHub Pages Actions 工作流。
- ⚠️ 原始李白/苏轼真人风格 WEBP 图像（`assets/` 下 8 张）尚未上传到 GitHub；网页提供内置古风 SVG 占位形象以避免破图。
- ⚠️ Cloudflare `worker.js` 尚未部署，网页中 AI 设置暂不能连接真正的 DeepSeek；离线问答、揭晓、人物介绍可以使用。
- 🔒 未在本仓库中保存任何真实 DeepSeek API Key。

## 发布为网址
GitHub 仓库 → **Settings → Pages → Build and deployment → Source: GitHub Actions**，保存后查看 **Actions → Publish Timecall to GitHub Pages** 的部署结果。

预计网址（仅启用 Pages 并部署成功后有效）：https://szh-sb.github.io/guohuai-timecall/

## 补齐原创人物素材
下载聊天中的 **时空来电 3.5 ZIP**，解压后打开 `assets/`，将 8 张 WEBP 图片上传到仓库同名 `assets/` 目录。这会自动替换内置占位形象。

## 启用真实 AI
GitHub Pages 不能安全地存放或调用 DeepSeek API。将 3.5 ZIP 内的 `worker.js` **单独部署**至 Cloudflare Workers，设置 `ALLOWED_ORIGIN=https://szh-sb.github.io`，为教师访问设置 `CLASSROOM_PIN` 并配置访问限制；然后由教师在网页临时填写 Worker URL 与 DeepSeek 密钥。不要把密钥上传至 GitHub。

网页口型和人物动作属于教学模拟，人物肖像、原声和对话都不是历史复原证据。
