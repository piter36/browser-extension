# ![FoxyProxy](/src/image/icon.svg) FoxyProxy Browser Extension

[![license](https://img.shields.io/github/license/foxyproxy/browser-extension.svg)](https://github.com/foxyproxy/browser-extension/blob/master/LICENSE) 
![GitHub repo size](https://img.shields.io/github/repo-size/foxyproxy/browser-extension)


Version 8.0+  
Browser extension source code for *Firefox*, *Chrome*, and other Chromium-based browsers like *Chromium*, *Brave* and *Edge*

FoxyProxy is being updated for manifest V3.
- Chrome minimum version 108 (released 2022-11-29)
- Firefox minimum version 93 (released 2021-10-05)
- Firefox for Android minimum version 113 (manifest) (API minimum 102)

Please post all feature requests to the [issues](https://github.com/foxyproxy/browser-extension/issues).


- [About](https://foxyproxy.github.io/browser-extension/src/content/about.html)
- [Help](https://foxyproxy.github.io/browser-extension/src/content/help.html)


## Versions

### Firefox
- [![Mozilla Add-on](https://img.shields.io/amo/v/foxyproxy-standard.svg)](https://addons.mozilla.org/firefox/addon/foxyproxy-standard/) [FoxyProxy Standard](https://addons.mozilla.org/firefox/addon/foxyproxy-standard/)
- [![Mozilla Add-on](https://img.shields.io/amo/v/foxyproxy-basic.svg)](https://addons.mozilla.org/firefox/addon/foxyproxy-basic/) [FoxyProxy Basic](https://addons.mozilla.org/firefox/addon/foxyproxy-basic/) 🆕
- Source Code: [Firefox Extension 7.5.1](https://github.com/foxyproxy/firefox-extension/)


#### Chrome
- [![Chrome Web Store](https://img.shields.io/chrome-web-store/v/gcknhkkoolaabfmlnjonogaaifnjlfnp.svg)](https://chrome.google.com/webstore/detail/foxyproxy-standard/gcknhkkoolaabfmlnjonogaaifnjlfnp) [FoxyProxy Standard](https://chrome.google.com/webstore/detail/foxyproxy-standard/gcknhkkoolaabfmlnjonogaaifnjlfnp)
- [![Chrome Web Store](https://img.shields.io/chrome-web-store/v/dookpfaalaaappcdneeahomimbllocnb.svg)](https://chrome.google.com/webstore/detail/foxyproxy-basic/dookpfaalaaappcdneeahomimbllocnb) [FoxyProxy Basic](https://chrome.google.com/webstore/detail/foxyproxy-basic/dookpfaalaaappcdneeahomimbllocnb)
- Source Code: [Chrome Extension 3.0.7.1](https://github.com/foxyproxy/Foxyproxy_Chrome)


## Installation Guide (for testing)
- Backup your FoxyProxy settings
- Download repo (or use `git`)
  - [browser-extension](https://github.com/foxyproxy/browser-extension) -> Code (green button) -> Download ZIP
  - Unzip the downloaded file
- **Firefox** *(Nightly/Beta/Developer Edition)*
  - Rename `manifest-firefox.json` in `src` folder to `manifest.json`
  - Go to `about:debugging#/runtime/this-firefox`
  - Click "Load Temporary Add-on..."
  - Select above `manifest.json`
- **Chrome**
  - Rename `manifest-chrome.json` in `src` folder to `manifest.json`
  - Go to `chrome://extensions/`
  - Enable Developer Mode (top right)
  - Click "Load Unpacked"
  - Select above `manifest.json` (or `src` folder)

- **Firefox for Android**  
  You can try installing FoxyProxy Basic v8.0
  - [Expanded extension support in Firefox for Android Nightly](https://blog.mozilla.org/addons/2020/09/29/expanded-extension-support-in-firefox-for-android-nightly/)
  - [How to Install Any Add-on in Firefox for Android](https://www.maketecheasier.com/install-addon-firefox-android/)

## Building for Distribution
- copy the appropriate manifest-xxx.json file to manifest.json; e.g. `mv manifest-chrome.json manifest.json`
- zip using [grunt](https://stackoverflow.com/questions/15703598/how-to-install-grunt-and-how-to-build-script-with-it), which requires npm and node. Run `grunt` in top-level directory. The add-on is packaged into `target.zip`. Alternatively, zip the `src` directory into the top of an archive and exclude a bunch of stuff manually.
