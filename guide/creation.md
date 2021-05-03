---
description: How to create an NPC with ServerNPC
---

# Creation

## Creating an NPC

You can create it in various ways. The first and most common it's Mojang names. But here's the list of the supported methods in ServerNPC.

* Mojang
* Mineskin
* Self Skin

## Mojang

To create a NPC with Mojang name it's very very simple.

{% hint style="info" %}
/npc create test1 iSnakeBuzz\_
{% endhint %}

If you typed this command, you will notice the NPC has spawned with my skin, but you can change my name \(iSnakeBuzz\_\) for anyone name.

{% hint style="danger" %}
Only if the name it's a Premium account, if not, it will be appear as a Steve.
{% endhint %}

## Mineskin

> **MineSkin.org** allows you to generate **skin texture data** signed by Mojang.  
> These can be used on ingame skull blocks or to change a player's skin using some packet magic :\).

Said by Mineskin.

It allow you to upload Skins without needing a Minecraft Account. Well, you can use the generated IDS in ServerNPC to create fantastics NPCs.

![](../.gitbook/assets/image%20%285%29%20%282%29.png)

{% hint style="info" %}
/npc create test2 420161720
{% endhint %}

And done, you've created a NPC with Mineskin. Very simple, right?

## Self Skin

Well, to use this you need [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) installed in your Server. If you don't know what it is, I fully recommend you to read the official page. But simplifying that, it's a library of placeholders.

First of all you need to install the `Player` extension to continue.

```text
/papi ecloud download Player
/papi reload
```

Execute both commands to a correct installation of the extension. Then we can continue with the NPC creation.

{% hint style="info" %}
/npc create test3 %player\_name%
{% endhint %}

Well, that very easy, if you don't see your Skin, probably you are a cracked player, at the moment we are working on a fix to work with SkinsRestorer but do not have a estimated time for that.

