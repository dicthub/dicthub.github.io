---
layout: docs
title: Install
description: Install pre-packaged version from official extension store or try latest version from source
group: manual
redirect_from:
  - "/manual/install/"
toc: false
---

## Stable

* [<i class="fab fa-firefox"></i> Firefox Add-ons Store](https://addons.mozilla.org/en-US/firefox/addon/dicthub/)
* [<i class="fab fa-chrome"></i> Chrome Web Store](https://chrome.google.com/webstore/detail/dicthub/cibocdpeaeganigafnnofchcliihpchn)

## Development

* [<i class="fab fa-firefox"></i> Firefox Beta release](https://github.com/dicthub/DictHubExtension/releases/download/v1.0.1/firefox.zip)
* [<i class="fab fa-chrome"></i> Chrome Beta release](https://github.com/dicthub/DictHubExtension/releases/download/v1.0.1/chrome.crx)

## From source

1. Checkout repository to local:
```
git clone https://github.com/dicthub/DictHubExtension.git
```

2. Run gradle build to get extension:
```
./gradlew build
```
```
gradlew.bat build
```
Artifacts are under `build` directory

3. Load unpackaged extension
  * [Chrome instructions](https://developer.chrome.com/extensions/getstarted#unpacked)
  * [Firefox instructions](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Temporary_Installation_in_Firefox)