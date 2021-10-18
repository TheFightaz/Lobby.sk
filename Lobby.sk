#=========================================#
#=====SK/PL WYKONANY PRZEZ THEFIGHTAZ=====#
#==========ZAKAZ KOPIOWANIA!==============#
#=========COPYRIGHT 2021©=================#
#=========================================#



#===LOBBY CORE PLUGIN===#



#OPTIONS FOR SHORTCOUT
options:
	tag: &4Ez&7Craft&f.pl &8|


#ON JOIN FUNCTION / ADD "ITEM" TO PLAYER INVENTORY AFTER JOIN

on join:
	clear player's inventory						#CLEAR INVENTORY ON JOIN NEED TO FIX ALL ITEMS IN INVENTORY
	wait 1 seconds									#TIMER ON JOIN
	set slot 4 of player to clock named "&7Wybór serwera" with lore "&4» &7Klinij &2LPM &7i otówrz &4menu!"			#GUI SLOT OF PLAYER INVENTORY
on first join:
	clear player's inventory
	wait 1 seconds
	set slot 4 of player to clock named "&7Wybór serwera" with lore "&4» &7Klinij &2LPM &7i otówrz &4menu!"

#OPENABLE GUI FOR PLAYER / SERVER CHOOSEN
on rightclick:
	if player's tool is clock named "&7Wybór serwera" with lore "&4» &7Klinij &2LPM &7i otówrz &4menu!":
		open chest inventory named "&4&lEz&7&lCraft&f&l.pl &8| &7&lSerwery" with 1 rows to player		#CHEST NAME INVENTORY 
		wait 2 tick
		set slot (integers between 0 and 1) and 3,5 and (integers between 7 and 8) of player's current inventory to red stained glass pane named "" with lore "" 		#RED GLASS OUTSIDE GUI
		set slot 2 of player's current inventory to stone named "&bCave&4Block" with lore "&4» &7Wejdź w tajemniczy świat &bjaskiń" and "&4» &7Odkryj nowości, które" and "&7dla was przygotowaliśmy!" and "" and "&4» &7Wersja &b: &41.8 &7- &41.17"			#CAVEBLOCK GUI
		set slot 4 of player's current inventory to paper named "&aInformację" with lore "&4» &7Wybierz jeden z naszych trybów" and "&4» &7I baw się dobrze!" and "" and "&4» &7Strona &b: &4Ez&fCraft&f.pl" and "&4» &7Discord &b: &4ezcraft.pl/discord" and "&4» &7FanPage &b: &4XXX"		#INFORMATION GUI
		set slot 6 of player's current inventory to oak sapling named "&bSky&4Block" with lore "&4» &7Chcesz odkryć wysparski tryb życia?" and "&4» &7Wbjaj na nasz &4SkyBlock!" and "" and "&4» &7Wersja &b: &41.8 &7- &41.17"  		#SKYBLOCK GUI

#GUI BLOCK EVENT / DO NOT TOUCH IF U DON'T KNOW WHAT TO DO!!!
on inventory click:
	if name of player's current inventory is "&4&lEz&7&lCraft&f&l.pl &8| &7&lSerwery":
		if clicked inventory is not player's inventory:
			cancel event

#CANCEL DROP SYSTEM ON MENU ITEM! / CANCEL MOVE ITEM FROM INVENTORY EVENT
on drop:
	if event-item is clock named "&7Wybór serwera" with lore "&4» &7Klinij &2LPM &7i otówrz &4menu!":
		cancel event
on inventory click:
	if clicked slot is 4:
		cancel event

#MAIN MENU TELEPORT SYSTEM / WITH BINGECORD!
on inventory click:
	if name of player's current inventory is "&4&lEz&7&lCraft&f&l.pl &8| &7&lSerwery":
		if clicked inventory is not player's inventory:
			if clicked slot is 2:
				close player's inventory
				clear player's inventory
				send "{@tag} &7Trwa rozgrzewanie teleportera... &8(&7Tryb &4Cave&bBlock&8)" to player
				wait 2 seconds
				execute console command "send %player% caveblock"
on inventory click:
	if name of player's current inventory is "&4&lEz&7&lCraft&f&l.pl &8| &7&lSerwery":
		if clicked inventory is not player's inventory:
			if clicked slot is 6:
				close player's inventory
				clear player's inventory
				send "{@tag} &7Trwa rozgrzewanie teleportera... &8(&7Tryb &4Sky&bBlock&8)" to player
				wait 2 seconds
				execute console command "send %player% skyblock"
				
#COMMAND BLOCKS FOR PLAYERS / LOBBY CORE 
on command:
    command is "bukkit:help" or "bukkit:me" or "bukkit:plugins" or "bukkit:tell" or "bukkit:version" or "help" or "plugins" or "plugin" or "version" or "versions" or "tell" or "whisper" or "me" or "minecraft:me" or "minecraft:help" or "minecraft:plugins" or "pl" or "?" or "bukkit:?" or "bukkit:pl" or "minecraft:pl" or "about" or "action" or "br" or "advancedban:ban" or "advanedban:ban-ip" or "advancedban:banip" or "advancedban:banlist" or "advancedban:list" or "adventure" or "adventuremode" or "afk" or "armor" or "antioch" or "away" or "back" or "backup" or "bcast" or "bcw" or "bigtree" or "blocks" or "book" or "boss" or "bosses" or "break" or "broadcast" or "ver" or "broadcastworld" or "brush" or "burn" or "cc" or "captcha" or "changems" or "chatdisable" or "chatenable" or "chatmute" or "chestcommands" or "ci" or "ck" or "wand" or "clean" or "reload" or "clear" or "ec" or "clearchat" or "clearinvent" or "calc" or "calculate" or "center" or "chunk" or "clearhistory" or "contract" or "copy" or "count" or "curve" or "cut" or "cyl" or "desel" or "spawnershop" or "skyblock author" or "skyblock help" or "authme" or "version" or "me":
        player don't have permission "fightaz.unlock":
            cancel event
            send "&8&l| &4&lEz&7&lCraft&f&l.pl &8&l| &7- &cNie poprawna komenda! &7Wybierz jeden z trybów!"
