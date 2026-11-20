# 罗潾手册 PWA

## 发布前
将整个文件夹中的内容上传到一个支持 HTTPS 的静态网站托管服务（例如 GitHub Pages）。请保留 `index.html`、`manifest.webmanifest`、`service-worker.js` 和 `icons` 文件夹的相对位置。

## 手机安装
1. 用手机浏览器打开发布后的 HTTPS 网站。
2. Android Chrome：打开浏览器菜单，选择“安装应用”或“添加到主屏幕”。
3. iPhone Safari：点“分享”，选择“添加到主屏幕”。

## 更换桌面图标
PWA 桌面图标由 `manifest.webmanifest` 指向的图标文件决定。将你想用的方形图片分别准备为 192×192 和 512×512 PNG，替换 `icons/icon-192.png` 与 `icons/icon-512.png`，再重新发布网站。手机可以通过 GitHub 网页端上传/替换这两个文件。
在网页内部选择照片，不能可靠地改变已经安装到手机桌面的 PWA 图标；更换后可能需要移除旧快捷方式并重新添加。

## 本地内容
帖子、图片、视频和主页设置仍保存在当前浏览器的 IndexedDB/localStorage 中。它们不会自动同步到其他设备，也不会因为发布到 GitHub Pages 而变成所有访客共享的数据。离线网页外壳可缓存，但本地内容仍属于各设备自己的浏览器。
