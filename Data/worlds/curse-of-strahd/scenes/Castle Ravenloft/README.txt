**These instructions should help you to install, understand, and use a full, single-scene version of Castle Ravenloft inside Foundry VTT.**

**Contents**

1. Acknowledgements
2. Required Foundry Modules and Version
3. Installation
4. Art
5. Levels and Heights
6. Walls and Structure
7. Lighting
8. Extra Files


**1. Acknowledgements**
* Original Maps: Aonbarr Cartography (https://www.patreon.com/aonbarrcartography/posts). Free (at time of writing) maps for the entire CoS module.
* Compilation, map edits using https://www.gimp.org/, this README, and Foundry build: me, u/splashed_potato on Reddit.

It is my hope that the work done in putting this together remains freely accessible as a way of giving back to the community and r/curseofstrahd.

**2. Required Foundry Modules and Version**

The following modules are required:
* Levels: https://github.com/theripper93/Levels (install via Foundry), and all dependencies

No other modules should be required.

This map was built and confirmed to work using versions:
* Foundry 9.242
* DnD 5e System 1.5.7
* Levels Module 2.4.7

**3. Installation**

1. Ensure you have the required modules installed.
2. Copy the folder structure that comes packaged with this README into your Foundry data folder such that the images inside are located in "<...>/Data/maps/Ravenloft Floor Images Formatted/". If you wish to store the images elsewhere, you will need to manually update the tiles for each of the floors to point at the new locations later.
3. In Foundry, create a new, empty scene.
4. Right click on the scene and select "Import Data", then import the 'scene_data.json' file that came packaged with this README. This contains the positions and data of all walls, lights, drawings, and tiles.

Done!

**4. Art**

All art used is originally by Aonbarr Cartography. I have made the following edits:
* Reduced the image dimensions from 16000x11200 pixels to 8000x5600 pixels. This is absolutely necessary to have things run smoothly in Foundry. It's a little blurry up-close, but absolutely playable.
* Reduced the DPI from 160 to 80, again for performance reasons.
* Moved two staircases to better align with adjacent floors (see part 5 for exact details).
* Rotated some staircases to match adjacent floors.
* Cut holes in some maps so that the staircases on below floors become visible.

**5. Levels and Heights**

The levels layer tool should have the following layer values:
* B3: -90 - -61
* B2: -60 - -21
* B1: -20 - -1
* Ground: 0 - 49
* 1F: 50 - 89
* 2F: 90 - 129
* 2Fa: 100 - 109
* 2Fb: 110 - 119
* 3F: 130 - 149
* 4F: 150 - 169
* 5F: 170 - 179
* 6F: 180 - 189
* 7F: 190 - 199
* Roof: 200 - 209

Note that it may be difficult to select drawings on the B3, as there is a Levels-enabled Hole drawn over the entire map on this layer with height -90 - Infinity. This is what enables vision between floors.

Floors 2Fa and 2Fb are the second and third floors of the Instant Fortress treasury at K41.

There are some minor differences from the RAW when it comes to floor heights. The basement is directly below the main castle floor, and the southeast tower is shorter. These changes were made to ensure that (1) staircases were aligned between floors, (2) floor height felt consistent in Foundry, and (3) there are no floors which are only stairs. Otherwise, RAW heights have been preserved as much as possible.

Trying to change heights WILL likely break things!

**6. Walls and Structure**

Walls may not all be visible for a floor when viewing the floor with the wall tool. This does not mean they are not there! To improve performance, many walls stretch between multiple floors, which means they do not show up in this view. For example, the outer curtain wall is a single solid wall over Ground and 1F, rather than two stacked solid walls with one on Ground and one on 1F.

The barrier at K87 (entrance to Barov and Ravenovia's Tomb) will require the DM to drag tokens over the wall manually.

Two minor structural changes were made to RAW:
* The northeast staircase in B1 has had its directional run altered from E-E-E-N-W to E-E-S-W to make it align with the same staircase on 1F. This should not impact gameplay at all.
* The staircase K33 on 1F has been extended to cut into part of K22 on 1F to make it align with the same staircase on 2F (area K35). This change removes some space from K22, which is an archer's post with no items or story significance.

**7. Lighting**

All torchlights are tinted slightly red as a stylistic choice. The outdoor and chapel torches also have height values to ensure they are visible from other floors. The chapel (K15) and catacomb (K84) stained glass windows have coloured light sources which are configured to switch off once the darkness level hits 0.25 (as light would not pass through them at night).


**8. Extra Files**

The 'art' folder includes a bunch of art from Aonbarr Cartography which you might want to include or use as token or item art. The images included are the ones that I think go well with this map setup. There are more on the Patreon linked above. If you're adding them as tiles on the maps, then you may want to reduce them to 80 DPI using a tool like https://www.img2go.com/, to match the rest of the tiles.

I have included an entirely optional bonus macro which controls the fire colour in the brazier room. To use it, simply import it or copy its contents into a new macro and make sure that the light ID being referenced in the first line matches the ID of the light in the brazier room.

Thanks for reading this far, and good luck with your campaign! I hope many people find this map helpful :). Ping me on Reddit if you have questions -- response not guaranteed.