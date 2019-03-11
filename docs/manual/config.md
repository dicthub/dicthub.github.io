---
layout: docs
title: Config
description: Config DictHub to customize your translation preference.
group: manual
redirect_from:
  - "/docs/config/"
toc: false
---

## Translation Settings
* `Preferred Language`<br>
  Set the default translation target language, usually the native language should be selected here.
* `Automatically detect language from query input`<br>
  If selected, DictHub will try to infer the language of the selected text (Currently by bing translation). Otherwise, language of the current webpage is used.<br>
  Mostly this option is suggested to be selected; there is some known case that the selected text can be valid in multiple languages, if the auto detection is causing less efficiency, this option can be turned off.
* `Max Translation Result`<br>
  Set the maximum translation results for the query. If enabled plugins are more than this value, plugins with higher priority is picked.

## Plugin Repository List
Config the plugin repository to load plugins. 
Plugin Repository is an index of plugins content with id, name, version and description.
* Click <i class="fa fa-minus-square text-danger"></i> to delete the repository entry
* Click <i class="fa fa-plus-square text-success"></i> to add new repository entry

## Plugin Settings
Plugins are loaded from the Repository List
* **Enable/Disable Plugin**: Use the switch right of the plugin line to enable/disable plugins<br>
  When plugin is enabled, plugin content is downloaded locally to speed up translation.
* **Update Plugin**: When plugin updates available, `Update` button is displayed.
* **Change Plugin Order**: Drag the plugin entry line to change plugin priority

## Advanced Settings
* `Edit Settings directly`<br>
  This enables advanced user to directly update stored preference.
* `Send anonymous usage data via Google Analytics to help improve this extension.`<br>
  Share usage information to Google Analysis, the data will be used to improve the extension only. Data sent is
  * Translation from/to language
  * Plugin stats: Success vs Failure
