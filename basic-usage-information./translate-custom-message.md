# Translate - Custom Message

## Translate - Custom Message <a id="page-title"></a>

**Important Note**

_The bot’s default prefix is !t \(or !translate\) - All commands must start with this prefix for the bot to process them. Bot must have proper permissions in all relevant channels for full functionality \(**read**, **write**, **react**, **mention**, **attachments**, **embed**\)._

_Users who wish to receive automatic translations in private must **enable DMs** via **server privacy settings**._

Translates a custom message entered by user.

## Command <a id="command"></a>

```text
> !t this: [msg]  
> !t this to [lang] from [lang]: [msg]
```

## Parameters <a id="parameters"></a>

* to **`[lang]`** - defaults to server default language
* to **`[lang, lang, ...]`** - translates to multiple languages
* from \[lang\] - defaults to automatic detection

## Examples <a id="examples"></a>

```text
> !t this: bonjour  
> !t this to spanish: hello world  
> !t this to arabic, hebrew: I love you  
> !t this to de from en: how are you?
```

