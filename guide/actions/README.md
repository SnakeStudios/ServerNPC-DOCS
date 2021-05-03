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

```text
/npc action (NPC NAME) add (TRUE/FALSE - CONSOLE) (PERMISSIONS OR NONE) (ACTION)
```

On \(ACTION\) you can put these options. Without `()` please.

* **cmd**:/say Hello
* **server**:Survival
* **msg**:&aHello %player%
* **wait**:1000 \(It is in [MILISECONDS](https://www.google.com/search?q=1000+milliseconds+to+seconds&oq=1000+milliseconds+to+seconds&aqs=chrome..69i57.447j0j9&sourceid=chrome&ie=UTF-8)\)

![/npc action npc1 add false none cmd:/say Hello!](../../.gitbook/assets/image%20%2816%29.png)

![\*You can add multiple actions :D\*](../../.gitbook/assets/2020-04-14_09.56.07.png)

### Getting actions setted

```text
/npc action (NPC NAME) list
```

![/npc action npc1 list](../../.gitbook/assets/image%20%2815%29.png)

### Removing Action

To remove the action added before, use the command below.

```text
/npc action (NPC NAME) remove (ACTION ID)
```

![/npc action npc1 list](../../.gitbook/assets/image.png)

![/npc action npc1 list](../../.gitbook/assets/image%20%282%29.png)

