# 晋江风小说工坊 · PWA

可安装到手机桌面的小说生成 / 书架 / 阅读工具。

## 用 GitHub Pages 部署

1. 新建 GitHub 仓库（例如 `novel-workshop`）
2. 把本压缩包内全部文件上传到仓库**根目录**（不要多包一层文件夹）
3. 仓库 Settings → Pages → Source 选 `Deploy from a branch` → Branch 选 `main` / `/ (root)` → Save
4. 等待一两分钟，访问：`https://你的用户名.github.io/仓库名/`

> 必须用 **HTTPS** 才能安装 PWA。GitHub Pages 自带 HTTPS。

## 用 Chrome 安装到手机桌面

### Android Chrome
1. 用 Chrome 打开部署后的网址
2. 右上角 ⋮ → **添加到主屏幕** / **安装应用**
3. 确认后主屏幕出现图标，点击即全屏打开（无浏览器地址栏）

### iPhone Safari（可选）
1. Safari 打开网址 → 分享 → **添加到主屏幕**

## 本地预览

PWA / Service Worker 需要通过 http(s) 访问，不要直接用 `file://` 打开。

```bash
npx serve .
# 或 python3 -m http.server 8080
```

## 文件说明

| 文件 | 作用 |
|------|------|
| index.html | 主应用 |
| manifest.json | PWA 清单 |
| sw.js | Service Worker（离线缓存页面壳） |
| icon-192.png / icon-512.png | 应用图标 |
| apple-touch-icon.png | iOS 图标 |

小说数据保存在浏览器 localStorage，清除站点数据会丢失，请及时「导出 TXT」。
