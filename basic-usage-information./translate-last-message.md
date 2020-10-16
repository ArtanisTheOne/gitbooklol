# Translate - Last Message

## Translate - Last Message <a id="page-title"></a>

**Important Note**

_The bot’s default prefix is !t \(or !translate\) - All commands must start with this prefix for the bot to process them. Bot must have proper permissions in all relevant channels for full functionality \(**read**, **write**, **react**, **mention**, **attachments**, **embed**\)._

_Users who wish to receive automatic translations in private must **enable DMs** via **server privacy settings**._

Translates last message chain\(s\) in channel.  
 A chain is a collection of messages by the same author, to keep things simple.

## Commands <a id="commands"></a>

```text
> !t last
> !t last [n] to [lang] from [lang]
```

## Parameters <a id="parameters"></a>

* `to [lang]` - defaults to server default language
* `to [lang, lang, ...]` - translates to multiple languages
* `from [lang]` - defaults to automatic detection
* `[n]` - number of chains to translate, default is 1
* `[-n]` - negative number means only one chain is translated

## Examples <a id="examples"></a>

```text
> !t last 2
> !t last to english  
> !t last to english, german, french
> !t last -6 to english from german
```

