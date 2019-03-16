---
layout: docs
title: Introduction
description: Get started with DictHub, customize translation experice with the built-in powerful plugin framework.
group: getting-started
redirect_from:
  - "/docs/"
  - "/docs/getting-started/"
  - "/getting-started/"
toc: false
---

<div class="alert alert-info" role="alert">
Can't wait! Download and try first:
</div>

[![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png)](https://github.com/dicthub/DictHubExtension/releases/download/v1.0.1/chrome.crx)
[![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png)](https://addons.mozilla.org/en-US/firefox/addon/dicthub/)
[![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png)](https://www.microsoft.com/en-us/store/collections/EdgeExtensions/pc/c)

## Meet DictHub..

<i class="far fa-thumbs-up"></i>  **DictHub is designed for..**
* Save time for translation during web reading, without transiting to another page;
* Understand the word better than just simple translation
* See translation in multiple languages (e.g. native language + english)
* ...

<i class="far fa-thumbs-down"></i>  **DictHub is not great for..**
* Long text translation
* Whole webpage/file translation

## How does it work?

DictHub extension is built with to components:
* DictHub extension framework which listens user query event and passes to plugins
* DictHub plugins fetch web result of sources, convert result to html content and pass to extension to render.

<img src="{{ site.baseurl }}/assets/img/DictHubFlow.svg" class="mw-100" />

Long story short, DictHub does nothing more than fetching the translation webpage (e.g. GoogleTranslation) and render on same webpage.

The way DictHub shows translation is inspired by a great extension [Greasemonkey](https://en.wikipedia.org/wiki/Greasemonkey)

## Sounds cool! How to contribute?

DictHubExtension is an open source project licensed under [MIT license](https://github.com/dicthub/DictHubExtension/blob/master/LICENSE), plugins are mostly under GPLv3 or MIT license.

Contributions are greatly appreciated to turn your effort into impact!

## Next Step

See our [Install]({{ site.baseurl }}/docs/manual/install/) page for instructions and [Config]({{ site.baseurl }}/docs/manual/config/) page to personalize your preference.