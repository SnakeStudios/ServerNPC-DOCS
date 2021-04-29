---
description: How to use HolographicsDisplay with ServerNPC and PlaceholderAPI
---

# Holograms Usage

## Getting Started

First, see how to setup the hologram system!

{% page-ref page="holograms-installation/" %}

Once everything is installed, let's continue!

## Create your first hologram

Use the command below to set your first hologram into your npc.

{% tabs %}
{% tab title="ADD COMMAND" %}
```yaml
COMMAND:
/npc holo {npc name} add {message}

EXAMPLE:
/npc holo npc1 add Hello! I'm a hologram :D
```
{% endtab %}

{% tab title="REMOVE COMMAND" %}
```
COMMAND:
/npc holo {npc name} remove {id}

EXAMPLE:
/npc holo npc1 remove 1
```
{% endtab %}

{% tab title="LIST HOLOS" %}
```
/npc holo {npcName} list
```
{% endtab %}
{% endtabs %}

![See the beautiful NPC](../.gitbook/assets/image%20%281%29.png)

### Add placeholder to Holograms

To update placeholders you need this placeholders before the message.

* {fastest} - 0.1 seconds. 
* {fast} - 0.5 seconds 
* {medium} - 1 seconds 
* {slow} - 5 seconds 
* {slowest} - 10 seconds.

In this case, i'm using the **{medium}** placeholder.

{% tabs %}
{% tab title="COMMAND" %}
```yaml
COMMAND:
/npc holo {npc name} add {medium}{message}

EXAMPLE:
/npc holo npc1 add {medium}Hello &e%player_name%
```
{% endtab %}
{% endtabs %}

![/npc holo npc1 add {medium}Hello &amp;e%player\_name%](../.gitbook/assets/image%20%2817%29.png)

![And here ya go.](../.gitbook/assets/image%20%283%29.png)

 

