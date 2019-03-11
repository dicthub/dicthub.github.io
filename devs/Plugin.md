---
layout: devs 
title: Plugin
description: A quick tutorial of developing new plugins for DictHubExtension.
group: development
redirect_from:
- /devs/
- /docs/development/
- /docs/development/plugin
toc: false
---

<div class="alert alert-info" role="alert">
    This pae is under construction. Directly reaching <a href="mailto:app@dicthub.org">app@dicthub.org</a> would be more helpful :-)
</div>

## Create a new Plugin

DictHubExtension is designed to be extensible by plugins, to support translation/dictionary from a new source, a new plugin can be easily created and published. Below are the quick steps for creating an example plugin:

### Set up local development and testing environment

1. Checkout template [plugin-local-test](https://github.com/dicthub/plugin-local-test) to local:
```
git clone https://github.com/dicthub/plugin-local-test
```
2. Start an local http server to serve the plugin content, e.g. python built-in quick http server:
```
python3 -m http.server 7777
```
Confirm that `http://localhost:7777/index.json` and `http://localhost:7777/plugin-local-test.js` is accessible from browser.
3. Add local test repository url to config:<br>
Use <i class="fa fa-plus-square text-success"></i> and add `http://localhost:7777/index.json` to repository list.
Now **Local Test Plugin** should be listed in PluginList.
4. Select any text in a webpage, and trigger DictHub popup or overlay page, 
```
Echo Query
{"text":"query","from":"en","to":"zh-CN"}
Powered by Local Test
```
should be displayed on popup or overlay page.

### Pull translation data and render result

For plugins, the following framework/lib are pre-loaded and plugins can use:
* [jQuery](https://jquery.com/) (currently 3.3.1)
* [Kotlin](http://kotlinlang.org/) (currently 1.3.20)
* [Kotlinx.Html](https://github.com/Kotlin/kotlinx.html) (Currently 0.6.12)
* [Bootstrap](https://getbootstrap.com/) (Currently 4.3)

The following steps suggests the general way of creating logic of the plugin:
1. Find the url pattern from user query to source.<br>
E.g. if we're writing a plugin for wikipedia, for `Ninja` the url is `https://en.wikipedia.org/wiki/Ninja`
2. Load the source content html (or JSON)<br>
You could use `jQuery.ajax()`(or `get()`, `post()`) or raw `XMLHttpRequest` to fetch the content.
3. Parse the content to get the result plugin want to render for user<br>
E.g. for wikipedia, the first paragraph is usally the brief definition of the query, we could use
```
$(".mw-parser-output:first > p:first")
```
To extract the first paragraph content.
4. Render the result in a user-friendly way including:
* Since most of other translation results are using `Bootstrap` components, it's better to keep aligned with same style;
* Include the full source url for futher checking by user;
* When no such entry exists, show a message indicates no such query;
* When parse html failed, show a warning message and preferably a bug report link to the plugin repository

### Publish the plugin
T.B.D