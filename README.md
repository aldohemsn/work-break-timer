# 职业活动与护眼计时器｜静态部署包

这是纯静态版本，不需要 Node.js、数据库、外部 API、CDN 或在线字体。包内已包含 HTML、CSS、JavaScript、图标、PWA 清单和离线缓存文件。

## 部署

将本目录内的全部文件原样上传到任意静态网站空间即可。请保持目录结构不变。可部署在域名根目录，也可部署在子目录。

适用平台包括 GitHub Pages、Cloudflare Pages、Netlify、Vercel 静态托管、Nginx、Apache、NAS 静态站点等。默认入口为 `index.html`。

## 本地运行

在本目录打开终端，任选一种方式启动本地静态服务器：

```bash
python -m http.server 8080
```

然后在 Chrome 打开 `http://localhost:8080`。

直接双击 `index.html` 也可使用基本计时功能，但 Chrome 出于安全限制，不会在 `file://` 页面启用 Service Worker、离线缓存和部分桌面通知能力。因此建议通过静态服务器访问。

## 离线与安装

首次通过 HTTPS 或 localhost 打开后，Service Worker 会缓存全部资源。之后断网仍可使用。Chrome 地址栏出现“安装”图标时，可安装为独立窗口应用。

## 字体说明

应用不请求 Google Fonts 或任何在线字体。中文界面使用操作系统自带字体栈（Windows 优先微软雅黑，macOS 优先苹方，并兼容常见思源/Noto 中文字体）；没有网络依赖，也不会因字体服务器不可用而失效。

## 数据与隐私

所有设置和每日完成轮次仅保存在当前浏览器的 `localStorage` 中，不上传到服务器。桌面通知须由用户在浏览器中主动授权。
