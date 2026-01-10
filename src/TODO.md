# TODO list updated 12/31/2025

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


## 1/9/2026 Game 2 Testing report to fix
- [x] check buying steak
- [x] fireball should have a larger power that breaks harder blocks
- [ ] lootbox rewards are still bad
- [x] Extract location didnt work

## 1/4/2026 Game 1 Testing report to fix
- [x] scaling of the prices do not reflect in the shop
- [x] dark redstone/lapis ore does not activate vein miner
- [x] went into negative cash when buying ore duplicate
- [x] placing tnt doesnt actually take away from inv
- [?] cannot buy steak
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