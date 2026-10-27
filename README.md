[中文说明](README.zh-CN.md)

# Jellyfin Library Cover Enhancer

Rebuilds Jellyfin **library** collage covers. Adjust title size, placement, weight, and a bottom gradient. Fonts can come from Jellyfin’s system matching, the bundled MiSans file, or a `.ttf` / `.otf` path you choose.

Movie, episode, and other **item** posters and metadata are left unchanged.

Chinese UI name: **Jellyfin 媒体库封面增强**.

## Screenshots

![My Media showing Movies and Series library cards with title overlays on the collage covers](docs/screenshots/cover-enhancer-movies.png)

My Media: Movies and Series library cards, with title overlays on the collage covers.

## Compatibility

- Jellyfin **12.2** (including nyanmisaka builds that report ABI `12.2.0.0`)
- `targetAbi`: `12.2.0.0`
- Plugin id: `8b3d6f12-9c44-4e2b-b8c1-7a5f2e143990`
- Assembly: `Jellyfin.Plugin.FolderCoverEnhancer.dll` (name unchanged from 1.0.x)
- Settings: `plugins/configurations/Jellyfin.Plugin.FolderCoverEnhancer.xml`

## Install from a plugin repository

1. In Jellyfin: **Dashboard → Plugins → Repositories → Add**
2. Name it anything you like. URL:

   `https://raw.githubusercontent.com/zzzLiu/jellyfin-plugin-library-cover-enhancer/main/manifest.json`

3. Install **Jellyfin Library Cover Enhancer** from the catalog, then restart Jellyfin.

## Manual install

Download `jellyfin-library-cover-enhancer_1.1.4.0.zip` from [Releases](https://github.com/zzzLiu/jellyfin-plugin-library-cover-enhancer/releases).

```bash
mkdir -p /config/plugins/LibraryCoverEnhancer_1.1.4.0
unzip jellyfin-library-cover-enhancer_1.1.4.0.zip -d /config/plugins/LibraryCoverEnhancer_1.1.4.0
```

The zip root must contain:

- `Jellyfin.Plugin.FolderCoverEnhancer.dll`
- `font.ttf`
- `meta.json`

Restart Jellyfin.

## Use

Open **Dashboard → Plugins → Jellyfin Library Cover Enhancer** (also in the server section of the dashboard menu).

Adjust the preview, save, then rebuild one library or all libraries. Refresh the home page after rebuilding.

The configuration page is English. It switches to Simplified Chinese when the signed-in user’s display language is `zh-*`. The installed plugin name and menu label follow `Accept-Language` the same way.

## Font

`font.ttf` is MiSans. Confirm that font’s license yourself before you redistribute the file. This project does not state or grant a font license.

## Support

If this plugin is useful, you can buy me a coffee on [Ko-fi](https://ko-fi.com/zzzliu):

[![Buy me a coffee](docs/donate/ko-fi-button.png)](https://ko-fi.com/zzzliu)

Users in China can scan the WeChat Appreciate (赞赏) QR code:

<img src="docs/donate/wechat-appreciate.jpg" alt="WeChat Appreciate QR code" width="220" />

## License

MIT for the plugin code. See [LICENSE](LICENSE). The bundled font is separate — see above.

## Changelog

See [RELEASE_NOTES.md](RELEASE_NOTES.md).
