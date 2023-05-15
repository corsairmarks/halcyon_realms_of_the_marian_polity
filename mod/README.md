# Overview

Despite the title being about my custom empire, this mod exists mostly to offer a new origin: Early Catalytic Processing.  Begin the game with Catalytic Processing as a bonus Civic that cannot be removed.  In addition, you get my light role-play empire (that uses this origin), the Halcyon Realms of the Marian Polity.

Origin: Early Catalytic Processing requires the Plantoid Species Pack.  The custom empire Halcyon Realms of the Marian Polity also requires Leviathans (for the portrait) and the Aquatic Species Pack (Aquatic trait and city art).  The variant custom empire Prosperous Domains of the Marian Corporation additionally requires MegaCorp and the Humanoid Species Pack.  You can use the origin without any DLC requirements other than the Plantoids Species Pack, however the custom empires will be unavailable.

# Changes

Adds a pre-scripted empire, the Halcyon Realms of the Marian Polity.  They are a peaceful, inward-facing society of agrarian molluscoids.  Yes, everyone has a version of farmer-snails and this one is mine.  The Mari are heavily focused on the production of agricultural products - their mineral-poor homeworld lead them to develop and depend on Catalytic Processing much earlier in their history than other empires.  In order to add this gameplay quirk, this mod adds Origin: Early Catalytic Processing that is used by the Mari but is also available for your own custom empires (except with Mining Guilds/Rockbreakers).

Origin: Early Catalytic Processing adds four "new" Civics that are effectively duplicates of the built-in Catalytic Processing Civics.  These duplicates allow the same job switch as the built-in Civics, but are not able to be removed and grant a bonus Civic slot to account for being forced to have the Civic.

Origin: Early Catalytic Processing automatically adds the Authority-appropriate Early Catalytic Processing civic to relevant empires during galaxy generation/game setup, but imposes a heavy food-to-alloy conversion penalty.  This penalty can be reduced, eliminated, and eventually replaced with an efficiency bonus through special technologies only available to empires with Origin: Early Catalytic Processing.

## Localisation

* English by corsairmarks (author)
* Japanese by Dryus: [[JP localize patch]Corsair's Custom Empires: Halcyon Realms of the Marian Polity](https://steamcommunity.com/workshop/filedetails/?id=2680360959) (sub-mod)

## Compatibility

In order to implement its changes, this mod overwrites one trigger from base Stellaris: `is_catalytic_empire`.  This trigger is used in a variety of places to determine Catalytic Technician/Drone job switches and a few other related setup effects.  This mod is not compatible with other mods that want to overwrite this same trigger, but should otherwise place nicely with most mods.

Built for Stellaris version 3.8 "Gemini."  Not compatible with achievements.

### When to Install

This mod should be added before starting a new game, and should not be removed from games in progress.  You can technically add it after starting a game, but you'll miss out on all of its effects.  Losing access to the new civics or technologies could cause problems if removed after game start.

### Recommended Companion Mods

* ["Agrarian" Idyll for Lithoids](https://steamcommunity.com/sharedfiles/filedetails/?id=2510669821) is not _just_ for Lithoids - this mod also adds (partial) Building Slots to Agrarian Idyll empires for their rural districts (mining/generator/agriculture), such as the Halcyon Realms of the Marian Polity.  That means you can obtain building slots while avoiding City districts, as the role-play for Agrarian Idyll heavily implies.
* [Eldanær Stellar Authority](https://steamcommunity.com/sharedfiles/filedetails/?id=2496360535) is another custom empire that I created.  More gameplay mechanics than the Mari, including a special colossus weapon just for Fungoid Necrophages.

## Known Issues

This mod overwrites one built-in Stellaris trigger in order to make empires with the new origin and duplicated civics count as "catalytic empires."  Expect to see one error in your error.log similar to this:

```
[15:38:58][game_singleobjectdatabase.h:165]: Object with key: is_catalytic_empire already exists, using the one at  file: common/scripted_triggers/01_halcyon_realms_of_the_marian_polity_scripted_trigger_overrides.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Properly gate custom empire behind its DLC requirements
* 2.0.0 Update for compatibility with Stellaris 3.2 "Herbert"
    * The Mari are now Aquatic, reflecting the description in their species bio
    * To have the 1-point Aquatic trait, the Mari are no longer Traditional (the bonus was only to jobs anyway)
    * The Halcyon Realms of the Marian Polity now uses the Aquatic cities
    * Playing the Halcyon Realms of the Marian Polity now requires the Aquatic Species Pack
* 2.1.0 Add a megacorp variant of the Mari: the Prosperous Domains of the Marian Corporation
* 3.0.0 Update for compatibility with Stellaris 3.3 "Libra" - no functionality changes
* 4.0.0 Update for compatibility with Stellaris 3.4 "Cepheus" - no functionality changes
* 5.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Adjust prescripted empires to account for trait price increase for Aquatic (swap Solitary for Unruly)
    * Include the Mindful trait for removal in the custom leader scripting
* 6.0.0 Add a compatibility trigger for other mods to check whether this one is active, remove old compatibility global flag
* 6.1.0 Ensure that non-megacorps with Origin: Early Catalytic Processing can reform into megacorps, and vice-versa
* 7.0.0 Update for Stellaris version 3.7 "Canis Minor" - integrate underlying game changes
* 8.0.0 Update for Stellaris version 3.8 "Gemini"
    * Adjust custom scripting for new leader system
    * Add councilor positions for Early Catalytic Processing (they duplicate the councilor positions for regular Catalytic Processing)
    * The Halcyon Realms of the Marian Polity has traded Civic: Inward Perfection for Civic: Anglers - they still view the greater galaxy with suspicion, but are no longer focused exclusively inward
    * Integrate underlying changes for technologies
* 8.0.1 Early Catalytic Processing empires don't get to unlock an extra councilor early

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/halcyon_realms_of_the_marian_polity)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.