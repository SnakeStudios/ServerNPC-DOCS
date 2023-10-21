---
description: How to use ServerNPC with commands or actions.
---

# Actions

## Getting started with Actions

The first thing you need to know is that there are multiple actions. Such as.

* Send player to server
* Execute command
* Send private message to player

**I hear recommendations..**

### Add new actions

For example, add the commnad "/say hello" to the npc

```
/npc action add (NPC NAME) (TRUE/FALSE - CONSOLE) (PERMISSIONS OR NONE) (ACTION)
```

On (ACTION) you can put these options. Without `()` please.

* **SPIGOT\_CMD**:/say Hello
* **BUNGEE\_SEND**:Survival
* **PLAYER\_MSG**:\&aHello %player%
* **WAIT**:1000 (It is in [MILISECONDS](https://www.google.com/search?q=1000+milliseconds+to+seconds\&oq=1000+milliseconds+to+seconds\&aqs=chrome..69i57.447j0j9\&sourceid=chrome\&ie=UTF-8))
* **PLAYER\_SOUND**:ENTITY\_VILLAGER\_YES
* **BUNGEE\_CMD**:Survival ([Needs BungeeCord Addon](https://builtbybit.com/resources/servernpc-bungeecord-addon.17407/))

![/npc action npc1 add false none cmd:/say Hello!](<../../.gitbook/assets/image (4).png>)

![\*You can add multiple actions :D\*](../../.gitbook/assets/2020-04-14\_09.56.07.png)

### Getting actions setted

```
/npc action list (NPC NAME)
```

![/npc action npc1 list](<../../.gitbook/assets/image (2).png>)

### Removing Action

To remove the action added before, use the command below.

```
/npc action remove (NPC NAME) (ACTION ID)
```

![/npc action npc1 list](<../../.gitbook/assets/image (1).png>)

![/npc action npc1 list](../../.gitbook/assets/image.png)
