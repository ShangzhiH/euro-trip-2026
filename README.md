# 2026 国庆欧洲行 · GitHub Pages 中国兼容版

这个版本针对“GitHub Pages + 中国大陆查看”做了降依赖处理。

## 已处理
- 不再依赖 `unpkg` / Leaflet CDN。
- 不再依赖 OpenStreetMap 在线瓦片。
- 每日地图改为 **静态路线图**，核心动线可离线查看。
- 每个点位提供 **高德 / Apple Maps / Google Maps** 三个外部导航入口。
- PWA 核心页面、manifest、图标由 Service Worker 缓存。
- 中国图源景点图片优先保留；若个别在线图片加载失败，不影响主行程。
- iPhone：Safari → 分享 → 添加到主屏幕。

## GitHub Pages 部署
1. 新建 GitHub 仓库。
2. 把本目录所有文件上传到仓库根目录。
3. Settings → Pages。
4. Source 选择 `Deploy from a branch`。
5. Branch 选 `main` / root。
6. 等待 GitHub Pages 生成 HTTPS 地址。

## 中国大陆访问说明
- `github.io` 本身的网络可达性仍可能因网络环境波动。
- 这个版本已经去掉页面内部最容易被墙导致“空白”的 OSM/UNPKG 依赖。
- 若要进一步提高大陆稳定性，建议给 GitHub Pages 绑定自定义域名，并考虑国内 CDN / 镜像托管。
