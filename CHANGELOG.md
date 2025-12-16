# 2.3.0 Release
### This is a big one, make sure to backup your worlds before updating!

## What's changed?
**Added**
- New fusion reactor
   └ More dynamic system with more components to choose from
   └ Models and GUIs that are less eye-bleeding
   └ Plasmas are now represented as a recipe selector instead of dedicated fluids, making the entire thing fully configurable
   └ Despite being recipe based, fusion reactors will still burn fuel at a steady rate
   └ Comes with load-balancing, if the solenoid power or fuel supply drops, the reaction will slow down
      └ This ensures that supply below maximum demand doesn't cause "flickering" due to constantly running out of fuel
   └ Comes with many juicy parts
      └ The plasma vessel is where the magic happens, has four connectors for other parts
      └ Klystron is used to ignite the plasma
      └ Breeding chamber uses the plasma's output flux to do irradiation recipes
      └ Collector increases byproduct yield
      └ Boiler turns water into SDS
      └ MHD turbine makes power out of the plasma directly at greater efficiency
      └ Coupler turns plasma output energy into usable klystron energy, allowing one reactor to be powered by another, creating a multi-torus setup
   └ Also has full QMAW documentation, if the tooltips aren't enough
- Boxcables
   └ Like boxducts, but for power
- Animated orbital transfers for all rockets, not just orbital stations!
   └ Sun occlusion is now calculated using the eclipse solver, no more random darkness during transfers!
   └ Improvements to the orbital transfer animations for more ⊹₊ ˚‧︵‿₊୨ realisme ୧₊‿︵‧ ˚ ₊⊹ are planned
      └ Fuel calculations are already accurate though, using derived dV based on Hohmann transfers
- Oxygen-Rich Air - found on Earth and Laythe
   └ All your setups will automatically use this fluid instead of compressed air, where applicable
- Minmus mint icecream and delicious Aussie Mint Slice biscuits
   └ Mint plants will spawn in the same places strawberries do
- Orbital station launching port
   └ Allows you to construct and launch rockets from orbital stations
    The terrestial VAB and rocket launch pad no longer function in orbit
- Tekto bedrock oil
   └ Avoid collecting this near your base, the fracking damage is a fair bit more pronounced than other bedrock deposits!
- Synthetic leather/pleather
   └ Very useful for Martian playthroughs
- Created Recipe Widget; Recipe GUI: Infinity Scroll; Recipe GUI: Max Height Settings
- Added NEI function to copy item name and meta
- Added Scroll to NEI Recipe Catalysts
- Implemented Dynamic Handler Height (NEI)
- Added NEI 'Bookmark recipe with count' Option
- Added option to sort the player's inventory with the keybind while the GUI is closed
- Added terracota variations
- Integrated AppleCore food tooltips into all NEI GUI panels
- Seeding slurry is now appreciably boosted in growing power
   └ Will only work in atmospheres with at least trace amounts of CO2
   └ As an upside, will now convert CO2 into O2 at a rate of 100mB of O2 per block of grass
- Added Bob Fluid Translator
   └ This allows better NTM-AE2 compatibility
- Added Immersive Cave Gen
- Added ability to swim underwater
- Added foxes
- Added bundles (who asked bruh)
- Added new sound system
   └ Overworld now has an ambient
   └ Your surrounding can affect sounds
- Player face now showing in chat and tab menu
- Added skin layer support
- Reworked villages
- Annihilator
   └ Destroys items and fluids and keeps track of how much has been destroyed
- NEI handlers for
   └ Atmospheric Extraction via Compression
   └ Celestial Bedrock Ore Processing
   └ Celestial Fluid Table Extraction
   └ Celestial Oil Extraction



**Fixed**
- Fixed arc furnace only allowing electrodes to be inserted when the lid is down instead of up
- Fixed issue where the amounts tracker wasn't being used correctly when using a custom acidizer config, preventing the acidizer partitioner from working
- Fixed multi fluid ID search potentially not working on systems with a non-latin locale
- Fixed particle accelerator source working even if not cooled
- Fixed foundry channels being overly laggy in certain setups
- Fixed potential mod incompatibilities with world generation mods that use outdated forge hooks
- Fixed the buzzsaw not properly replanting trees using the leaves2 block type
- Fixed creepers regaining their exploding AI task upon relog, if defused
- Fixed assembly and chemical factories not properly saving their recipe fluid buffers
- Fixed light blue and light gray dyes not working when dyeing cables
- Fixed bismuth armor not having a valid repair material
- Fixed compressors needing at least one mB of fluid more to process a recipe than necessary
- Fixed many NTM structure spawn conditions being hardcoded (again) preventing them from spawning in modded biomes that would otherwise be a fit
- Fixed spawn offset for some structures which caused them to float in the air
- Fixed icons in the QMAW title bar often times being too dark when rendered with a 3D model
- Fixed rocket artillery modes having incorrect tooltips
- Player models now tilt with rockets, no more feet sticking out during gravity turns
- Worldgen performance was poo poo, now it is 14x less poo poo (that's 28x less poo with RTG installed!)
- Crash with certain malformed rideable rockets
- Celestial world providers extended the wrong class, breaking oregen in GT
- Meteors spawning in non-surface modded dimensions (like AE2 spatial cells)
- Insane thunder spam when a dimension with no atmosphere is loaded
- Attempt at fixing station thrusters remaining "on"
- Fixed ore acidizer recipe config just straight up not working with ore dictionary keys
- Fixed logistic network nodes disabled via redstone not re-enabling when redstone is cut
- Added provisional emergency brake to drone pathfinding, pathfinding will simply fail if it goes on for too long
- Fixed ore acidizer partitioner freezing the game
- Fixed ore acidizer partitioner trash slots not being accessible via automation
- Fixed recipe for the measuring tape
- Fixed Witch Spider infinite projectile duplication
- Fixed crash when opening lunch box from offhand
- Fixed some crashes when grabbing items from drawers
- Fixed teleport task player reference crashes
- Fixed pressing '2' when hovering crafting output not putting the crafted item(s) in the hotbar (NEI)
- Fixed missing lang key for NEI favorite keybind
- Fixed NEI Permutation Filter 
- Fixed NEI Favorite Recipes in bookmarks for ingredients
- Fixed NEI Bookmarks Shadow Items
- Fixed NEI None hotkeys for java8
- Fixed NEI tooltip item lighting
- Fixed NEI HUD flickering
- Fixed recipe result count
- Fixed NEI Bookmarks Chain Tooltip Height
- Fixed NEI Button Texture
- Fixed shift+scroll of ingredients in the recipe GUI
- Fixed 'Delete Item' tooltip not showing in Creative Mode
- Fixed small mouse movement while double-clicking causing drop all items
- Fixed NEI favorite state refresh
- Fixed NEI recipe collapsing
- Fixed pressing space in text box close UI if space is your inventory key
- Fixed glider showing upside-down for other players
- Fixed non-deployed glider position for other players
- Fixed a Haunted Miner research requiring itself (HEE)
- Fixed splitting of items with max stack size of 1 during sorting (Bogosorter)
- Fixed Bogosorter Keybindings
- Fixed Bogosorter refill sync issue
- Fixed various p2p binding issues
- Fixed issues when changing p2p type that involves conversion
- Fixed conversion to p2p-static doesn't return replaced p2p to inventory
- Fixed conversion to p2p-normal doesn't consume p2p from inventory
- Fixed drops in p2p are only dropped when no space in player inventory
- Fixed the quest name in the notification is not localized (in multiplayer)
- Fixed chisel slot voiding in some conditions
- Fixed fast clouds rendering with setting off after game restart
- Fixed Tileentities not casting shadows
- Fixed entity/item textures and lighting break with shaders
- Fixed Bibliocraft clipboard skipping a page
- Fixed offhand attack dealing 1 damage
- Fixed offhand item switching animations
- Capsules can be exited during transfers, when the doors should be locked
- Holding crouch can inconsistently drop you out of a capsule even when the doors are locked
   └ Due to some vanilla shenanigans, you'll sometimes encounter visual issues if you hold the key, but now you'll still remain in the capsule
   └ To prevent potential gamebreaking issues, you can force-leave a capsule by holding crouch for three seconds (unless in deep space, where you'll always be fully blocked from leaving)
- Fixed the old fusion station thruster appearing as the new. as-of-yet unimplemented one
- Fixed gamebreaking issue causing crashes and world corruption where the multi detonator had its tooltip misspelled
- Fixed panzerschreck equip animation not speeding up with the sawed off mod
- Fixed FENSU not keeping its charge when broken
- Added more null checks to world generation, hopefully preventing weird one-off crashes
- Fixed arc furnace queue slots inserting too many items, causing the output to exceed max stack size



**Changed**
- **REMOVED IRON BACKPACKS - EMPTY THEM BEFORE UPDATING**
- **REWORKED WHOLE QUESTBOOK** (thank you \_SkippyPlaysMC_!)
- Added completely new crash reportation system
- Debuffed mobs
   └ Decreased their spawn rate
   └ Now there are no Bosses (Infernal Mobs)
- Rebalanced food system
   └ Now snacks, meals meaty meals are giving you way more saturation
   └ But raw vegetables are not that good now
- Updated chinese localization
- Updated meteors
   └ Meteors will now punch through weak blocks like leaves instead of getting stuck on trees
   └ Meteor impacts now have new visuals
   └ Falling meteors will produce a sound instead of stealthily blowing people up
   └ Fallen meteors will now be placed deeper into the actual crater instead of hovering awkwardly over the hole
- Added QMAW pages for the particle accelerator parts along with a PA overview page and a simple step by step construction tutorial
- Increased the acidizer partitioner's input limit from 9 to 45 slots
- Ammo containers are now functional again
   └ Each gun has a fixed "default ammo" that will be given
   └ Grants ammo for up to three held guns, selected randomly
   └ Ammo given does not respect caliber conversion mods
   └ Amount of ammo given depends on the mag size and type of ammo
      └ Most pistols and low capacity rifles will get two reloads worth of ammo
      └ High capacity rifles will typically get only one magazine
      └ Rocket launchers typically only get a small amount of rockets
      └ The fat man only gets a single nuke
      └ Certain legendaries do not give ammo at all, they are omitted when three randomly held guns are selected
- Ammo containers are now found in more itempools
- The arc furnace input queue can now be moved into the recipe grid if the lid is at least slightly open instead of requiring a fully opened lid
   └ This means that in system with slow input, the time window when items can be added to the arc furance is now more forgiving
- Pipe anchors now have a look overlay showing the currently configured fluid type
- Removed ammo duping using nitra, instead, four large piles can now be combined into an ammo container
   └ Ammo containers crafted from nitra cannot give "expensive" ammo types
   └ This mainly excludes mini nukes and .35
   └ Comes in a distinct blue color instead of military green
   └ Makeshift containers also yield only half as much ammo as regular ones
- Using a defuser, creepers can now be rendered harmless manually
- Defusing creepers now also works if the creeper hasn't lit its fuse yet
- Defused creepers are now permanently harmless, they can no longer be manually re-ignited at all
- Manual defusers now also affect big man johnson
   └ Defusing only works if the timer is active
   └ The glpyhid will explode instantly, but only about as powerful as a conventional rocket, not destroying blocks
   └ Doing so will also drop one usable demolition mini nuke
- The painsaw ability no longer plays the blood splash particle effect
   └ Instead, it will outright gib the target
- Pile plutonium rods can now be reprocessed in the PUREX in addition to the old anvil recipes
   └ The recipes require 100mB of sulfuric acid and 100HE/t, the lowest requirement for all reprocessing recipes
   └ The recipes are part of a shared auto switch group, meaning that even if different rod types are produced, only one PUREX is necessary
- Grass is no longer a valid paint block for paintable cables and ducts
- Multiblocks are no longer affected by collapses caused by nuclear explosions
- The old NITAN powder chests have been removed
   └ In their place, there's now a different, more useful structure with similar but not identical spawn rules
- ROR controller torches can now set the threshold of particle accelerator dipoles
- Removed the legacy recipes from the terra drills
- Slag can now be cast into ingots
- Re-solidifcation of bedrock ore crumbs now requires ore slop instead of nitric acid
   └ Due to ore slop being only obtainable from processing raw bedrock ore, this places a hard cap on how many times a single ore can be re-solidified out of crumbs
   └ This approach means that crumb yields don't have to be nerfed, and prevents that issue from popping up again should there ever be a new, more efficient processing path
- Rewrote the ore layer generator (hematite, bauxite) to be way more performant during worldgen
- The mining laser can now be stopped by applying a redstone signal to one of the ports
- Ionized particles can no longer be liquefacted into helium-4, helium is now a direct liquid byproduct of several fusion reactor recipes
- Adjusted schrabidic acid recipe to account for higher ionized particle yield
- Increased the ICF's stellar flux output by a factor of four
- Air intake is no longer decorative, can create compressed air
        Will consume air inside pressurized rooms and convert it into compressed air at a 1:100 ratio
        This means a klystron will consume 25mB/t of oxygen if used in an orbital station, just a tad more than the old fusion reactor consumed
- Entanglement kits now use krypton instead of xenon, which can be acquired on Earth after stainless steel
- T-51 armor can now be used as a spacesuit
- Minor circuit rework
   └ Avionics chip added
   └ Existing avionics chip renamed to astrionics unit
   └ Cheaper military grade chips on Tekto!
- Murky wings can now descend properly when used in orbit
- Removed the old ZOMG beams, negative energy type explosions now use DFC-like effects instead
- Removed the old multitool (it sucked)
- Stages now decouple in two steps, with the engine shroud decoupling shortly after the prior stage
- Most seeds can now be obtained by plowing the land
- Removed GregCaves
- Added Backhand Support for Storage Drawers
- Paused Bloodmoon for a couple of days after world creation
- Speedup NEI rendering
- Improved NEI recipe search
- Optimized NEI Bookmark Chains
- Optimized NEI permutations
- Removed Permutations from Output (NEI)
- Optimized cross-dimension loading
- Disabled Bogosorter keybindings by default
- Backhand slot is now being skipped during dropoff
- Optimized FMP Rendering and memory leaks
- Moved Snakestone head and body blocks into the Smooth Stone chisel 
- Network Visualizer now shows connections between a Crafting Input Bus/Buffer and its proxies
- Improved zoom key handling (reset on GUI enter and compatibility with mouse buttons)
- Optimized in-world item rendering
- [Shaders] Basic compatibility with NTM:Space skybox & more
- Removed HBMAEAddon
- Updated tips in loading screen
   └ Should be less cringe
- Removed legacy fusion reactor parts from the creative inventory
- Removed the legacy fusion reactor core components
- If a legacy fusion reactor explodes, it is now destroyed forever and cannot be reassembled
- Legacy fusion reactors no longer disassemble when being mined, rather they drop as one block
- Legacy templates are no longer listed in the creative tab
- Removed the old meltdown achievement
- Eating canned fists now hurts
- Due to repeated incidents regarding canned black holes, the mechanics have changed
   └ Vortices spawned now have a flag set that prevents them from breaking blocks entirely
   └ Vortices decay 4x faster than those spawned by singularity items, it should last about 2.5 seconds in total
   └ It will still very much kill you instantly and destroy your items
- Storage crates can no longer be placed into containment boxes
- Both types of blueprint booklets are now obtainable via precision assembler
   └ The recipes are lengthy, require a lot of power and have a low chance of succeeding
   └ Recipes require the divine pufferfish, driver of all innovation
   └ Where can you get this much pufferfish? Go figure it out
- Bedrock coltan is no longer a dedicated bedrock ore type
- Alt fire is now available for 10ga double barrel shotguns, allowing only a single barrel to be fired at once
- Drainage pipes, flare stacks and the annihilator now have the default fluid priority of LOW, meaning that excess removal using those no longer requires flow control pumps
- Halved base energy consumption for the solidifier and liquefactor
- Changed cracking tower recipe to use desh instead of polymer, as well as a little bit more niobium in favor of all the clay catalysts it used to have
- Iron and corroded barrels have been deprecated and are no longer obtainable
- Steel barrels and 256k tanks no longer use tar in their recipes
- Solidifying biogas into compressed biomass now yields 4x more, making the biogas route twice as efficient as simply compressing biomass
- Finally removed the long deprecated ambience radiation generator and geothermal generator
- Nerfed the ballistic jackets, as they are comically cheap and made some zombies impossible to kill in early game
- RBMK fuel rod items can now be inserted directly into fuel rods via right click, instead of having to open the GUI
- Containment boxes now use ferrouranium instead of raw U-238
- Added missing recipes to two legendary weapons
- Trash can is now forbidden
- Hunger depletes slower now
- Updated russian localization
- Changed the recipe change button on the mixer to be bright red with arrows on it (since the "C" looked too much like it meant "clear")





[Full Changelog](https://github.com/Nuclear-Tech-New-Horizons/NTNH/compare/2.2.0...2.3.0)

## Download
[GitGub](https://github.com/Nuclear-Tech-New-Horizons/NTNH/releases/tag/2.3.0)
