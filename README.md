# 一物一价 · GitHub Pages 部署包

纯静态版本：所有 CSS / JS 已内联进 `index.html`，无任何后端依赖。
数据仍保存在浏览器的 localStorage / IndexedDB 里（和你现在用的在线版一样）。

## 文件清单

| 文件 | 用途 |
|---|---|
| `index.html` | 整个应用（双击即可在电脑上打开使用） |
| `icon-180.png` | iPhone 添加到主屏幕的图标 |
| `icon-512.png` / `icon-1024.png` | 备用高清图标 |
| `.nojekyll` | GitHub Pages 配置，别删 |

## 部署到 GitHub Pages（网页操作，约 10 分钟）

1. 注册 / 登录 [github.com](https://github.com)；
2. 右上角 **+** → **New repository** → 名字随便取（例如 `cost-app`），选 **Public**（免费账号 Pages 必须公开仓库）→ **Create repository**；
3. 仓库页面点 **uploading an existing file**（或 Add file → Upload files）；
4. 把本目录下 **全部 5 个文件**（含 `.nojekyll`，它是隐藏文件，Mac 上用 Cmd+Shift+. 显示；也可以先打包成 zip 上传再解压——用 GitHub 网页端上传 zip 不会自动解压，推荐用下面第 7 步的命令行方式或 GitHub Desktop）拖进去；
   - 最简做法：只上传 `index.html` + 3 个图标 png 也能跑，`.nojekyll` 非必需；
5. 点 **Commit changes**；
6. 仓库 **Settings** → 左侧 **Pages** → **Source** 选 `Deploy from a branch`，Branch 选 `main` / `/ (root)` → **Save**；
7. 等 1~2 分钟，回到 Pages 页面顶部会出现地址：`https://你的用户名.github.io/cost-app/`；
8. iPhone Safari 打开这个地址 → 分享 → **添加到主屏幕**。

## 之后更新内容

改了代码需要重新部署：仓库页面打开 `index.html` → 铅笔图标编辑 → 粘贴新内容 → Commit，Pages 会自动更新（约 1 分钟）。

## 注意

- GitHub Pages 仓库有 1GB 限制、每月 100GB 流量，个人使用绰绰有余；
- 仓库如果是 Public，别人拿到地址也能访问页面（但看不到你的数据，数据只在你手机/浏览器里）；
- 想私有仓库 + Pages，需要 GitHub Pro（$4/月），个人使用没必要。
