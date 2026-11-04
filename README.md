# 国槐计划｜时空来电 3.5

面向初中课堂的历史人物 AI 互动实验室。学生通过“是 / 不是 / 不确定”提问猜身份；猜对或点击“一键揭晓”后，与同一历史人物进行模拟通话。

## 功能
- 十位历史人物的身份猜谜、教学资料与揭晓
- 常见问题即时判断，复杂提问可接入 DeepSeek 的 `/api/guess`
- 文字交流、可选语音朗读、口型模拟、人物动作与教师演示
- GitHub Pages 提供静态页面；Cloudflare Worker 转发 DeepSeek 请求

## 打开网站
在仓库 Settings → Pages 中，将发布来源设为 **Deploy from a branch**，选择 `main`、`/(root)` 并保存。
地址通常为 https://szh-sb.github.io/guohuai-timecall/ 。

## 云端 AI
GitHub Pages 不运行后端。将 `worker.js` 部署到 Cloudflare Workers，设置 `ALLOWED_ORIGIN=https://szh-sb.github.io`，课堂中由教师在网页设置界面临时填写自己的 API Key 与 Worker URL。**不要将任何密钥上传到本仓库。**

> 本项目的历史人物外观、语言和声音均为教学情景模拟，不能当作真实史料。未接入云端时也可以体验离线猜谜与预设对话。
