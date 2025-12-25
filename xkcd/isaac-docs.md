# **Isaac's documentation**

Isaac is your friendly neighbourhood bot and hangs out in several channels on Slashnet. This is his full user documentation.

Isaac's canonical pronouns are he, they or it. He's fine with all of them. :)

<br>

## Bot admins

The bot administrators have access to some special maintenance commands for Isaac. If you have any questions about the bot, please ask them.

The bot admin for Isaac on Slashnet is **CO2**.

<br>

## Title resolver

Isaac resolves titles of webpages. It's simple: Just use a link starting with `http://` or `https://` in any channel message and Isaac will do his best to find the title of that webpage and print it in channel.

This functionality does not work in private messages.

<br>

## Wayback machine link replacer (for Bucket)

Use the command `!wayback` followed by either a full bucket factoid or a simple link to have Isaac look for a replacement URL in the Wayback Machine and generate a Bucket substitution syntax for you.

Since Isaac is not allowed in #xkcd, this command works in PMs too. Please don't abuse it - we don't want to overload the Wayback Machine which is run by the heroes of archive.org

Example with a full factoid:

```
<CO2> !wayback cute is http://i.imgur.com/zvkn8.jpg
<Isaac> Archived URL found: http://web.archive.org/web/20250818151628/https://i.imgur.com/zvkn8.jpg. Here is how to update it in bucket:
<Isaac> Bucket: cute =~ s,http://i.imgur.com/zvkn8.jpg,http://web.archive.org/web/20250818151628/https://i.imgur.com/zvkn8.jpg,
```

Simply copy that last line into #xkcd and you will fix the Bucket link.

Note: This functionality is new as of December 2025, please message CO2 if you discover bugs.

Note 2: In testing I noticed the archive.org API sometimes times out internally. In that case, Isaac will report that no URL was found. If that happens - please check archive.org manually. It doesn't mean no URL exists.

<br>

## Pronouns

Isaac can keep track of the preferred (gender) pronouns of users, and you can look them up at any time.

**Note:** Isaac makes use of NickServ login data found through the `/whois` command for this functionality. The reason for this is twofold:

* This prevents a hard-to-solve problem of keeping track of users through nick changes and reconnects.
* This prevents the possibility of people messing with other people's pronouns by changing into their nickname.

The pronoun function uses these commands, that should be used on a line by themself. All of these commands are available both in channel and in private messages to Isaac.  
Isaac uses a global list for this, so there's no need to set this per channel.

It is possible to set multiple preferred pronouns for yourself, but this needs to be done one by one.

* `!pronouns <nickname>` Look up the pronouns for this user. Example use: `!pronouns Isaac`
* `!pronouns-add <pronoun>` Add a preferred pronoun for yourself. Example use `!pronouns-add he`
* `!pronouns-remove <pronoun>` Remove one of your preferred pronouns.
* `!pronouns-forget` Make Isaac forget ALL of your pronoun data.

The following pronoun options are available: **he, she, they, it, other**

If you lost access to your NickServ account and want anything changed or removed, please ask a bot admin for assistance.

<br>

## Botsnack

Can a bot who doesn't enjoy the occassional botsnack even be called a bot? Just type `botsnack` on its own line in any channel Isaac is in and see what happens.

<br>

## Other

The command `!help` will bring you back to this page. :)

<br>

## Admin-only commands

These commands work both in channel and in private messages, but can only be used by bot admins.

* `!quit` Hard shutdown of the bot. Only to be used if Isaac shows signs of becoming Skynet. After a shutdown CO2 needs to do a manual restart to bring him online again.
* `!pronouns-admin-add <pronoun> <nickname>` Adds a preferred pronoun to ANY nickname.
* `!pronouns-admin-remove <pronoun> <nickname>` Removes a preferred pronoun from ANY nickname.
* `!pronouns-admin-forget <nickname>` Make Isaac forget ALL pronoun data for this nickname.

<br>  

## Puppet master commands

_In the deep lore, there exist rumors of some secret role even more powerful than bot admins, namely the so-called puppet masters. Who are they? No-one really knows..._

Puppet masters have access to the following commands, that only work from private messages sent to Isaac.

* `!say <#channel> <text>` or `!say <nickname> <text>` Sends `<text>` to `<#channel>` or in a private message to `<nickname>`.
* `!act <#channel> <action>` or `!act <nickname> <action>` Sends `<action>` as a `/me` action to `<#channel>` or in a private message to `<nickname>`.

<br>

## Source code

If you're interested in the nitty-gritty details or want to run your own copy of Isaac, his source code is here: [https://github.com/CO2-Codes/Scala-IRC-bot](https://github.com/CO2-Codes/Scala-IRC-bot). It is maintained by CO2.
