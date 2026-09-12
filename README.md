# AICom 官网（aicom-site）

AICom —— 本地设备 MCP 网关的官方网站。独立于应用主仓（[aicom-app](https://github.com/mengxiangrui1211/aicom-app)），
本仓库即 GitHub Pages 部署根。

## 本地预览

纯静态、零构建：

```bash
# 任选其一
python -m http.server 8080
npx serve .
```

浏览器打开 http://localhost:8080

## 目录结构

```
aicom-site/
├── index.html          # 首页（单页）
├── 404.html
├── robots.txt
├── assets/
│   ├── fonts/          # 字体自托管（不依赖 Google Fonts，国内直连可用）
│   ├── img/            # logo / favicon / OG 分享图 / 吉祥物 IP 素材
│   └── shots/          # 产品实拍截图（来自 aicom-app docs/04-素材说明，ASCII 命名）
└── README.md
```

## 发布流程

1. 本地提交并推送到 `main`
2. GitHub 仓库 Settings → Pages → Source 选 `main` 分支 / `(root)`
3. 约 1 分钟后生效：https://mengxiangrui1211.github.io/aicom-site/

## 内容同步约定

- **版本号**：index.html 内 `const APP_VERSION` 为单一来源，应用发新版后改这一处
- **下载链接**：指向 aicom-app Releases latest，无需随发版改动
- **截图**：应用界面大改后从 aicom-app 仓库重新拷贝并保持 ASCII 命名
