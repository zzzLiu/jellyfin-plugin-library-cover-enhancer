[English](README.md)

# Jellyfin 媒体库封面增强

这个插件用来重新生成 Jellyfin 首页上的**媒体库**拼图封面，并自定义封面上的文字和样式。

可以调整标题的字号、位置、粗细，以及底部渐变。字体可以使用 Jellyfin 的系统匹配、插件自带的 MiSans，或你指定的 `.ttf` / `.otf` 文件。

影片、剧集和其他**条目**的海报与刮削数据保持不变。

英文名：Jellyfin Library Cover Enhancer。

## 效果图

![我的媒体中的电影与剧集媒体库卡片，拼图封面上带标题文字](docs/screenshots/cover-enhancer-movies.png)

我的媒体：电影和剧集两张媒体库卡片，拼图封面上带标题文字。

## 兼容性

- Jellyfin **12.2**（含上报 ABI `12.2.0.0` 的 nyanmisaka 构建）
- `targetAbi`：`12.2.0.0`
- 插件 id：`8b3d6f12-9c44-4e2b-b8c1-7a5f2e143990`
- 程序集：`Jellyfin.Plugin.FolderCoverEnhancer.dll`（与 1.0.x 相同）
- 配置：`plugins/configurations/Jellyfin.Plugin.FolderCoverEnhancer.xml`

## 用插件仓库安装

1. Jellyfin：**控制台 → 插件 → 仓库 → 添加**
2. 名称随意，地址填：

   `https://raw.githubusercontent.com/zzzLiu/jellyfin-plugin-library-cover-enhancer/main/manifest.json`

3. 在目录安装 **Jellyfin Library Cover Enhancer**，然后重启。

## 手动安装

从 [Releases](https://github.com/zzzLiu/jellyfin-plugin-library-cover-enhancer/releases) 下载 `jellyfin-library-cover-enhancer_1.1.4.0.zip`。

```bash
mkdir -p /config/plugins/LibraryCoverEnhancer_1.1.4.0
unzip jellyfin-library-cover-enhancer_1.1.4.0.zip -d /config/plugins/LibraryCoverEnhancer_1.1.4.0
```

zip 根目录需包含：

- `Jellyfin.Plugin.FolderCoverEnhancer.dll`
- `font.ttf`
- `meta.json`

重启 Jellyfin。

## 使用

打开 **控制台 → 插件 → Jellyfin Library Cover Enhancer**（仪表盘服务器菜单也有同一页）。

调预览、保存，再重建一个或全部媒体库封面。重建后刷新首页。

配置页默认英文；当前用户显示语言为 `zh-*` 时用简体中文。已安装插件名和菜单同样跟 `Accept-Language`。

## 字体

`font.ttf` 是 MiSans。再分发前请自行确认字体许可。本项目不声明、也不授予字体许可。

## 支持 / 捐赠

如果这个插件对你有帮助，可以在 [Ko-fi](https://ko-fi.com/zzzliu) 请我喝杯咖啡：

[![Buy me a coffee](docs/donate/ko-fi-button.png)](https://ko-fi.com/zzzliu)

国内用户可以扫描下方微信赞赏码：

<img src="docs/donate/wechat-appreciate.jpg" alt="微信赞赏码" width="220" />

## 许可证

插件代码为 MIT，见 [LICENSE](LICENSE)。自带字体另论，见上。

## 更新说明

见 [RELEASE_NOTES.md](RELEASE_NOTES.md)。
