## Issues
- There are client side mods that hide the players bossbar for some reason right now these mods are (Better F3)

# Roadmap updated: 7/2/2026
- [ ] remove water caves if possible
- [ ] UHC custom weapons
- [ ] make extract point spawn mobs around the player before sending them home
- [ ] selectable difficulties
- [ ] add expensive feather falling - Possibly wont add to increase risk factor
- [x] make finding caves easier - Maps must be opened by the player - For now this is 
- [ ] add support for trial chamber
- [x] Music disc audio becomes distorted the farther players are from 0,0. only generate valid spawns within 2mx2m
- [ ] custom music https://www.reddit.com/r/C418/comments/1342bkf/is_there_a_way_to_add_some_more_tracks_to_the/
- [ ] dialogs https://skripthub.net/docs/?id=14436
- [ ] manaquins at spawn displaying the top 3 players on the leaderboard
- [ ] Custom caverns or structures can be located by purchasing a compass?

# 7/3/2026 - Playtest num 2
- [x] lootboxes should obvously give different amounts
- [x] lucky miner doesnt send message when procced
- [x] damage on mobs is broken
- [x] extracting doesnt give points back + gamemode doesnt change back to adventure
- [ ] spectact player see what they see
- [x] create worlds on another server then transfer them to the main server. figure out how to tp players between worlds.
    -  Skbee contains a world generation feature which utilizes dimensions. When the server is empty or when daily restarts happen generate X amount of worlds. if the server reaches a threshhold new worlds will be generated followed by lag which will need to be told to the player
    -  Allow players to enter the nether. when entering the portal they will be teleported to a brand new nether which will have difficult mobs but higher value ores.
    - Account for game rules within the world as they may be per dimension 
    - Teleport the player to 0,100,0
    - https://skripthub.net/docs/?id=11634 
- [x] more death messages https://skripthub.net/docs/?id=10573
- [ ] add fire protection
- [x] fix monster spawner not rewarding points
- [x] upgrading to netherite possibly removes all pickaxe efficieny enchants
- [x] allow players to move items around in their inventory
- [x] allow droping items unless it is armor, pickaxe, or the menu item
- [x] allow players to move around items in their inventorys when in the shop. Addtionally add a safeguard when players move said items so they do not charge themselves or buy things on accident


# 6/22/2026 - playtest num 1
- [x] previous runs duration still invalid
- [x] first difficulty shows mob speed health at 50 should be 0
- [x] cycle through music
- [x] add more documentation for extract point
- [x] make /enchants
- [x] add leaderboard
- [x] disable natural mob spawns
- [x] modify mob scaling
- [x] add iron golems in the shop
- [x] make lootbox animations cooler
- [x] if player is shifting fire fireball as second clause
- [x] send message to player displaying what booster card they've unlocked
- [x] nerf streak to require more ores before multiplier kicks in
- [x] a visualizer to see how deep you are
- [x] something telling player going deeper = more ores
- [x] add more difficult mobs the deeper you go
- [x] night vision in /settings
- [x] stats dont display properly
- [x] visually show player has hit max level in shop
- [ ] points per minute in hotbar
- [x] minecart chests and barrels give you items
- [x] remove putting items in pots
- [x] not allow drinking milk
- [x] disallow rightclicking beds
- [x] end of run stats




# 6/18/2026
- [x] When spawning extract load the chunk and then save.
# 5/20/2026

- [x] lootbox procc msgs are not formatted correctly
- [x] Add /setup wich generates 25 valid spawns, sets gamerules
- [x] Enchant tiers are not color coded correctly and lootboxcollector was able to duplicate IV to V
- [x] Starting in... looks like ass

- [x] Placing lootboxes does not work fix next!


# 4/6/2026

## QOL
- [x] Damage indecators
- [x] Create an array of 100 different spawning points preloaded to avoid needing to load lots of chunks

- [x] dont store pointbar in variable use minecraft boss bar id's
## Anticheat
- [ ] Create a custom anticheat that collects data to determine if a run wasnt legit

## On next play test, validate:
- [x] The Extractor

## Multiplyer support
- [ ] Validate that multipler players can start their own independent game. Change all variables to include %player% at the end
    - [x] All variables have been validated to have %player%

## Website support
- [ ] Create a website that hosts the variable infromation from each game

## Enemy
- [ ] The curroption: Teleports player to parkour area on contact then teleports them back



# 3/18/2026
## Cards
- Booster cards are unlockables that can be obtained through playing the game. These cards can be selected in the spawn to benefit the next run.
- Cards should be able to unlock randomly
- After a minimum total point threshold has been passed once the player ends their run they will receive a notificaiton saying they unlocked a card
    - [x] Vein miner 1-1: Start the run with the vein miner enchant
    - [x] Blood lust 1-3: Randomly(5%, 10%, 15%) receive strength 1 after attacking
    - [x] Second life: Have a 50% chance of reviving when dying (1 time use per run)
    - [x] Extraction expert: Start the run with the Extractor item
    - [x] Head master: Start the run with 3 golden heads

## Custom items
- [x] Extractor: When used teleports the player to the surface.

## Options
- [x] Create a options menu that players can open and change different settings
    - [x] Volume
    - [x] Enchant procc notification type
        - [x] Chat display
        - [x] Audio alert
    - [x] Skip lootbox animations
    - [x] Starting music on/off
    - [x] Visual block floating effect on/off


# 12/31/2025
## Commands
- [x] Add a /debug command to give the player 1,000,000 points when starting out

## On block break
- [x] whenever the player mines any block the item of the block should drop in the middle of the block. This block would need to check if Lucky Miner has procced aswell inorder to show the correct ore.
    - drop 1 taget-block at target-block-location
    - on pickup:
    - if player is ingame:
    - cancel event

## Custom Enchants
- All enchants will need to be procced using a function inorder for vein miner to call them.
- Current enchant level should be stored in a variable to keep the server from checking the lore on the players tool constantly
- No enchant should validate if the player is in the game due to the fact that the player must be in the game inorder to even have the enchant
- The price increase from each consecutive enchantment should be stored in a variable for easy alteration later on.
- Custom enchants should have custom colors associated with them. Enchants will be stored in the lore of the item and in a variable
- Enchants will have to be transfered when the player upgrades their pickaxe tier
- Custom enchants may need their own section in the shop menu as the shop will becom cluttered without multiple pages
    - [x] Vein miner: will mine ores surrounding the targeted block
        - lvl 1-3: 2 extra blocks broken, 4 extra blocks broken, 8 extra blocks broken
        - Cost per level starts at 1k will 2x every time (1k, 2k, 4k)
        - when the player mines a block with this enchant if the player has other enchants on the pickaxe those enchants must be able to be procced on the effected blocks. This means the functions to procc other enchants should be called

    - [x] Streak: As the player breaks more and more ores the streak rewards them with a point multiplier (current mult + streak mult) the streak multiplier will go up to 1.5x points.
        - lvl 1-1: the point multipler begins at 1.00x after the player has mined 5 ores it begins increasing to +0.01x every consecutive block after that one. After 10 sections the streak will be lost
        - Cost: 20k
        - The streak multiplier should be added next to the base multipler "points earned (base + streak)"

    - [x] Ore duplicate: As the player breaks ores theres a chance the ore will be replace needing to be broken again this replacement should happen before any vein miner checks so the ore can duplicate then if the player has the vein miner enchantment it will proc next
        - lvl 1-5: 0.5%, 0.75%, 1.0%, 1.25%, 1.5%
        - particles and sound should play whenever the enchant has procced (sounds should be able to be disabled later on)
        - Cost per level starts at 2k will 2x every time
    
    - [x] Lucky Miner: As the player breaks ores theres a chance a higher teir ore will be earned based off of the current ore teir
        - lvl 1-5: 0.5%, 1.0%, 2.0%, 4.0%, 5.0%
        - Cost per level starts at 1k will 2x every time
        - Should display the correct ghost ore when breaking indicating that the enchant has procced 

    - [x] Shard finder: Chance to find shards when mining
        - lvl 1-5: 0.5%, 0.75%, 1.0%, 1.25%, 1.5%
        - Cost per level starts at 500 will 2x every time

    - [x] Feed: Feeds the player 1 hunger point when mining ores
        - Cost: 5k

    - [x] Powerball: shoots a fireball whenever the player right clicks. cool down is 60 seconds
        - lvl 1-3: effects the radius of the fireball
        - Cost per level starts at 5k and will 2x every time
        - effected broken blocks should active other enchants

## Custom items
- [x] Mining shards or lootboxes similar to cosmic prisons? open them to get random items/points
    - on right click with prismarine shard
    - Loot table should be stored in onLoad with percentage chance of obtaining
    - rare chance on being obtained when mining ores. can be increased with enchants

## Custom mobs / Difficulties
- [x] Instead of increasing game speed which would cause server lag replace this with a way to spawn in harder mobs with custom armor / enchants
- [x] When the player enters a new difficulty a enderdragon summoning or wither summoning sound should play as a audio indicatior telling the player the difficulty has increased
    - Instead of having a narrator tell you messages in chat change it to what the new difficulty has modified
    
## Multiplyer support
- [ ] Validate that multipler players can start their own independent game. Change all variables to include %player% at the end
    - [x] All variables have been validated to have %player%

## Database support
- [ ] Create a website that hosts the variable infromation from each game


## 1/9/2026 Game 2 Testing found bugs
- [x] check buying steak
- [x] fireball should have a larger power that breaks harder blocks
- [x] lootbox rewards are still bad
- [x] Extract location didnt work

## 1/4/2026 Game 1 Testing found bugs
- [x] scaling of the prices do not reflect in the shop
- [x] dark redstone/lapis ore does not activate vein miner
- [x] went into negative cash when buying ore duplicate
- [x] placing tnt doesnt actually take away from inv
- [x] cannot buy steak
- [x] fireball needs to spawn infront of player 2 blocks
- [x] all armor enchants do not scale in price
- [x] wind charge explosions give the player ores
- [x] legendary lootboxes dont have unique animation
- [x] add sound to lootboxes
- [x] difficulties need to tell the player what has changed
- [x] extract location needs to be told to the player
- [x] legendary lootbox reward is sad
- [x] Golden heads should give speed 2 and resistance 1
- [x] spawnExtract location needs to have a player pass through it for multiple games compatability