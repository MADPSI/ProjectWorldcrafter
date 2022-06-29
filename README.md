# Overview
Project **Worldcrafter** is a multi-layered modification to the Adventure Editor, which provides considerably more creative freedom than the default experience. The mod consists of, at present, three components: 

### Core
The project Core contains the majority of the changes, being the only package that is absolutely required. Among its features: 
* Modifies most placeable objects to greatly increase the range to which they can be scaled. 
  * Creatures, Vehicles, Buildings, Gameplay Objects, Sounds, Effects and Terrain Stamps can now be scaled from 0.001% to effectively infinitely large, though in the case of physical objects, they must still remain within the atmospheric height limit.
    * For Sounds, the maximum range at which they can be heard has been extended to encompass the entire playable planet and likely most of the surrounding void.
    * Effects can likewise be scaled to effectively infinite size, but due to the fact that the properties governing Level of Detail are compiled into the effect files themselves instead of the associated playable object, the limit at which the effect derenders remains the same.
    * Decal Stamps like Plazas tend to be cut off by the seams of the planet, of which there are twelve, due to the planet being a round-faced cuboid.
    * Terrain Stamps can be scaled infinitely, and the intensity that governs the resulting height or depth of the deformation has been vastly extended. Maximum Height and Depth is still limited independently by a seperate file, which cannot be modified exclusively for Adventures, instead affecting all generated planets throughout the game, and therefor is not included in this version.
  * Fixed Objects have not been modified due to inconsistent but pervasive crashes. For now, this can be solved by disguising an infinitely scaleable Gate Gameplay Object as one of these Objects, though this method unfortunately sacrifices certain kinds of attached effects.
* Extends the Complexity of Build Mode, more than doubling the amount of placeable assets and essentially removes Complexity from Terraforming Mode, allowing practically limitless placement of Terrain Stamps. Complete removal of the Build Mode Complexity Limit remains evasive, the upper limits of infinite Terrain modification remain unclear.
* Allows Gameplay Objects to be Disguised as more types of creations, including Creatures, Cells and other Gameplay Objects. Cells possess strange rendering properties, Gameplay Objects lack effects and, in the case of gates, render oddly.
  * The Mine has had its default Damage reduced to 0.01%, which _does_ damage the captain's health (which supports decimals despite not displaying them) but not in a visible way. This can be used to force the captain out of sneak or create trigger systems without causing significant damage. Once changed, the Damage of the mine cannot be set back to 0.01%, requiring the player to re-add the mine to the palette to reset its properties.
* Unpublished adventures now default to having 100 Sporepoints as a way to circumvent the zero plays bug requiring one to grind dozens if not hundreds of Adventures to reach Captain Level 10.

### Camera
The mod includes a toggleable component to alter the limitations of the Play Mode Camera. Zoom distances have been greatly increased to allow a planetary view at maximum distance, and at minimum distance, the camera can be zoomed in to the captain's model, which due to alpha detection becomes invisible, allowing for a barebones first-person experience. Zooming into the creature has been known to cause a glitch where the camera switches to a lower pivot point, the cause for which is currently unknown. These changes do not affect Freecam mode (enabled with Ctrl+Alt+C).

### Objects
The mod also adds a toggleable component that introduces several experimental Gameplay Objects with a variety of useful features. These objects cannot, unfortunately, be shared, being replaced by placeholders when attempting to do so. Among them you have:
* An intangible, disguiseable object that functions in a manner similar to a Gate, but without collisions and being unaffected by Keys. Useful for shrubery that the player is intended to walk through.
* A pickup-able, disguiseable object that functions similarly to a Key, but cannot be used to interact with Gates. It can however still be thrown at or gifted to creatures.
* A selectable, indestructible object that works much like a Crate or Explosive Barrel, but is entirely invincible. Useful as a sort of bullseye for targeting without destroying.
* A solid, disguiseable object, which like the intangible variant acts like a Gate, except unable to interact with Keys while maintaining collision.
* An Open Gate model placed under Fixed Objects.

## Credits:
* ERROR! / Metalblaze - Testing.
* Derezzed - Testing.
* Klaracbarack - Testing.
* ThePlantGuy - Testing.
* Liskomato - Testing, _successfully_ implementing extended palette slots into their own mod. Check it out here (link pending)

## Changelog
* **Version 1.0.0**. Initial GitHub upload.
 * Fixed Dirt Plaza 1 being replaced with Lava Pit
 * Updated package signatures after inadvertently resetting them
 * Fixed Open Gate Fixed Object missing rotating Palette model
