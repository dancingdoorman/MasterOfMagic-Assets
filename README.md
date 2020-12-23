# MasterOfMagic-Assets
The assets for the remake of Master of Magic

The aims of the Asset repository are:
1. Use the Large File Structure (LFS) flag on the repository containing binary assets.
2. Have the asset repository used in another repository as a submodule or subtree.
3. Convert Scaled Vector Graphics (SVG) versions of the assets so the game can be scaled to any size.
4. Document the asset conversion process
5. Have a geniric folder structure based on a number of dimension that can be reused for other games

# Asset repository with LFS used by engine repository
Using a seperate repository is uncommen for amateur game development. This should document and demistify the proces.

# Pixalated Asset conversion to SVG
The conversion proces should be documented so it is repeatable for all the assets and for other pixaled games.

# Dimensions for the Folder structure
Some dimensions may be uncommon for game creators like the screenplay and Core knowledge psychology dimension.

Screenplay writers use a number of types that are usefull for games. This is more obvious for for Visual Novels (VN), but are also applicable to more mechanical games.
In developmental psychology core knowledge is defined as the knowledge people and animals are born with.
The dimensions match with the types used in screenplay writing.

## Cases when dimensions can be ommited
Some dimensions can be ommited from the folder structure, but are added here for completeness and compatibility with other games. 
* If there is only 1 release the "Release version" dimension can be ommited.
* If the game does not change in appearance during the game, for instance there is no appocalitic event wherafter all units look different, all is static and thus the "Game time" dimension can be ommited.
* If the extensions of the files are distinct enough the "Functional" dimension can be ommited.

## Some dimensions can be swaped with other dimensions based on priority
The "Version" dimension can be put higher up the structure if large swats of the assets are versioned as sets.

The "Functional" dimension can be put higher up the structure if there are seperate trees for audio, text, image and video. Because these functional items are further away from eachother treating them as a logical set is then harder. For example removing a Mercenary Hero from the game would involve traversing and removing multiple folders in the audio image and text folder structures instead of just the folder for the Mercenary Hero.

## Dimension Overview
1. Release version (packaging)
  * core
  * dlc
  * expansion
2. Game time (screenplay)
  * act1
  * act2
  * act3
  * base
  * static
3. Screenplay (Core knowledge psychology)
  * characters (agents)
  * determinations (number calculus)
  * groups (hierargy)
  * locations (geography)
  * props (objects)
4. Game Logical
  * Mercenaries
  * Merchant
  * Units
  * Players
  * Prisoners  
5. Functional
  * audio
  * image
  * model
  * text
  * video
6. Version
  * blurs
  * edits
  * resizes
  * vectorization
