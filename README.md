# XDI
[![Build status](https://ci.appveyor.com/api/projects/status/github/NCR76/xdi?branch=master&svg=true)](https://ci.appveyor.com/project/NCR76/xdi)

The Extended Dialogue Interface (XDI) is a community framework and engine modification for Fallout 4 that removes the hardcoded 4-option limit on dialogue and adds native support for any number of player dialogue options.

XDI enables mods to create new dialogue experiences that emphasize player choice and have dialogue options that truly reflect their intent.

This is an unofficial fork that incorporates changes from [Flenarn](https://www.nexusmods.com/users/33971250) and [Wolfmark](https://www.nexusmods.com/users/3224063).

[Original mod](https://www.nexusmods.com/fallout4/mods/27216) by [registrator2000](https://www.nexusmods.com/users/17152929).

## How to see prompts
This is a modified version that supports a new option named `bShowOriginalPrompt` (disabled by default). Edit `Data\MCM\Settings\XDI.ini` to add `bShowOriginalPrompt=1` in the `[DialogueMenu]` section to see the original prompts. If the file is missing then copy it from `Data\MCM\Config\XDI\settings.ini` to `Data\MCM\Settings\XDI.ini` and edit this copy. Use a better text editor than Notepad for this, like [Notepad++](https://notepad-plus-plus.org/), [EditPlus](https://www.editplus.com/), etc...

### Formatting
The `sShowOriginalPromptFormat` setting can be used to specify the format: `$prompt` will be replaced with the original prompt and `$text` will be replaced with the response. Example:

```
[DialogueMenu]
bShowOriginalPrompt=1
sShowOriginalPromptFormat=[ $prompt ] $text
```

Note: use `&#187;` for the &#187; character. The default format is:

```
[DialogueMenu]
bShowOriginalPrompt=1
sShowOriginalPromptFormat=$prompt &#187; $text
```

Note that a game restart is required whenever the `sShowOriginalPromptFormat` setting is changed.
