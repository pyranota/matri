# Matri - Universal Matrix Client
Based on Telegram Web A, packaged for Desktop, Android and IOS with Tauri

## Local setup

```sh
mv .env.example .env

bun i
```

Obtain API ID and API hash on [my.telegram.org](https://my.telegram.org) and populate the `.env` file.

## Dev mode

```sh
bun run dev
```

### Invoking API from console

Start your dev server and locate GramJS worker in console context.

All constructors and functions available in global `GramJs` variable.

Run `bun run gramjs:tl full` to get access to all available Telegram requests.

Example usage:
``` javascript
await invoke(new GramJs.help.GetAppConfig())
```

#### GitHub release

##### GitHub access token

In order to publish new release, you need to add GitHub access token to `.env`. Generate a GitHub access token by going to https://github.com/settings/tokens/new. The access token should have the repo scope/permission. Once you have the token, assign it to an environment variable:

```
# .env
GH_TOKEN="{YOUR_TOKEN_HERE}"
```

##### Publish settings

Publish configuration in `src/electron/config.yml` config file allows to set GitHub repository owner/name.

##### Release workflow

- Run `npm run electron:publish`, which will create new draft release and upload build artefacts to newly reated release. Version of created release will be the same as in `package.json`.
- Once you are done, publish the release. GitHub will tag the latest commit.

### Dependencies
* [GramJS](https://github.com/gram-js/gramjs) ([MIT License](https://github.com/gram-js/gramjs/blob/master/LICENSE))
* [pako](https://github.com/nodeca/pako) ([MIT License](https://github.com/nodeca/pako/blob/master/LICENSE))
* [cryptography](https://github.com/spalt08/cryptography) ([Apache License 2.0](https://github.com/spalt08/cryptography/blob/master/LICENSE))
* [emoji-data](https://github.com/iamcal/emoji-data) ([MIT License](https://github.com/iamcal/emoji-data/blob/master/LICENSE))
* [twemoji-parser](https://github.com/twitter/twemoji-parser) ([MIT License](https://github.com/twitter/twemoji-parser/blob/master/LICENSE.md))
* [rlottie](https://github.com/Samsung/rlottie) ([MIT License](https://github.com/Samsung/rlottie/blob/master/COPYING))
* [opus-recorder](https://github.com/chris-rudmin/opus-recorder) ([Various Licenses](https://github.com/chris-rudmin/opus-recorder/blob/master/LICENSE.md))
* [qr-code-styling](https://github.com/kozakdenys/qr-code-styling) ([MIT License](https://github.com/kozakdenys/qr-code-styling/blob/master/LICENSE))
* [croppie](https://github.com/Foliotek/Croppie) ([MIT License](https://github.com/Foliotek/Croppie/blob/master/LICENSE))
* [mp4box](https://github.com/gpac/mp4box.js) ([BSD-3-Clause license](https://github.com/gpac/mp4box.js/blob/master/LICENSE))
* [music-metadata-browser](https://github.com/Borewit/music-metadata-browser) ([MIT License](https://github.com/Borewit/music-metadata-browser/blob/master/LICENSE.txt))
* [lowlight](https://github.com/wooorm/lowlight) ([MIT License](https://github.com/wooorm/lowlight/blob/main/license))
* [idb-keyval](https://github.com/jakearchibald/idb-keyval) ([Apache License 2.0](https://github.com/jakearchibald/idb-keyval/blob/main/LICENCE))
* [fasttextweb](https://github.com/karmdesai/fastTextWeb)
* webp-wasm
* fastblur

## Bug reports and Suggestions
If you find an issue with this app, let Telegram know using the [Suggestions Platform](https://bugs.telegram.org/c/4002).
