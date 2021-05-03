---
description: 'Description'
---

there is 5 type of action that can be used in the plugin

msg: To send a message to player
cmd: To use a command
sound: To send a sound to player
wait: Delaying the action
server: To Connect a server

CMD - MOST READ
/npc action (npc-name) add (true/false - Use by Console or Player) (none/permission - To set Permission) cmd:/say I'm %player% hello all
                           (true: command will enter by console)   ('!' permission can be use for negetive) (%player% is ServerNPC placeholder but placeholdersapi support)
                           (false: player will enter the command)

CMD Exampel
player will send greating to server by intracting the npc
/npc action test add false none cmd:/say I'm %player% hello all
                                  ('/' Is needed if the command enterer is player 'false') 
                          (Permission matter because Player Need To have the permissions)


player will send greating to server by intracting the npc but need permission 
you can give 'say.hello' to players that you don't want to intract with npc

/npc action test add say.hello none cmd:/say I'm %player% hello all
                                  ('/' Is needed if the command enterer is player 'false') 


player will send greating to server by intracting the npc but most not have the need permission 
you can give 'say.hello' to players that you don't want to intract with npc

/npc action test add !say.hello none cmd:/say I'm %player% hello all
                                  ('/' Is needed if the command enterer is player 'false') 



console give the player 1 grass block

/npc action test add true none cmd:give %player% grass_block 1
                         (Permission Dosen't matter because Console have all the permissions - DON'T use the Negetive Permision '!')
                                 ('/' Is NOT NEEDED if the command enterer is Console 'true' - Console is not a player to use '/')



MSG
/npc action (npc-name) add (true/false - Use by Console) (none/permission - To set Permission) msg:&aHi %player_name%
                           (USE false HERE)              ('!' permission can be use for negetive)      (%player% is ServerNPC placeholder but placeholdersapi support)

MSG EXAMPEL
send greting to player by intracting the npc

/npc action test add false none msg:&aHi %player%


send greting to player by intracting the npc but needs the permission 'say.hello'
you can give 'say.hello' to players that you want to intract with npc

/npc action test add false say.hello msg:&aHi %player%


send greting to player by intracting the npc but most not have the permission 'say.hello'
you can give 'say.hello' to players that you don't want to intract with npc

/npc action test add false !say.hello msg:&aHi %player%

here a cool way to add message

    - false|none|msg:&ahere a grass
    - true|none|cmd:give %player% grass_block 1
    - false|say.hello|msg:&ahere a grass cool guy



SOUND
/npc action (npc-name) add (true/false - Use by Console) (none/permission - To set Permission) sound:ENTITY_VILLAGER_YES
                           (USE false HERE)              (Only use negetive permission '!' or none - because it's throw a unwanted message)

Sound list can be found here: https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Sound.html

SOUND EXAMPEL
play the sound for a player

/npc action test add false none sound:ENTITY_VILLAGER_YES



WAIT
/npc action (npc-name) add (true/false - Use by Console) (none/permission - To set Permission) wait:2000  
                           (USE false HERE)                                                       (It is in MILISECONDS - 2000 = 2 Second)
                                                         (Only use negetive permission '!' or none - because it's throw a unwanted message)

WAIT EXAMPEL
make an action to be dalyaed by 2 second

/npc action test add false none wait:2000


you can make a player to bypass the delay by giving them a permission and negetiving it

/npc action test add false !say.hello wait:2000

you can add delay between all actions 

    Action:
    - false|!say.hello|wait:1000
    - false|none|sound:ENTITY_VILLAGER_YES
    - false|!say.hello|wait:2000
    - false|!say.hello|msg:&aHi %player%
    - false|say.hello|msg:&aHi &e&n%player%&a, You have a cool a permission that make you bypass the delay.



SERVER
/npc action (npc-name) add (true/false - Use by Console) (none/permission - To set Permission) server:survival  
                           (USE false HERE)                                                       (It is in MILISECONDS - 2000 = 2 Second)
                                                         (!permission can be use for negetive but not recommended to set a permission)

you need the ServerNPC BungeeCord Addon plugin to be instaled on bungee server (no config needed for this plugin)
get it here: https://www.spigotmc.org/resources/servernpc-bungeecord-addon.84094/

SERVER EXAMPEL
send a player to survival

/npc action test add false none server:survival


send player to Survival server but need the permission 'go survival'
you can give 'go.survival' to players that you want to be sended to the Survival server

/npc action test add false go.survival server:survival


send player to Survival server but most not have the permission 'go.survival'
you can give 'go.survival' to players that you don't want to be sended to survival

/npc action test add false !go.survival server:survival

here a cool way to send a player to your survival server

    Action:
    - false|!go.survival|wait:1000
    - false|none|sound:BLOCK_BEACON_ACTIVATE
    - false|none|msg:&2Going to Survival
    - true|nono|cmd:title %player% title {"text":"Going To Survival!", "italic":true, "color":"dark_green"}
    - false|!go.survival|wait:1000
    - false|none|server:survival
