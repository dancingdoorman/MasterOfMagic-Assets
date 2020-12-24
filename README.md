# MasterOfMagic-Assets
The assets for the remake of Master of Magic

The aims of the Asset repository are:
1. Use the Large File Structure (LFS) flag on the repository containing binary assets.
2. Have seperate branches for the complete asset tree (master), for asset updates and for asset development steps. 
3. Have the asset repository used in another repository as a submodule or subtree.
4. Convert Scaled Vector Graphics (SVG) versions of the assets so the game can be scaled to any size.
5. Document the asset conversion process
6. Have a generic folder structure based on a number of dimension that can be reused for other games
7. Make it possible to create a ID-Asset Index from the folder structure so Asset update packages can override and extend existing assets.

## Asset repository with LFS used by engine repository
Using a seperate repository is uncommen for amateur game development. This should document and demistify the proces.

## Pixalated Asset conversion to SVG
The conversion proces should be documented so it is repeatable for all the assets and for other pixaled games.

## Dimensions for the Folder structure
The folder structure tries to group the assets by specific dimensions that are easy to determin thus making the tree structure easy and fast to navigate and also easy to order and maintain.
Creating an ID-Asset Index from the structure, mainly from the logical parts, would make updating and reordering assets more flexible, as the location of the assets is gotten via the index and thus indirect, being able to be redirected.

Getting to a specific asset could be done by answering a number of questions.
1. What release should the asset be in?
2. Is the asset affected by game time and if so in what act should it be?
3. In what knowledge category should the asset be sorted?
4. For what game mechanic is the asset used?
5. To what game specific thing belongs the asset to?
6. What function has the asset?
7. To what asset belongs this version of the asset to?

The folder structure has folders that are not used currently like dlc, expansion, act1, act2, act3, model, video, etc. but function as specific extension points that make it easier to add assets in the future while not disturbing the structure. 

Some dimensions may be uncommon for game creators like the screenplay and Core knowledge psychology dimension. These are added as easy to determin categories and natural to humans, so everybody can understand them. These categories make the structure also more stable as for instance a scepter may start out in possesion of Tauron, a game specific character, then be usable by all characters, a game mechanic, and finaly be also usable by mercenaries, another game mechanic. Putting the scepter asset in the Tauron folder initialy then moving it to the characters folder and finaly to some folder above characters and mercenaries, is confusing. It's better to identify it as it's own category and put it in the props/MagicalItems folder in the first place and point to that whenever it is needed.

Screenplay writers use a number of types that are usefull for games. This is more obvious for for Visual Novels (VN), but are also applicable to more mechanical games.
In writing a screenplay or storytelling in general the "Inciting incident" is the moment where the hero changes from his normal routine to his story arc. This generaly changes the visual imagry of the hero and the world the hero is in. In the case of Master of Magic the wizard is the hero and the game tells his story. While being banished the game could use the assets from Act2 instead of Act1. 


In developmental psychology core knowledge is defined as the knowledge people and animals are born with.
The 5 dimensions match with the types used in screenplay writing. 
Humans can sort things easily into one of the dimension, as they are fundamental do being alive, and can thus function as a sorting function for the "Game Mechanics" and "Game Specific" things.

### Merging by maintaining standard dimensions 
By maintaining the standard dimensions of the folder stucture merging with updates or other games is possible without conflict.

Possible games to merge assets with are:
* Colonization
* Civilisation
* Warlords
* Age of Wonders
* Kings Bounty
* Heroes of Might and Magic

### Ommiting dimensions 
Some dimensions can be ommited from the folder structure, but are added here for completeness and compatibility with other games. 
* If there is only 1 release the "Release version" dimension can be ommited.
* If the game does not change in appearance during the game, for instance there is no appocalitic event wherafter all units look different, all is static and thus the "Game time" dimension can be ommited.
* If the extensions of the files are distinct enough the "Functional" dimension can be ommited.

### Swapping dimensions
Dimensions can be swapped based on priority or preference
* The "Release version" can be moved in a number of ways
 a. It may be moved down if a release only adds a thing to the "Logical Game Mechanic" like a new race in an "expansion". 
 b. The "Release version" could also be under "Logical Game Time" adding "DLC" to "Act1" or "base" of the game. 
The issue is that "Release version" is generaly a bigger aggregation of assets that could land under any other dimension. It is howerever generally 1 download or install of the whole game. Placing it under an other dimension would make it a specific download of for instance a race. 

* The "Logical Game Time" dimension may be swapped with the other Logical dimensions as for instance only the characters change from Act1 to Act2 or only a specic hero changes like Tauron changes from Act1 to Act2. The later is similar to a transitory state like "Angered" or "Supercharged", but returning to "Normal" later.

* The "Functional" dimension can be put higher up the structure if there are seperate trees for audio, text, image and video. Because these functional items are further away from eachother treating them as a logical set is then harder. For example removing a Mercenary Hero from the game would involve traversing and removing multiple folders in the audio image and text folder structures instead of just the folder for the Mercenary Hero.

* The "Version" dimension can be put higher up the structure if large swats of the assets are versioned as sets. As people are working on 1 asset at the time, this would not be ergonimic. The "Version" dimension differs from the "Release Version" in that the later is an agregation of assets instead of a "Version" of a specific asset.

### Inteleaving dimensions
Some dimensions may be interleaved. 
* For VN's the "Release version" could be under the "Logical Game Time" dimension as it would contain scenes specific to that release but falling under for instance under Act1.
* For instance the "Logical Game Specific" and the "Logical Game Mechanic" dimensions may be woven together to make it easier to handle a game specific thing. An example would be the Gnoll race going in the groups/Races folder, but containing itself the "Logical Game Mechanics" of "Units" containing Gnoll specific units like "Settlers" and "Spearman". This example would make it easy to add another race with specific units. If for instance the "Settlers" unit is the same for all races it would be better to put that in the "base" race or the "base" folder.

### Dimension Overview
1. Release version (packaging)
  * core
  * dlc
  * expansion
2. Logical Game Time based (screenplay)
  * act1
  * act2
  * act3
  * base
  * static
3. Logical Game Screenplay based (Core knowledge psychology)
  * characters (agents)
  * determinations (number calculus)
  * groups (hierargy)
  * locations (geography)
  * props (objects)
4. Logical Game Mechanic
  * Mercenaries
  * Merchant
  * Units
  * Players
  * Prisoners
  * Abilities
  * Concepts
  * Monsters
  * Nations
  * Races
  * Buildings
  * Communities
  * Occupations
  * Terrain
  * Minerals
  * Roads
  * Items
  * Spellbooks
  * Treasure
5. Logical Game Specific
 * Tauron
 * Wild Game
 * Orc Settlers
 * Gnoll Spearman
 * etc...
6. Functional
  * audio
  * image
  * model
  * text
  * video
7. Version
  * resizes
  * edits
  * blurs
  * vectorization
