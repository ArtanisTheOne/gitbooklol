# Translate - Channel Automatic

**Important Note**

_The bot’s default prefix is !t \(or !translate\) - All commands must start with this prefix for the bot to process them. Bot must have proper permissions in all relevant channels for full functionality \(**read**, **write**, **react**, **mention**, **attachments**, **embed**\)._

_Users who wish to receive automatic translations in private must **enable DMs** via **server privacy settings**._

Automatically translates any new messages in the current channel and forwards them to you. Admins/mods can set forwarding to same channel, other channels or other users in the server. Messages in forwarded channels will also be sent back to origin\*.

## Command <a id="command"></a>

```text
!translate channel from [lang] to [lang] for [dest]
```

## Parameters <a id="parameters"></a>

* for **`[dest]`** _\(optional\)_  Forwarding destination where the translated messages will be sent, defaults to “me” - translations sent via direct/private messages between you and the bot. Admins/mods can use discord mentions as forward destination with possibility to set multiple destinations at once. See examples below.
* to **`[lang]`** _\(optional\)_  The language to translate to, defaults to server default language.
* from **`[lang]`** _\(optional\)_  The language to translate from.

## Examples <a id="examples"></a>

Using full language names

```text
> !translate channel from [english] to [spanish]
```

Using language short codes

```text
> !translate channel from [en] to [es]
```

Assigning a user as the target for translations

```text
> !translate channel from [english] to [spanish] for [me]
```

### Server Admins/Mods <a id="server-adminsmods"></a>

Send translations to same channel

```text
> !translate channel from [english] to [spanish] for [#SameChannelMention]
```

Send translations to another channel in server

```text
> !translate channel from [english] to [spanish] for [#OtherChannelMention]
```

Send translations to another user in server

```text
> !translate channel from [english] to [spanish] for [@UserMention]
```

Send translations to multiple channels/users in server at once

```text
> !translate channel from [english] to [spanish] for [#Channel1], [#Channel2], [@User1], [@User2]
```

### Stopping <a id="stopping"></a>

To stop an automatic translation task, simply go the original channel and use the stop command:

```text
> !translate stop  
> !translate stop for [me]
```

### Admins/Mods <a id="adminsmods"></a>

Stop all automatic translations

```text
> !translate stop for [all]
```

Stop all automatic translations for specific channel in server

```text
> !translate stop for [#ForwardChannelMention]
```

Stop all automatic translations for specific user in server

```text
> !translate stop for [@UserMention]
```

_Help command for stop: `!translate help stop`_

### Notes <a id="notes"></a>

_Help command for automatic translation: !translate help auto._

Values wrapped in brackets **`[ ]`** mean user input. **`[lang]`** values can be language names in English, native language names or ISO 639-1 codes. For example, **`german`** **`de`** and **`deutsch`** will all work the same.

Messages by bots are ignored.

Command messages are also ignored.

If you have a lot of users speaking a different language then it is advised you create a special public channel for them as a destination instead of having each one receive translated messages in private.

