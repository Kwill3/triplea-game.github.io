---
layout: page
title: Release Notes
permalink: /release_notes/
---

## [2.5.22285](https://github.com/triplea-game/triplea/releases/tag/2.5.22285) Nov 1, 2020

|[#8057](https://github.com/triplea-game/triplea/pull/8057)|FIX|Increase window size to prevent chat message panel from being squished and rendering too small|
|[#8049](https://github.com/triplea-game/triplea/pull/8049)|FIX|Avoid game crash during game selection when maps are missing required XML data|
|[#8048](https://github.com/triplea-game/triplea/pull/8048)|FIX|Fix potential freeze when starting large save games in lobby.|
|[#8031](https://github.com/triplea-game/triplea/pull/8031)|FIX|Map parsing errors will be more gracefully handled, will no longer crash the game and will print the name of the map that generated the error.|
|[#8023](https://github.com/triplea-game/triplea/pull/8023)|FIX|World War 2 Global will correctly switch unit ownership of units placed in India from UK_Pacific to British.|


## [2.4.22192](https://github.com/triplea-game/triplea/releases/tag/2.4.22192) Oct 29, 2020

|[#8002](https://github.com/triplea-game/triplea/pull/8002)|FIX|Fix error during AI games or battle calculator for maps that have "Submarines Defending May Submerge Or Retreat" set to true and "Submersible Subs" set to false (EG: world_war_ii_classic and classic_variations).|
|[#8000](https://github.com/triplea-game/triplea/pull/8000)|FIX|Default Order of Loss will now take into account support from all units in the battle.|
|[#7979](https://github.com/triplea-game/triplea/pull/7979)|FIX|Prevent unlikely infinite battle calculations, battle calculations now limited to 10,000 rounds|
|[#7948](https://github.com/triplea-game/triplea/pull/7948)|CHANGE|A battle that only contains units that can not hit each other because of canNotTarget and canNotBeTargetedBy will result in a stalemate.|

## [2.3.22161](https://github.com/triplea-game/triplea/releases/tag/2.3.22161) Oct 27, 2020

|[#7631](https://github.com/triplea-game/triplea/pull/7631)|FEATURE|Build in support to be able to load (most) 1.8 maps. 1.8 "variant" maps will not work, though most others should now load without issue.|
|[#7899](https://github.com/triplea-game/triplea/pull/7899)|UPDATE|Removed from "infrastructure" units the ability to be immune to targeted (AA-like) fire and made infrastructures targetable also beyond the first round of combat (in accordance to the fact that TripleA allows infrastructures to remain in combat beyond the first round).|
|[#7876](https://github.com/triplea-game/triplea/pull/7876)|UPDATE|Loading saves from newer game engine versions will require you to upgrade your game engine version. This is to avoid subtle errors and other rule problems that could occur. |
|[#7894](https://github.com/triplea-game/triplea/pull/7894)|NEW|Add option in 'test settings' for testing to force load any game, ignoring compatibility|
|[#7823](https://github.com/triplea-game/triplea/pull/7823)|UPDATE|Battle UI step labels have been updated to be more specific|
|[#7704](https://github.com/triplea-game/triplea/pull/7704)|UPDATE|Escape key now closes the 'select map' window|
|[#7693](https://github.com/triplea-game/triplea/pull/7693)|UPDATE|Improve performance of the 'available maps' button and startup time for bot servers|
|[#7637](https://github.com/triplea-game/triplea/pull/7637)|UPDATE|Generate an unlimited number of default player colors when player colors are not specified in map.properties. Use default color '#DEB887' for the 'impassable' player color if not specified in map.properties.|
|[#7617](https://github.com/triplea-game/triplea/pull/7617)|UPDATE|Map XMLs can now be located anywhere in a map zip or map directory, for example they can now be in a sub-directory of the 'games' folder.|
|[#7596](https://github.com/triplea-game/triplea/pull/7596)|UPDATE|Map XML parser re-written to allow for more flexible XML structure. The XML DTD is no longer checked or used.|
|[#7585](https://github.com/triplea-game/triplea/pull/7585)|UPDATE|Improved map loading performance (about 3x times faster)|
|[#7834](https://github.com/triplea-game/triplea/pull/7834)|FIX|Hard AI purchases factories/constructions again|
|[#7767](https://github.com/triplea-game/triplea/pull/7767)|FIX|Non-amphibious units selected for AI casualties after similar amphibious units.|
|[#7765](https://github.com/triplea-game/triplea/pull/7765)|FIX|Air Transported units in no longer cause battle errors in Warcraft: War Heroes|
|[#7723](https://github.com/triplea-game/triplea/pull/7723)|FIX|Defending subs can now submerge if "Submarines Defending May Submerge Or Retreat" is true even if there are no other retreat territories.|
|[#7611](https://github.com/triplea-game/triplea/pull/7611)|FIX|Fix errors on game start when the last played map is deleted on disk.|
|[#7602](https://github.com/triplea-game/triplea/pull/7602)|FIX|Disable sound options instead of showing an error message if there is no sound on the installed system.|
|[#7598](https://github.com/triplea-game/triplea/pull/7598)|FIX|Fix rare ConcurrentModificationException game crash when loading save games|
|[#7528](https://github.com/triplea-game/triplea/pull/7528)|REMOVE|Remove XML 'color' property option|
|[#7518](https://github.com/triplea-game/triplea/pull/7518)|REMOVE|Remove unused and unsupported game XML tag 'removeConnection'|
|[#7500](https://github.com/triplea-game/triplea/pull/7500)|REMOVE|Remove feature to define maps as grid-based, remove unused {map:grid} XML element|
|[#7437](https://github.com/triplea-game/triplea/pull/7437)|REMOVE|Removed GPG signing of installer files (GPG signatures will no longer appear in github releases)|


## [2.2.20868](https://github.com/triplea-game/triplea/releases/tag/2.2.20868) Aug 22, 2020

|[#7419](https://github.com/triplea-game/triplea/pull/7419)|FIX|Movement incorrectly disallowed into certain territories on WaW |


## [2.2.20790](https://github.com/triplea-game/triplea/releases/tag/2.2.20790) Aug 12, 2020

|[#7292](https://github.com/triplea-game/triplea/pull/7292)|FIX|Fixed an issue where rarely a NonMonotonicSequenceException  could occur when planning moves|
|[#7269](https://github.com/triplea-game/triplea/pull/7269)|FIX|Fix null error in AddUnits#buildUnitOwnerMap when loading a saved game|
|[#7262](https://github.com/triplea-game/triplea/pull/7262)|FIX|Improve server launching to better handle startup errors, prevents a 'stuck' server state.|
|[#7249](https://github.com/triplea-game/triplea/pull/7249)|FIX|Reduce memory usage when loading the 'Unit Help' menu|
|[#7245](https://github.com/triplea-game/triplea/pull/7245)|UPDATE|Hidden map units are no longer counted in player stats|
|[#7243](https://github.com/triplea-game/triplea/pull/7243)|FIX|Rare date parser error on game launch when checking for out-of-date maps|
|[#7241](https://github.com/triplea-game/triplea/pull/7241)|UPDATE|About menu is replaced with a link to the game license.|
|[#7227](https://github.com/triplea-game/triplea/pull/7227)|FIX|Disabling 'Air Attack Sub Restricted' in Map Options will correctly allow airplanes to hit subs.|
|[#7217](https://github.com/triplea-game/triplea/pull/7217)|FIX|Missing unit error message for Warcraft War Heroes when a unit dies and is turned into XP should no longer occur.|
|[#7148](https://github.com/triplea-game/triplea/pull/7148)|UPDATE|Improve minimap rendering performance to be faster and use less memory|
|[#7143](https://github.com/triplea-game/triplea/pull/7143)|UPDATE|Error report uploads will now automatically include map name and memory usage details|
|[#7070](https://github.com/triplea-game/triplea/pull/7070)|FIX|Potential game crash during calculation of units that belong in the units-to-place panel|
|[#7064](https://github.com/triplea-game/triplea/pull/7064)|UPDATE|Unit Missing error will now indicate which image is actually missing|
|[#7060](https://github.com/triplea-game/triplea/pull/7060)|FIX|MISSING UNIT IMAGE error for kamikaze units will no longer show up on Big World|
|[#7030](https://github.com/triplea-game/triplea/pull/7030)|FIX|Fixes combat window sizing with Windows 10 magnification|
|[#7022](https://github.com/triplea-game/triplea/pull/7022)|FIX|Warcraft War Heroes no longer errors with "sortedTargetsToPickFrom" must have the same size as targetsToPickFrom list|
|[#7018](https://github.com/triplea-game/triplea/pull/7018)|FIX|AI no longer crashes when determining if a territory with a submerged sub can be held.|
|[#7007](https://github.com/triplea-game/triplea/pull/7007)|FIX|Submerged subs don't retreat when other units retreat|


## [2.1.20365](https://github.com/triplea-game/triplea/releases/tag/2.1.20365) July 1, 2020

|[#6984](https://github.com/triplea-game/triplea/pull/6984)|UPDATE|Error uploads will now recognize duplicates and give you a link to an existing error upload if there is one. Added 'map-name' as an error upload field|
|[#6978](https://github.com/triplea-game/triplea/pull/6978)|FIX|Fix lobby chat to break on word boundaries|
|[#6970](https://github.com/triplea-game/triplea/pull/6970)|FIX|TWW will no longer crash before Germany's non-combat phase.|
|[#6943](https://github.com/triplea-game/triplea/pull/6943)|FIX|PlayerOwnerChange exception in Warcraft War Heroes is fixed|
|[#6937](https://github.com/triplea-game/triplea/pull/6937)|FIX|Fix URI syntax error triggered in PBF when a forum username contains a space|
|[#6897](https://github.com/triplea-game/triplea/pull/6897)|FIX|Trenches getting invalid first strike on defense in Domination 1914 fixed.|
|[#6885](https://github.com/triplea-game/triplea/pull/6885)|FIX|Attacking a sub unit with a destroyer unit in a map with no air units will no longer throw an error.|
|[#6879](https://github.com/triplea-game/triplea/pull/6879)|FIX|MARTI dice rolls where the first die has multiple digits are now parsed correctly|
|[#6864](https://github.com/triplea-game/triplea/pull/6864)|FIX|Fix remember password feature for play-by-forum|
|[#6851](https://github.com/triplea-game/triplea/pull/6851)|FIX|Potential error when AI is calculating transport movement|
|[#6842](https://github.com/triplea-game/triplea/pull/6842)|CHANGE|Missing Unit Image error now indicates if image should be a damaged and/or disabled image|
|[#6814](https://github.com/triplea-game/triplea/pull/6814)|FIX|Game crash when calculating a sea battle with units that can bombard|


## [2.0.20234](https://github.com/triplea-game/triplea/releases/tag/2.0.20234) June 24, 2020

|[#6802](https://github.com/triplea-game/triplea/pull/6802)|FIX|Make lobby player listing sort order be case insensitive|
|[#6801](https://github.com/triplea-game/triplea/pull/6801)|FIX|Fix NPE possible when AI is evaluating naval bombardment|
|[#6800](https://github.com/triplea-game/triplea/pull/6800)|FIX|Fix UnsupportedOperationException during battle phase possible when fighters are transported as cargo|
|[#6793](https://github.com/triplea-game/triplea/pull/6793)|CHANGE|Improve bot logging of which maps are loaded|
|[#6780](https://github.com/triplea-game/triplea/pull/6780)|FIX|Fix forum posting formatting regression reported in #6735|


## [2.0.20183](https://github.com/triplea-game/triplea/releases/tag/2.0.20183) June 22, 2020

- Fixed: Map listing may not render if default game is blank
- Fixed: Can encounter error if deprecated costPU is still present
on a map, possible if maps are not updated
- Fixed: Can encounter NPE in game selector initialization
if default game is missing or errors out (due to costPU for example)

## [2.0.20123](https://github.com/triplea-game/triplea/releases/tag/2.0.20123)

| Engine  | Feature | Automatic bug reporting, dialog to upload error logs appears when a game error occur  |
| Engine  | Feature | New placements panel shows units that have been purchased |
| Engine  | Feature | New units-to-move panel shows units that can be moved in current territory and how many units are left to move |
| | | Use ',' and '.' to select next and previous unit, 'space' to skip units and 's' to sleep units |
| Engine  | Feature | Ctrl+Enter hotkey has been added for the 'done' buttons |
| Lobby   | Feature | Can right click players in lobby chat to see when they registered|
| Lobby   | Feature | Lobby account menu has a change name option |
| Lobby   | Feature | New 'forgot password' option available when logging in |
| Map XML | Feature | Add nested foreach to attachments (#4831) |
| Map XML | Feature | Add XML variables and foreach (#4791) |
| Map XML | Feature | Add new canal option canNotMoveThroughDuringCombatMove (#4816) |
| Map XML | Feature | Add new player option giveUnitControlInAllTerritories (#4808) |
| Map XML | Feature | Add onlyRepairIfDisabled phase option (#4775) |
| Map XML | Feature | Add option 'canRetreatOnStalemate' to configure if zero power units vs zero power units gives attacker the option to retreat (#6500) |
| Staging Screens | Update | Display Java version on main screen (#4415) |
| Staging Screens | Update | Split PBEM/PBF to two different screens |
| Lobby   | Update  | Lobby rewritten from the ground-up, technology upgrade |
| Lobby   | Update  | Empty Bot hosts will appear as 'available' instead of 'waiting for players' |
| Lobby   | Update  | Improvements to banning and ban messaging |
| Lobby   | Update  | Slap messages are displayed to all |
| Lobby   | Update  | Account passwords now must be at least 5 characters long |
| Map XML | Update  | Divide isSub into Attributes (#4831) |
| AI      | Update  | Various performance improvements |
| PBEM    | Update  | (PBEM) Allow posting from after purchase phase (#4770) |
| AI      | Fix     | Improve large map performance (#4764) |
| AI      | Fix     | Fix battle results when checking for submerging (#4738) |
| Rules   | Fix     | Don't allow transports to load after being in battle if LHTR (#4857) |
| Rules   | Fix     | Allow attacker to withdraw before defender submerges for revised rules (#4820) | 
| Rules   | Fix     | Fix New Fighters On Old Carriers To Ignore Allied/Enemy Carriers (#4508) |
| Rules   | Fix     | Fix Land Scramble Error by preventing a route to/from the same territory (#4494) |
| Engine  | Fix     | Hotkey fixed so game post and players tab no longer use the same hotkey |
| Engine  | Fix     | Hover over unit tooltip works consistently (#4853) |
| Engine  | Fix     | Fix current player logic in battle simulator when history is open (#4828) |
| Engine  | Fix     | Fix undo blitz battles (#4813) |
| Engine  | Fix     | Fixed various memory leaks (#4806) |
| Engine  | Fix     | Battle calc fixes and improvements (#4576) |
| Engine  | Fix     | Ensure XXE security fix (#4516) |
| Engine  | Fix     | Map download screen - Display map size downloaded so far when total map size is unknown (#4515) |
| Engine  | Fix     | Auto Kill logic looking at attack value rather than defense (#4409) |
| Engine  | Fix     | Improve route finding to consider friendly and requiresUnits (#4498) |
| Lobby   | Fix     | 'Ghost games' should no longer be a problem |
| Map XML | Fix     | Allow whenHitPointsDamagedChangesInto to work for units with no HP left (#4720) |
| Engine  | Remove  | Drop game host mute ability (#4783) |
| Map XML | Remove  | Remove deprecated costPu option as all maps have been updated (#4493) |

## [1.9.0.0.13066](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.13066) - November 18th 2018

* Fix determination of transported units during amphibious assaults (#4252)
* Use dynamic heap size for installers to fix Windows 32 bit installer (#4328)
* Add check for sea units to enemySurfaceExclusionTerritories to fix surface warship objectives (#4351)
* Update A&A forum poster for new forum (#4361)

## [1.9.0.0.12226](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.12226) - September 28th 2018

* Allow Option for Unit Overflow to Left Instead of Right: https://forums.triplea-game.org/topic/680/allow-option-for-unit-overflow-to-left-instead-of-right
* Group and Sort Units onto Placements Logically: https://forums.triplea-game.org/topic/681/group-and-sort-units-onto-placements-logically
* Improve Hotkeys: https://forums.triplea-game.org/topic/690/improve-hotkeys
* Improve Resources Tab: https://forums.triplea-game.org/topic/702/improve-resources-tab
* Display Territory Naval Base and Air Base Info: https://forums.triplea-game.org/topic/678/territory-naval-base-and-air-base-info
* Support Loading Unzipped Maps From In-game Downloads: https://forums.triplea-game.org/topic/706/loading-unzipped-map-from-in-game-download
* Allow 0 cost unit production rules: https://forums.triplea-game.org/topic/758/zero-cost-production
* AI - Improved Neutral Categorization: https://forums.triplea-game.org/topic/776/ai-improve-neutral-categorization
* AI - Add Support for Land Transporting Units: https://github.com/triplea-game/triplea/pull/3439
* PBF/PBEM - need indication when the game play is connected to a verified dice roller: https://github.com/triplea-game/triplea/pull/3441
* Unit Icons Added By Conditions: https://forums.triplea-game.org/topic/882/unit-icons-added-by-conditions
* Add Small Map Properties: https://forums.triplea-game.org/topic/887/mini-me-map-options
* Add Resources Cost to User and Political Actions: https://forums.triplea-game.org/topic/418/expand-useractionattachment-politicalactionattachment-to-all-resources
* Remove AA attack limit of half dice side value: https://github.com/triplea-game/triplea/pull/3489
* AI - Place triggered sea units: https://github.com/triplea-game/triplea/pull/3542
* Add Unit count and damage display outline: https://forums.triplea-game.org/topic/917/unit-count-and-damage-display-outline
* Allow political notifications to only targets (Feudal Japan): https://github.com/triplea-game/triplea/issues/3558
* Add Unit Tooltips: https://github.com/triplea-game/triplea/pull/3477
* Include Dice Stats from Save Game: https://github.com/triplea-game/triplea/issues/3478
* Improve Route Finder to Consider Territory Effects: https://forums.triplea-game.org/topic/945/improve-route-finder-to-consider-territory-effects
* AI - place units on non infra factories: https://github.com/triplea-game/triplea/pull/3645
* Unit Tooltip Improvements & Poll: https://forums.triplea-game.org/topic/942/unit-tooltip-improvements-poll
* Add Support for Land Transports Moving Through Canals: https://forums.triplea-game.org/topic/984/add-support-for-land-transports-moving-through-canals
* Enhance Route Finding To Consider Canals: https://forums.triplea-game.org/topic/1007/enhance-route-finding-to-consider-canals

## [1.9.0.0.9687](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.9687) - March 12th 2018

### Added
* Unit option fuelFlatCost (#3244)
* Resources and territory effects icon support (#3118)
* XML resource property isDisplayedFor (#3034)
* Estimate player income (#3033)
* Player resource bar (#3013)
* Unit property and logic for whenCapturedSustainsDamage (#2989)
* Check so disabled units can't move (#2988)
* Property to allow loading in hostile sea zones (#2984)
* Hit differential detail (#2807)
* Setting to always show console when any output is written (#2705)
* Unit repaired changes into (#2691)
* Unit option for when hit points damaged changes into (#2689)
* MARTI staging server to dice server list (#2685)
* Capacity for land transports (#2673)

### Changed
* Enhance route message with background and fuel costs (#3189)
* Improve settings window layout (#2952)
* Upgrade license to GPL-3.0-or-later (#2949)
* Update battle calculator unit ordering (#2941)
* Remove give map feedback feature (#2927)
* Use minimum size instead of size for battle frame (#2839)
* Error messages pop-up shown instead of error console. A 'view details' button can be clicked to see the error console with full details. (#2782)
* Use latest Substance L&F library (#2680)
* Remove War Club play-by-forum (#2669)

### Fixed
* Lock not held exceptions in various use cases (#3174, #3212)
* Infinite loop when unable to parse default map (#3036)
* Lobby divider location on resize (#2998)
* NullPointerException when closing game (#2997)
* Undo bombing change that should set previous bombing not HP damage (#2990)
* Non-deterministic ordering of political action roundels (#2978)
* Incorrect TUV in battle calculator when retreating (#2970)
* Code that is adding paratroopers to a second transport (#2825)
* Casualty selection window size (#2813)
* Exception when lobby host override set but port override not set (#2771)
* Table rendering of start time in lobby (#2718)
* Exception when assigning a default color to a player (#2704)
* Chat message history navigation keys (#2654)
* Prompt to download Tutorial map (#2650)

## [1.9.0.0.7621](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.7621) - November 25th 2017

### Added
* Wait indicator while loading default map at startup (#2573)
* Wait indicator while parsing maps (#2572)

### Changed
* Parse maps in parallel (#2571, #2572)

### Fixed
* Air units not able to attack after being transported by allied carrier (#2634)
* Unexpected hits to multi-hit units in Hard AI games (#2617)
* Slow battle calculator in network games (#2617)
* Bot crash when joining game (#2610)
* History reflection attachment calls (#2607)
* Combat client settings (#2599)
* Hotmail PBEM (#2598)
* Game crash when attacking neutral territories (#2596)

## [1.9.0.0.7378](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.7378) - November 5th 2017

### Added
* Support for dice image "0" (#2561)

### Changed
* Only check non-transported units for requiresUnitToMove (#2560)

## [1.9.0.0.7342](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.7342) - November 1st 2017

### Added
* Wait indicator during lobby login (#2548)

### Changed
* Reduced default simulation run counts (#2531)

### Fixed
* Slow battle calculator (#2544)
* Map blend rendering when zoom < 100% (#2542)

## [1.9.0.0.7062](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.7062) - October 11th 2017

### Added
* 'Remember me' option when logging in to lobby, credentials are securely saved on your computer (#2395)
* Option to securely save PBEM/PBF credentials (#1955)
* Buttons to select alliances more easily in single-player mode

### Changed
* Upgraded retreat options - no double prompt with one valid territory
  * Don't offer prompt when only defenseless units remain
* Game play speedup, automatically select a single battle for combat
* Game play speedup, automatically select defenseless unit battles first (e.g. when selecting battles to fight, all battles against undefended transports would be auto-selected first)
* Overhauled Settings Window available from the file menu (#2137)
* Show dice details is now a default option in PBF/PBEM
* Enabled TripleA to download Maps via a browser (#2274)
* Associated TripleA savegames with TripleA at the OS level when running the installer
* Improved naming of auto save games
* Improved internal password security (#2101)
* Improved security of network game authentication (#2107)

### Fixed
* Console opening when playing a network game (#2289)
* Threading errors reported when starting Map Creator (#2238)
* Out-of-date map check (#1695)
* Maps so they can have AI-only players (#2149)
* Many outdated game links
* Game crash when game release version is updated

### Removed
* Beta Map Creator (#2156)
* 'Old jar' functionality (#2284)

And many more internal changes, bugfixes, etc.

## [1.9.0.0.3635](https://github.com/triplea-game/triplea/releases/tag/1.9.0.0.3635) - January 21st 2017

* Game no longer shuts down when host disconnects, allows game to be saved.
* All rocket targets are now selected before dice are rolled.
* Removed non-default 'brute force' casualty selection option

## 1.9.0.0.3566

* SBR and air battles now fought at the beginning of combat automatically
* Progress indicator added to the 'map snapshot' feature

## 1.9.0.0.3453

* Primarily bug fixes. SBR rules now working again on most maps (map XMLs updated, download of latest maps required)


* Minimum Java version is now Java 1.8
* New Install4j Installers available for all OS, replaces makensis installers
* Wav audio files have been converted to mp3, reducing game and map download size. Support for wav files has been dropped.
* An updated, beta version, map creator has been added, available from the engine settings menu from the main launch screen
* Removing all "Grid" games (Chess, Checkers, Go, Kings Table) as well as inaccessible puzzle games (N-Puzzle and Tic-Tac-Toe).
* Performance improvement, bot servers will use less CPU, games will start faster

### Game Rule Updates
* Updated canals to check if at least 1 canal is passable between any two sea territories, rather than checking that every canal is passable

### Game Engine UI and Behavior
* Combat window auto-continues after a short delay when a dice roll results in all misses, or all units hit
* Improved missing map behavior when joining games, the game will still crash, but instead of an error message there is now a prompt asking if you would like to download the missing map. Clicking 'yes' will begin the missing map download.
* A new settings window is availabe from the game menu, some settings options have been moved there, and some new ones made available.
* Unit route drawing updated to draw smoother routes, with arrows at the end of the route line to indicate move direction.
* Add total army unit count to the TerritoryPanel
* Main screen now shows the Engine Version
* Core game settings consolidated and are now defined in a 'game_engine.properties'. The file controls game engine version and lobby URL
* New option to draw nation mini-flags next to, or underneath units
* Pressing the 'u' key while hovering over moved units will undo the move (note, there is a bug where the map loses key focus in multiplayer games, to work around this, click the map first and then the 'u' key will work: [View issue Ticket](https://github.com/triplea-game/triplea/issues/305))

### AI Changes

* AI will now do strategic bombing
* AI - Added check for whether factories can be placed to purchase
* AI - consider enemy turn order
* AI - consider multi-nation attacks
* AI - Add new Fast AI player, similar to Strong AI, but uses a simplified combat simulation to improve processing speed
* AI - Add capital value for amphib attacks
* AI - remove strong AI
* AI - Update casualty selection unit value calculation to consider

### Map Changes
* Map Download Overhaul - Tabbed View with progress bars, can remove downloaded maps from the download window, and a game restart is no longer required to play new maps
* Maps have been moved to Github, they will download faster, and map development can now be done with far less administrative support.
* Game engine will pick up map 'clones' from the downloaded maps folder. This means you can clone a map repo directly in the download maps, update it, play it, and then you can commit and push the changes to then update the main map repo. Map makers should no longer have to do any map zipping or unzipping.

### Bug Fixes
* Bugfix - 'delete corrupt map' game crash when the confirmation dialog window was shown
* Bugfix - edit menu select nation now has scrollbars when there is a long nation list


## Changes for 1.8.0.9

* Bug fix, retreat from naval combat was not possible, now fixed. (redrum)
* Fixed possible infinite loop bug when a corrupt map exists in the map downloads, PR#76\. (lafayette)
* Increase scroll speed when using arrow keys. Holding down control speeds up arrow key scroll. (lafayette)
* Placing cursor next to the very edge of the map increases scroll speed. (lafayette)
* Hard AI - Fixed calculating defenses on maps with air/naval bases to properly calculate enemy range. (redrum)
* Hard AI - Fixed bug around not defending against enemy units that were transported the previous turn as they were being marked as already transported when potential enemy attacks were calculated. (redrum)

## Changes for 1.8.0.7

* Hard AI - Improved performance on large maps. (redrum)
* Hard AI - Added support for valuing exposed units when attacking. (redrum)
* Hard AI - Improved air units landing safely. (redrum)
* Hard AI - Added scrambling support. (redrum)
* Hard AI - Improved transport movement and defense. (redrum)
* Hard AI - Added support for purchasing and landing on carriers. (redrum)
* Hard AI - Improved naval non-combat move and avoid sea units getting stuck. (redrum)
* Hard AI - Improved casualty selection to consider unit cost. (redrum)
* Hard AI - Added unit support attachment consideration for purchasing and movement. (redrum)
* Hard AI - Added politics support for 2 team maps such as Global 1940\. (redrum)
* Hard AI - Improved capital defense. (redrum)
* Hard AI - Added support for WW2v1 non-limit placing of units. (redrum)
* Hard AI - Added support for territory effects. (redrum)
* Hard AI - Added support for China on WW2v3\. (redrum)
* Hard AI - Added support for unit placement limits. (redrum)
* Hard AI - Fixed sorting bug causing error: Comparison method violates its general contract. (redrum)
* Hard AI - Improved carrier/fighter casualty sorting to avoid leaving fighters stranded. (redrum)
* Hard AI - Units of the same type are now moved all at once rather than one at a time. (redrum)
* Hard AI - Fixed several rare NullPointerException errors. (redrum)
* Hard AI - Added support for nations without capitals. (redrum)
* Source code migrated to github - [GitHub Repository](https://github.com/triplea-game/triplea) (veqryn)
* Fixed maxBuilt to include unplaced units, PR#62\. (LaFayette)
* Added a convenience button to undo all moves during a phase, PR#61\. (LaFayette)
* Removed obsolete Dynamix (land-only) AI. (veqryn)
* Fixed issue with TripleA logging users out of axisandallies.org when posting turns. (redrum)
* Fixed bug with movement validation for fighters launching from a carrier and flying into enemy land territory then returning. (veqryn)
* Bug fixes on unit casualty sorters, and switching approximate method in as the default. (veqryn)
* Created a new prototype unit sorter for quicker approximate sorting, including support attachments. (redrum)

## Changes for 1.8.0.5

* Created a prototype unit sorter for sorting units with support attachments (still in beta) and added it as an option in engine preferences. (veqryn & redrum)
* Updating Substance/Insubstantial look and feel UI to version 7.3\. (veqryn)
* Fixed bug with how AA casualties are taken for multiple-hitpoint airplanes. (veqryn)
* Fixed null pointer error in Classic (WW2v1) rockets. (veqryn)
* Speeding up battle calculator by reducing possibilities of thread contention over locks. (veqryn)
* Fixed bugs in Fuel cost for units, including around loading and unloading, and moving air with carriers. (veqryn)
* More stability improvements for server games. (veqryn)
* Fixed a thread deadlock that occurs when a game ends while the battle calc is still open, resulting in triplea not returning to the host screen. (veqryn)
* Prevented battle calc's calculate button from being enabled until data has finished being copied. Also added a tool tip on the button to let the user know how much memory they have left. (veqryn)
* Fixed display issue with repairs not being recorded properly in history panel. (veqryn)
* Fixed memory leak in battle calc and game data, causing an exponential number of units to be added to saves. (veqryn)
* Fixed bug in bid placement where you could not play British units in UK Pacific territories in Global 1940/1942\. (veqryn)
* Changing default host waiting time to 900 seconds (15 minutes) so that large games do not time out on people who don't know how to change the setting. (veqryn)
* Massive improvements to the new Hard AI. (redrum)
* Fixed lag and synchronization issues in the multi-threaded battle calc. Also added methods to time how long it takes to copy the game data, and use fewer threads if this takes more than 5 seconds. (veqryn)
* Fixed possible deserialization error in resource collections. (veqryn)
* Fixed bug in movement performer, which under certain rare circumstances would take all movement away from air units going from sea to land. (veqryn)
* Further work on ProAI (called Hard AI in game menu), including new methods to determine retreats in battles. (redrum)
* Fixed bug in username muting, which caused it to not work at all. (veqryn)
* Fixed issue with the game waiting on a player to click all 'OK' messages before a battle would continue. (veqryn)
* Fixed MapCreator so that it will properly send the map folder to the utility programs. (veqryn)
* Adding options to engine preferences to change how long your game host waits for clients on game startup and for observers joining. (veqryn)
* Allowing host to wait up to 100 seconds when starting a game for all clients to report in as good, and wait up to 30 seconds for observers joining after game has started. (veqryn)
* Fixing two memory leaks that allowed AI's and GameData to stay in memory after exiting back to main screen. (veqryn)
* Creating a threaded version of the BattleCalculator, to speed up results. (redrum & veqryn)
* Creating a logging window for ProAI so that players can watch the log. (redrum)

## Changes for 1.8.0.3

* Created new step property option, "repairPlayers", which will allow a player to repair the units owned by a different player. (veqryn)
* Fixed issue where your move phase was skipped if the only unit you owned was a land unit in a transport. (veqryn)
* Allowing land units to receive repairing and bonus movement from neighboring sea zone sea units. (veqryn)
* Units on transports no longer are able to repair other units, allow scrambling, or give movement to other units. (veqryn)
* Fixed issue where a unit that dies from rockets, still participates in subsequent strategic bombing battle. (veqryn)
* Fixed issue with allied land units in friendly transports and allied air on friendly carriers losing their movement when their transport/carrier moved. (veqryn)
* Fixing issue with allied land units starting game loaded on friendly transports, could not offload until at least one non-combat phase had passed. (veqryn)
* Deleted global game option property, "Allied Air Dependents", and replaced with its inverse, "Allied Air Independent". (veqryn)
* Added menu option under 'Export" menu, called "Export Unit Charts", which will create an html document showing all units in the game and their properties and cost. (veqryn)
* Created an new menu option under the 'Help' menu called "Unit Help", which will display a table of all units, by player, including all unit properties. (veqryn)
* Fixed bug in relationship attachment property change by trigger. (veqryn)
* Deleting phase step property option, "resetUnitState", and replacing with "resetUnitStateAtEnd" and "resetUnitStateAtStart". (frogg)
* Making createsUnitsList ability choose a random territory when producing to a neighboring territory. (veqryn)
* Fixing bugs in AI's where factories were on water zones that had no territory attachment. (veqryn)
* Fixed bug where a stalemate battle with carriers that can be damaged and when damaged don't let planes land, were not letting defending planes move to land. (veqryn)
* Deleting game option property "Unescorted Transport Dies", as it no longer does anything. (veqryn)
* Cleanup of HeadlessGameServer classes. (veqryn)
* Fixed bugs in Placement, which were allowing infinite placement of sea units which were constructions. (veqryn)
* Some updates for 'Great War' world war 1 map, and Pact of Steel 2\. (veqryn)
* Possible fix for "Could not stop delegate execution" bug. (veqryn)
* Fixed possible bug where a corrupted game save had the initialization delegate get called more than once. (veqryn)
* Adding a new AI called "Hard AI". Also renamed AI's: EZ Fodder -\> Easy AI, Moore N Able -\> Medium AI, Dynamix -\> Land Only AI. (redrum)
* Fix for infinite crash-reload loop on loading a corrupt autosave on a host bot. (veqryn)
* Fixed issue with Victory trigger not being able to use html properly. (veqryn)
* Fixed illegal state exception error in landing paratroopers during a battle. (veqryn)
* Possibly final fix for a game hang / frozen bot on game launch. (veqryn)

## Changes for 1.8.0.1

* Adding new sci-fi sound for "future" era. (pulicat, cernel, veqryn)
* Allowing "NONE" as a valid option value in sounds.properties file. (veqryn)
* Fixed null pointer exception in Moore AI for water based factories. (veqryn)
* Fixed bid delegate so that it will still run even if the player has no resources other than the bid amount. (veqryn)
* Fixed possible null pointer exception in Triggered Victory which is triggered from outside of the end round delegate. (veqryn)
* Making TransportTracker a static implementation to clean up the engine a little bit. (veqryn)
* Fixing various bugs in Global 1940, ww2v3, v4, v5, and v6\. (veqryn)
* Created new Player Rule Attachment, "immuneToBlockade", which will prevent blockade production loss for that player. (veqryn)
* Allowed 1940's paratroopers tech (ariborne combat) to move to / attack territories that have been blitz or already conquered this turn. (veqryn)
* Allowed 1940's paratroopers tech (airborne combat) to move from allied bases, and to allow travel over water. (veqryn)
* Created new step properties for special move delegates, "airborneMove", which controls if it is an Airborne Combat move phase. (veqyrn)
* Adding some more pre-industrial sounds. (pulicat)
* Allowed muting of custom aa gun sounds and custom notification, victory, and defeat sounds. (veqryn)
* Created resource image factory for making images and icons of resources. (veqryn)
* Fixed user interface to allow purchasing resources. (veqryn)
* Fixing engine to allow purchase rules for purchasing resources. (veqryn)
* Fixed memory leak in repair rules for repairing factories. (veqryn)
* Creating a menu option in the "File" menu called "Post PBEM/PBF Gamesave...", which will for pbem games post/email the savegame to the forum, without having to wait for the end turn phase. (veqryn)
* Changing trigger "notification" to use "players". (veqryn)
* Changing unit attachment property, "repairsUnits", to allow multiple and to have repair values associated with each unit, thereby allowing units to be repaired by X amount each turn. (veqryn)
* Created new unitPlacement attribute, "unitDamage", which will let a unit start with bombing factory damage. (veqryn)
* Created new unitPlacement attribute, "hitsTaken", which will let a unit start damaged. (veqryn)
* Deleting game option property, "SBR Affects Unit Production", and simplifying the engine to only use direct unit damage. (veqryn)
* Getting units with different bombing unit damage to not stack. (veqryn)
* Allowing selection of casualties for multiple hit units to allow damage points past one. (veqryn)
* Getting "hitPoints" to work in the graphical user interface. (veqryn)
* Getting "hitPoints" to work on the back end inside the engine. (veqryn)
* Created new unit attachment property, "hitPoints", which sets the number of hitpoints a unit has, and also deleted property "isTwoHit". (veqryn)
* Allowing sounds to be played by trigger, by putting "_sounds" after a duplicate of the Notification message key, with the value equal to "notification_" or "victory_" or "defeat_" + the sound key found in the sounds.properties file. (veqryn)
* Added logfile "dump" command for host bots, that will from the command line print out all status, connection, memory, and thread information to the log. (veqryn)
* Created ability for lobby admins to mute and/or boot players in a host bot, remotely. (veqryn)
* Created ability for lobby admins to see the player connections in any host game. (veqryn)
* Created ability for lobby admins to see chatlog of a host bot remotely. (veqryn)
* Adding a new autosave, 'autosave2', which will take turns being saved to with 'autosave'. (veqyrn)
* Changing movement validation to disallow moving from a contested battle territory into an enemy territory. (veqryn)
* Fixed bug with a territory owned by one player but having enemy units in it, if the owned reconquers the territory it is no longer marked as newly-conquered. (veqryn)
* Fixed bug preventing sounds inside a zipped map from playing if the zipped map file path had any spaces or special characters in it. (veqryn)
* Fixed bug preventing phase sounds from playing more than once in a non-pbem game. (veqryn)
* Creating an option to select local players and AI's for PBEM games. AI's will not post/email the turn summary and savegame at the ends of their turns however. (veqryn)
* Fixing bug with host bots where disabling players, quitting, then reloading and disabling even more players, resulted in game crash. (veqryn)
* Disallowing previously disabled players from being re-enabled after a game has started. (veqryn)
* Fixed bug with moderator lobby unbanning utility. (veqryn)
* Created ability for lobby admins to ban players inside a host bot, remotely. (veqryn)
* Created ability for lobby admins to stop game on a host bot remotely. (veqryn)
* Created ability for lobby admins to shut down a host bot remotely. (veqryn)
* Created new option for host bots, "triplea.lobby.game.supportPassword", which when set will allow remote actions on the host bot from the lobby admins. (veqryn)
* Created new option for host bots, "triplea.lobby.game.reconnection", which will set the time between lobby reconnection refreshes, with the minimum and default being 6 hours. (veqryn)
* Created new game option property, "Disabled Players Assets Deleted", which will delete all units and resources from a disabled unused player during game startup. (veqryn)
* Allowing clients to disable and enable players for host bots, but not normal hosts. (veqryn)
* Forcing random start to not allow disabled players to select territories, and also letting savegames keep disabled state, and disabled players switched to an AI. (veqryn)
* Creating new playerlist option for players, "canBeDisabled", which if set to true will force the game to delete all delegates for that player, thereby allowing more customized multiplayer games. (veqryn)
* Forcing hosts and hosting bots to always use Secure Random source when playing online, even when the host is not playing. (veqryn)
* Updating TripleA to require at least Java 6 or greater. (veqryn)
* Updating included jar libraries to latest versions. (veqryn)
* Updating embedded JRE to Java 7 update 51 for x86\. (veqryn)
* Updated Substance UI to version 7.2.1, and included approximately 14 new Look and Feel skins. (veqryn)
* Created a menu option called "User Notifications..." which lets you turn off notifications you would receive from End Turn Reports, Triggered Notifications, Chance rolls that are successful or failed. (veqryn)
* Fixing Comment Log so that it updates in real time. (veqryn)
* Changed automated hosting bots so that they show up as having 1 less player (ie: the bot itself doesn't count), which means zero players if noone else has joined. (veqryn)
* Changed unit resource creation so that positive resources will be created before negative resources. (veqryn)
* Fixing bug in destroyedTUV condition for allRounds that prevented it from working at all. (veqryn)
* Added an updated engine jar for 1.7.0.5 so that the new engine can play old 1.7.0.x savegames. (veqryn)
* Changed game setup screen so that the buttons for "Choose Game", "Load Saved Game", and "Game Options", will no longer be greyed out for Clients who have connected to an automated hosting bot. Those buttons will perform the same as if the client used the "Network" menu instead. (veqryn)
* Adding a menu option to change an automated hosting bot's game options, and creating backend to process this request. (veqryn)
* Forcing automated hosting bots have have a "support email address", so that when a bot has hung or stopped responding, a moderator in the lobby can email the bot's owner to notify them of the situation. (veqryn)
* Forcing automated hosting bots to have no password, to start with the string "Bot", and have "automated_host" somewhere in comments. (veqryn)
* Adding a column to the lobby called "B" for "Bots", which will show which hosts are automated hosting bots. They will also show up as italics. (veqryn)
* Fixed order of firing in ww2v3 and Global 1940, so that defending subs that are not sneak attacking will fire after all attackers have fired. (veqryn)
* Fixing a bug where attacking with a carrier loaded with allied fighters, then retreating, would prevent those fighters from being able to participate in battles for the rest of the game. (veqryn)
* Allowed TripleA clip player to access sound files within a zipped map. (veqryn)
* Fixed bug that allowed fighters to be moved greater than their allowed movement if paired with a carrier. (veqryn)
* Adding scroll bars to placement window. (veqryn)
* Fixed another bug in getMaxUnitsToBePlaced, it will no longer stop the game if it frees up enough capacity to place but not equal to theoretical maximum. (veqryn)
* Fixed bug where a strategic bombing unit receiving negative support and/or negative terrain modifier would be unable to bomb is its attack power decreased to zero. (veqryn)
* Created new step properties for move delegates, "combinedTurns", which changes some validation for intermeshed player phases, such as allowing air to live if the ally could place a carrier under them. (veqyrn)
* Created new step properties for purchase and place delegates, "bid", which controls if it is a bid phase. (veqyrn)
* Created new step properties for move and end turn delegates, "repairUnits", which controls when units get repaired. (veqyrn)
* Created new step properties for move and place delegates, "removeAirThatCanNotLand", which controls when air that can not land gets killed. (veqryn)
* Created new step properties for move delegates, "resetUnitState", which controls when units get their movement and other stats reset. (veqryn)
* Created new step properties for move delegates, "giveBonusMovement", which controls when bonus movement is given. (veqryn)
* Created new step properties for move delegates, "fireRockets", which controls when rockets fire. (veqryn)
* Created new step properties for move delegates, "combatMove" and "nonCombatMove", which control movement validation. (veqryn)
* Prevented AA type units from firing on both start and end of movement, when option "Force AA Attacks For Last Step Of Fly Over" is turned on. (frogg)
* Created new game property option "Abandoned Territories May Be Taken Over Immediately", which allows an abandoned territory to be taken over on the turn it was abandoned, rather than waiting for it to be attacked. (veqryn)
* Created new game property option "Sea Battles May Be Ignored", which allows attackers to not create a battle in a contested sea zone. (frogg)
* Created new game property option "Contested Territories Produce No Income", which will stop all production in territories that contain enemy units. (frogg)
* Created new game property option "Retreating Units Remain In Place", which will allow retreats to only the same territory as the battle. (frogg & veqryn)
* Allowed AxisAndAllies.org forum poster to maintain "notify me" settings. (Bruce Nielsen)
* Changed trigger property "when" so that it can be set multiple times, allowing a trigger to fire multiple times per round. (frogg)
* Changed game property option "Battle Rounds" to "Land Battle Rounds". (veqryn)
* Added game property option "Sea Battle Rounds". (frogg)
* Possible fix for host game hang, when host is launching and another player leaves or joins at start of launch. (veqryn)
* Possible fix for game hang / game freeze during hosting, client start step should now wait for delegate bridge to finish updating. (veqryn)
* Possible workaround for game hang / game freeze during hosting, if error occurs game should now drop back to waiting screen instead of just hanging or ghosting. (veqryn)
* Adding much more logging to HeadlessServerGame in order to try to find cause of the CastClassExceptions in TripleAPlayer.start() and NullPointer/IllegalArgumentExceptions in RemoteName. (veqryn)
* Fixed null pointer error in battle calculator when spamming the cancel button. (veqryn)
* Rebalancing Great War world war 1 game. (veqryn)
* Fixed bug where chanceIncrementOnFailure and chanceDecrementOnSuccess were not allowing any number of zero or less for chance. (veqryn)
* Fixed error where games with a round offset where doubling what round the game started on each time it was saved via the history panel. (veqryn)
* Creating a headless chat service, so that server can be created in a headless environment and still chat. (veqryn)
* Fixed bug causing fatal errors in client-server games when client owned very last step/delegate of game (only applied to some grid based games). (veqryn)
* Adding a log file for the headless server located at /log/headless-game-server-\<servername\>-log\<#\>.txt, to keep track of events. (veqryn)\</servername\>
* Adding many more additional commands to headless game server console, including show connections, ban player, save game, and stop game. (veqryn)
* Stopped headless game server from being able to load any savegame for a map to which it does not have the required map files for. (veqryn)
* Possible fix another possible hang/freeze point causing a Could Not Block Delegate Execution error. (veqryn)
* Fixed headless game server's connect to lobby so that resetting the connection does not erase info about the game. (veqryn)
* Possible fixes two possible hang/freeze points in Server Game, one caused by a bogus ClassCastException in ClientGame, the other by a bogus NullPointerError/IllegalArgumentError in RemoteName from PlayerDelegateBridge. (veqryn)
* Making sure sound system never loads sound clips for headless game server. (veqryn)
* Added a console to automated headless game server host, which allows commands such as 'help', 'status', 'memory', 'threads', and 'quit'. (veqryn)
* Created a headless UIContext for use with headless game server, so that it may run on a linux platform that has no configured graphics environment. (veqryn)

## Changes for 1.7.0.3

* Got headless game to show options to client's, for changing the game, changing to an autosave, sending a save to the server, and getting the savegame from the host. (veqryn)
* Got headless game to restart its lobby connection once per 8 hours. (veqryn)
* Got headless game server to be able to connect to lobby, and host games repeatedly without requiring any UI or swing event thread. Also got to immediately reload autosave when a player quits. (veqryn)
* Got headless game server to be able to pick games, and have a mini-ui for hosting and for during the game. (veqryn)
* Got headless game server to be able to host minimap, with the game screen headless. (veqryn)
* First pass at setting up framework for a headless game server. (veqryn)
* Preventing AA units with maxRoundsAA from getting removed early from battle. (veqryn)
* Fixed bug causing Random Territory Start delegate to fail in online games due to requesting dice too quickly. (veqryn)
* Updating Great War ww1 map and xml, to improve options and balance. (veqryn)
* Updating packaged JRE to Java 7 update 21 for x86\. (veqryn)
* Made fuelCost no longer charge for allied air dependants, paratroopers, and owned air on owned fighters not making an attack. (veqryn)
* Created new game option property, "Use Fuel Cost", which will control if we charge for fuel in our movement. (veqryn)
* Added an option to turn off the end of turn report, into the game menu bar. (veqryn)
* Changed engine preference for max memory into a "system.ini" file, that way a user can delete or reinstall TripleA if they screw up. (veqryn)
* Created new engine preference option to set the maximum memory used for triplea, for joining, hosting, and also an option to have triplea always restart with higher memory maximum. (veqryn)
* Created new option in engine preferences to show engine log console, and also had the console show current memory usage. (veqryn)
* Reducing maximum memory to 896mb, down from 1024mb, in order to stop these errors from happening, and not allowing engine to add 20% to this when joining online games or hosting. (veqryn)
* Figuring out some user's Java jvm's and/or the JRE included with triplea, only allow up to xmx 1024mb of memory maximum, and that the program completely fails when going over this limit, often causing the user to be unable to join or host games online. (veqryn & diaz)
* Fixing some lock not held errors. (veqryn)
* Fixed bug causing triggered notifications to not use local images when shown on a client computer. (veqryn)
* Not allowing scrambling question when only and SBR raid is in a territory and scramble to SBR is turned off. (veqryn)
* Fixed bug causing Territory Effects to not be applied at all, ever. Also fixed possible issue with 'choose best roll' in low luck. (veqryn)
* Fixed bug causing national objectives which rewarded players on a per-territory basis using the "each" modifier to not work. (veqryn)
* Fixed bug causing paratrooping land units who's air transports were hit by AA fire to not be removed from the battle. (veqryn)
* Fixed possible null pointer in color chooser for color property, which occurred when chosing the color for map text. (veqryn)

## Changes for 1.7.0.1

* New attachment properties for Triggers, Politics, and User Actions: "chanceIncrementOnFailure" and "chanceDecrementOnSuccess" which will modify the "chance" value. (veqryn)
* Fixing fuelCost to not be charged for units in transports. (veqryn)
* Major changes to both the map and the placements and the rules for "Great War" world war one game. (veqryn)
* Implemented all sounds through IDelegateBridge.getSoundChannelBroadcaster().playSoundForAll() or through DefaultSoundChannel.playSoundOnLocalMachine() for a few local sounds like slapping in chat. (veqryn)
* Created new channel broadcaster for use with playing sounds on both server machine and client machines. (veqryn)
* Created user interface element for RandomStartDelegate, so that players can pick which territory they want and what units they want in it. (veqryn)
* Gave all AIs methods to pick territories, and they will attempt to focus on a single area of the board. (veqryn)
* Created new game option property, "Territories Are Assigned Randomly", which determines if territories are randomly assigned or picked by players during RandomStartDelegate. (veqryn)
* Created new delegate, "RandomStartDelegate", which will allow for randomly assigned territories or territories chosen in turn order. (veqryn)
* Fixed problem where territory names that were parseable integers could not allow any territory based conditions. I still recommend territories have a non integer character in them though. (veqryn)
* Fixed null pointer error in signalGameOver when called by a trigger for a game that has never reached the end round step. (veqryn)
* Minor adjustment to retain capital produce number methods to allow a value of zero. (flaaargle)
* Created user interface element for the User Action Delegate, based on the existing politics interface. (veqryn)
* Created new delegate, "UserActionDelegate", which will allow nations to take any kind of condition/trigger based action. (veqryn)
* Created new text file, "actionstext.properties", which contains action text for the user interface for taking user actions, similar to politicstext.properties. (veqryn)
* Added new property, "activateTrigger", to UserActionAttachment, which will fire a trigger when the nation takes this action. (veqryn)
* Added properties for conditions, conditionType, invert, chance, costPU, text, actionAccept, and attemptsPerTurn to the User Action Attachment. (veqryn)
* Created new attachment, "UserActionAttachment", which holds actions that can be taken by a player, based on an abstraction of the political action attachment. (veqryn)
* New Condition Attachment property option, "gameProperty", which can be set equal to the exact string of any boolean game property option, including custom made up ones. (veqryn)
* Created new AI specially for multiplayer free-for-all games, "Does Nothing AI", which will buy units the first round then destroy all money all subsequent rounds, along with doing nothing else. (veqryn)
* Abstracted methods to find the power and rolls of units into a single method. (veqryn)
* Fixed issue with Marine amphibious attackers showing a bonus on the battle screen even when attacking via land. (veqryn)
* Fixed null pointer error in Strong AI (Moore AI). (veqryn)
* Getting the UnitSupportAttachment faction option to handle both allied and enemy, thereby allowing giving positive or negative support to enemy units. (veqryn)
* Getting the UnitSupportAttachment dice option to handle both strength and roll, thereby allowing giving extra rolls to units. (veqryn)
* Changing defending submarines to fire after all attacking units under classic rules, where property Defending Subs Sneak Attack is false. (veqryn)
* Created new button, "Order of Losses", in the battle calculator, which will all you to put in a text script of which casualties to select in what order. (veqryn)
* Added option to retreat in battle calculator when we are losing, which is approximated by seeing if our 'meta-power' is lower than the opponent's. (veqryn)
* Created new image utility, TileImageReconstructor, which will recreate an image based on base tiles or relief tiles and/or draw a polygons file onto an image. (veqryn)
* Adding a visual log to AutoPlacementFinder and TileImageBreaker, and getting the AutoPlacementFinder to cut out at a max of about 50 placements per territory. (veqryn)
* Changed unit attachment "isMarine" to allow for integers instead of boolean. (veqryn)
* Updated default casualty selection to take territory effects into consideration. (veqryn)
* Updating web poster to keep track of many entered websites, and save them all to the local cache but not to the savegame. (veqryn)
* Created new unit attachment property, "canAirBattle", which determines if a unit participates in a normal battle's air battle. (veqryn)
* Allowing defense to ground their planes before an air battle (preceding a normal battle) if withdrawing is turned on, however if the territory is lost they die. (veqryn)
* Fixed battle screen null pointer errors caused by maps with artillery units but no supportable units. Also fixed bug where maps without notes could not be closed. (veqryn)
* Allowed AA Gun type units to fire back in same round if killed by other AA Gun type units. (veqryn)
* Added new steps to must fight battle so that offensive aa guns will work correctly. (veqryn)
* Created new unit attachment properties, "offensiveAttackAA" and "offensiveAttackAAmaxDieSides", which will be used by offensive aa guns. (veqryn)
* Created new unit attachment property, "maxRoundsAA", which sets the number of rounds an AA gun may fire in, with 1 being default. Only normal battles are affected, while flyover and strategic bombing are not affected. (veqryn)
* Created new game option property, "Battle Rounds", which sets the maximum number of rounds of combat for normal battles, with -1 being infinite which is default. (veqryn)
* Created new game option property, "Can Scramble Into Air Battles", which will allow a player to scramble air to neighboring territories in order to defend against air raids and air battles. (veqryn)
* Set up battle delegate and tracker to allow air battles to be created for normal battles. (veqryn)
* Created new game option property, "Battles May Be Preceeded By Air Battles", which will allow normal battles to have air battles first. (veqryn)
* Created new game option properties, "Air Battle Attackers Can Retreat" and "Air Battle Defenders Can Retreat", which allow retreating from air battles. (veqryn)
* Created new game option property, "Air Battle Rounds", which will allow setting the number of rounds of combat for air battles. (veqryn)
* Abstracted StrategicBombingRaidPreBattle to become AirBattle, no longer extending StrategicBombingRaid. (veqryn)
* Fixed bug that caused a rare skipping of a battle involving transports and air vs undefended transports. (veqryn)
* Adding new PBEM feature, the ability to post to a custom triplea website. (weigo)
* Adding scroll bar to chat panel for online game waiting host room before game launched. (veqryn)
* Expanded Unit tool tips to include unit support attachments, and also to detail more info for other abilities. (veqryn)
* Increasing maximum memory to 1gb (1024mb), up from 768mb. (veqryn)
* Creating a new monthly check to see if all maps are up to date, and if not then asking the user to update their maps. (veqryn)
* Allowed "men" in International Draughts to capture backwards, which appears as a game option in Checkers. (veqryn)
* Created caching mechanism for the game notes, so that it is only in memory when the notes tab is open and otherwise can be cleared from memory if needed. (veqryn)
* Created a new Unit Attachment option, "damageableAA", which allows this AA gun type unit to cause damage to a two hitpoint unit instead of outright killing it. (veqryn)
* Fixed bug where AA shots on 2 hitpoint units with Choose AA Casualties on was resulting in no damage or killed unit. Also changed battle display to show "typeAA" for each AA Fire phase, instead of a generic identifier. (veqryn)
* Allowing custom AA hit and miss sounds for irregular AA types, with the folder being located at "battle_\<typeaa\>\_hit" and "battle_\<typeaa\>\_miss" (folder must be lowercase though), where \<typeaa\>is the unit attachment "typeAA" of that unit. (veqryn)\</typeaa\>\</typeaa\>\</typeaa\>
* Adding text labels to the Battle Calculator for the number of hitpoints and the total attack or defense power of each side. (veqryn)
* Adding a new Hot Key "F" for 'Find Units', which will highlight all units you own that have movement left, but only during a movement phase. (frigoref)
* Allowed Edit Mode to add land units to a sea zone if there are either transports already there or transports also being added at the same time. (veqryn)
* Allowed Edit Mode to remove units owned by different players. (veqryn)
* Changed territory attachment "victoryCity" to allow integers instead of boolean, thereby allowing victory cities with greater value, and also added a tooltip to tech purchase phase to show what techs are in each category. (eurofabio)
* Allowed Edit Add Units to check if artwork exists for units not in a production frontier, and if so allow them to be created. (veqryn)
* Added more info to Battle Calc including total TUV swing, and allowing retreat after losing all air units or having only x units left. (veqryn)
* Fixed bug where having sea units begin the turn on top of an enemy sub, and then not moving them but also not attacking, caused them to lose their movement anyway. (veqryn)
* Fixed bug where you could move a destroyer after it had killed a sub, during noncombat move. (veqryn)
* Updating text xml's and adding TWW xml for new tests. (veqryn)
* Fixing bug in air movement validation for complex movement cases. (veqryn)
* Fixing several memory leaks related to game notes staying in memory multiple times. (veqryn)
* Creating Edit Mode for Grid Based games like chess, checkers, and go. (veqryn)
* Added feature to automatically parse HTML text in game notes and in notifications, and replace all image links with links to the map folder's "doc/images/" directory, thereby allowing local image files to be used. (veqryn)
* Adding ability to specify when the attacker should retreat after how many rounds, to the battle calculator. (veqryn)
* Added fields for average number of rounds, average attacking units left when attacker won, and average defending units left when defender won, to the battle calculator. (veqryn)
* Added new Edit option to change political relationships between players. (veqryn)
* Created option in game 'View' menu to change the font size and font colors of things like territory names, pu's, unit count, and factory damage count. (veqryn)
* Fixed serious bug with process runner util that prevented a new classpath from being used, most notably preventing the 'old jars' from getting run. (veqryn)
* Creating a method in IDisplay to send messages to all player's computers, but only once per computer. Also includes ability to send to certain players only. (veqryn)
* Forced all non-returning void dialogs to run in a separate process as to not block the game from moving forward.
* Forced all UI interactions to either go through a single thread, or wait for thread to finish, so as not to have multiple popups at same time. (veqryn)
* Creating simple message dialog report for end of turn collection of PUs and national objectives and any blockade action. (veqryn)
* Creating a mouse shadow image to go with the route image, showing how much movement you have left for any selected units, in blue font. (veqryn)
* Possibly fixing bug where the game host process does not end, even though all windows close. (veqryn)
* Allowing all Grid Games to use the play by email and forum posters. (veqryn)
* Abstracted the Forum Poster to its own component and static methods. Added new checkboxes for including savegame and for reposting the turn if it failed the first time. (veqryn)
* Creating victory conditions for Go, and creating a UI for players to negotiate which groups of stones are alive or dead. (veqryn)
* Creating all game logic for Go. (veqryn)
* Creating UI for Go. (veqryn)
* Allowing Grid Games to change their width and height mid-game, like through game options. (veqryn)
* Creating initial framework and loader for Go. (veqryn)
* Creating simple AI for Checkers, and adding rules to enforce the forcing of jump capture moves when available. (veqryn)
* Creating UI for Checkers. (veqryn)
* Adding all game logic for Checkers. (veqryn)
* Adding sound for joining a game chat room. (cpp-ose & jeparedes)
* Creating framework and loader for Checkers. (veqryn)
* Adding Chess to available games that come with TripleA, and cleaning up source and UI, and fixing various bugs in the grid games framework. (veqryn)
* Getting Grid Games to use the History Panel, and adding the history panel and other options to their menu bar. (veqryn)
* Getting GridMapPanel to scroll by having it extend ImageScrollerLargeView, and fixing up all grid based games to use this. (veqryn)
* Getting Grid Games to allow having a chat panel in multiplayer and networked games. (veqryn)
* Abstracting both Sliding Tiles (N-Puzzle) game and Tic Tac Toe game into Grid Game. (veqryn)
* Created a min-max/alpha-beta type of AI, which takes a long time to think but actually makes OK moves. (veqryn)
* Created a very very simple AI for Chess, based on random moves plus capturing pieces when available. (veqryn)
* Finished checking for Check and Check Mate in Chess. (veqryn)
* Finishing movement validation for Chess. (veqryn)
* Adding a visual cue for which moves are legal for Chess and other Grid games. (veqryn)
* Added movement validation logic for Chess. (veqryn)
* Upgrading the graphics for Grid Games, and including a mouse shadow of selected units, and a highlight of which units on map are currently selected. (veqryn)
* Major abstraction of both King's Table and Chess into a single framework for Grid based games. (veqryn)
* Completing most of UI aspect of Chess game. (veqryn)
* Creating framework for a Chess game. (veqryn)
* Created a notification to the user when they start a version of TripleA for the first time, showing the new features of this version. (veqryn)
* Created a notification to the user when they start TripleA that checks if their TripleA is the latest version, and if not asks them to update it. (veqryn)
* Created a notification to the user when they click "list games" that will alert them to which maps they already have which may be out of date and need updating. (veqryn)
* Added the default map downloader xml web link to the download maps feature, if the user does not already have any. (veqryn)
* Fixed movement validation bug that prevent loading of land units onto a transport during noncombat if the transport was in an enemy 'owned' sea zone. (veqryn)
* Fixed bug where units being transported or otherwise dependent were being counted towards unit presence and unit exclusion objectives. (veqryn)
* Changing territory attachment "occupiedTerrOf" into "originalOwner". (veqryn)
* Deleting game option property "Occupied Territories" since it does not do anything anymore. (veqryn)
* Created new territory effect attachment option, "unitsNotAllowed", which is a list of units that will be prevented from moving into any territories with this effect. (crystalct)
* Adding ability to specify which round the game starts on, through a round offset in gameplay section of xml. (veqryn)
* Added ability to Right Click on any node in the History panel, and save a game at that point in history [could still be buggy, do not use for tournament games]. (veqryn)
* Abstracted delegates so that the server can now determine if it needs to wait on the user for input for a delegate or not. (veqryn)
* Fixed bug where having a tech token but not having enough money to buy a new one, would cause you to skip rolling for the existing token. (veqryn)

## Changes for 1.6.1.4

* Adding dotted lines to the LOTR Middle Earth map, to show connections over rivers. (veqryn)
* Not showing tech in stats panel if game xml does not have any technologies. (veqryn)
* Created new stepProperty, "turnSummaryPlayers", which holds a list of players for whom we will include their turn summary information in the forum/email post. (veqryn)
* Created new stepProperty, "skipPosting", which when true will skip the forum posting for that EndTurn type step. (veqryn)
* Created new xml option type "stepProperty" for a step (gamePlay - sequence), which can hold small options for modifying a delegate step. (veqryn)
* Adding some more sounds for ancient/classical era. (veqryn)
* Adding some more ww2 sounds and national anthems for main players. (hepster)
* Allowing air movement over neutrals and enemy territories so long as movement over neutrals is allowed, and no nonparatrooping units are present. (veqryn)
* Creating caching mechanism for sound clips, so that there are never more than 24 sound clips being held in memory. This should prevent errors in MacOS and Linux, which can not handle having large number of sound clips open at same time. This may however result in a delay before hearing clips, and still could result in errors if clips are really long. (veqryn)
* Fixed null pointer error for a trigger based game property change of a field that starts out as null. (veqryn)
* Fixed bug in strategic bombing that allowed strategic bombing of units that can be damaged, which were also being transported. (veqryn)
* Adding scroll bars to notification messages window. (veqryn)
* Increasing max memory from 640mb to 768mb, and up to 896mb for online games. (veqryn)
* Moved all sounds to a specific "era" folder (ww2, preindustrial, classical, future) and changing how sounds are found again, so that there should no longer be any need for duplicate sound files. Now all sounds should come with TripleA, and you can use the "sounds.properties" file to cherry pick which sounds you want. (veqryn)
* Created a "sounds.properties" file which allows you to specify which era of sounds (ww2, preindustrial, classical, future) you are using, and also set up custom sound choices for each sound location path. (veqryn)
* Getting TripleA Map Panel to center on the capital of a player, whenever we switch to a new player's phase. (veqryn)
* Changing getBoundingRect and createTerritoryImage and getTiles so that any polygons on the right or bottom will be translated to be on the negative left or top, hopefully solving issue where the mini territory image was not being displayed properly for territories on both sides of a map divide. (frigoref)
* Abstracting the Stats panels into AbstractStatPanel so that extending Stats panel (and all of its overhead) is no longer necessary for the EconomyPanel, ObjectivePanel, TerritoryDetailPanel, and other panels. (veqryn)
* Changing Tech Stats Panel to use small flag images for column headers instead of the first letter of nation names. (veqryn)
* Fixing bugs with placing constructions in sea zones. Now constructions can only be "produced" by the territory they are going into. (veqryn)
* Adding a lot more sounds to the engine (zim xero) and some sounds specific to napoleonic empires. (hepster & veqryn)
* Added tutorial on how to make a map and/or map skin. (veqryn)
* Allowing for Sea Factories, and Air Factories, to produce from owned sea zones. (veqryn)
* Added UPnP support to TripleA, so that TripleA will now attempt to Forward Ports for the user. This means users should no longer have to do port forwarding themselves to be able to host a game online. (veqryn)
* Created framework for using UPnP library, and UI component for user. (veqryn)
* Added java library for Universal Plug and Play (UPnP) to TripleA. (veqryn)
* Created new HotKey, "N", which when pressed during a movement phase, will cycle through all units with available movement left, focusing the map on the unit. (veqryn)
* Created new HotKey, "I", which when pressed will create a popup for 5 seconds showing all the info about the unit and/or territory your mouse is currently over. (veqryn)
* Allowing the map to be scrolled by using the arrow keys and/or WASD. (veqryn)
* Added original owner, whenCapturedByGoesTo, captureUnitOnEnteringBy, and changeUnitOwners to the Territory tooltip and territory tab info. (veqryn)
* Fixing Move Panel and Place Panel so that Undoing a move or place will not result in scrolling back to the top, and will instead scroll to make sure that the move under the undoed move is still visible. (veqryn)
* Allowing all sounds to have a player associated with them. Just name the sound "\<soundname\>\_\<playername\>". If the player sound does not exist, it will use the default non-player sound. (veqryn)\</playername\>\</soundname\>

* Added a ton more new sounds to the engine. (veqryn)
* Changed Sounds so that instead of specific sound files, the engine will search for specific sound folder. The engine will then randomly select a sound in that folder and play it. This allows for randomized sounds. (veqryn)
* Made sure any clicking or dragging gives focus to the main map panel area. Also ensuring that if focus goes to the tabs panel tabs, that the focus goes back to the map. (veqryn)
* Created new game option property, "Submarines Defending May Submerge Or Retreat", which will allow defending submarines to submerge or retreat to a friendly neighboring sea zone. (veqryn)
* Deleting game option property, "Hari-Kari Units", since it doesn't do anything at this point. (veqryn)
* Deleting game option property, "Previous Units Fight", since it doesn't do anything at this point. (veqryn)
* Allowing sea units to retreat back if the retreating to territory contains only ignored enemy units. (veqryn)
* Disallowing rockets from firing over impassible territories by default. (veqryn)
* Added message on how long a ban lasts for, when a user tries to reconnect to the lobby. (veqryn)
* Created ui wrapper for properties, and allowed most to be editable. (veqryn)
* Created new map utility, "MapPropertiesMaker", which will make the "map.properties" file. (veqryn)
* Added an 'Is Amphibious' check box to the battle calculator, so that units like marines will correctly calculate for an amphibious battle. (veqryn)
* Getting Decoration Placer to auto place all images nicely on the map if they match the territory names or if they are not decorations. Also including detailed instructions. (veqryn)
* Got the Decoration Placer to work with placing PUs, decorations, name images, capitals, vc's, and all other image types and text files. (veqryn)
* Creating new map utility, "Decoration Placer", which allows a map maker to put decorations and other images on a map, recording their points in a text file. (veqryn)
* Fixed bug in Triggers that use "chance" and also have more than 1 action or event inside them, so that they will no longer test once for each action, and instead only one time total. (veqryn)
* Created new tab, "Notes", which will just show the game notes, on the right side of the screen. (veqryn)
* Getting the objective panel to not refresh more than every 10 seconds, and adding a "Refresh" button so that it can be manually refreshed. (veqryn)
* Getting the objectives on the objective tab to show up in colors (red = true, blue = used up), and show more information: \<#of uses left\>\<t=true f="false"\>\<#of objectives filled\>. (veqryn)\</t=true\>
* Including on Objective tab whether condition is currently true or not, and getting it to update with the game. (veqryn)
* Creating new text file, "objectives.properties", which will hold all the details about what objectives to show on the objective tab. (veqryn)
* Creating new stats panel, "Objective" Tab, which will contain a list of all national objectives and any other conditions the map maker wants. (veqryn)
* Created new "map.properties" variables: "map.cursor.hotspot.x", and "map.cursor.hotspot.y". (veqryn)
* Allowing TripleA to use custom cursors located at "misc/cursor.gif". (veqryn)
* Getting TripleA to use any sounds located in a folder named "sounds" in any map file, thereby allowing custom sounds for every map. (veqryn)
* Renaming the "images" folder into "assets", and then moving the "sounds" folder to be inside of the "assets" folder, inside the triplea program directory. (veqryn)
* Created new text file, "comments.txt", which will control where things like convoy route names and comments will go. (veqryn)
* Deleted "map.properties" variable "map.showConvoyNames" and replaced with "map.showComments". (veqryn)
* Created new folder, "territoryNames", which can be filled with .png images of each territory name. These will be displayed at the points in "name_place.txt". (veqryn)
* Created new "map.properties" variables: "units.stack.size", "map.showSeaZoneNames", and "map.drawNamesFromTopLeft". (veqryn)
* Deleting xml property, "Display Sea Names", and will replace it with a map.properties property "map.showSeaZoneNames", because display options should not be in the xml, only game logic should be. (veqryn)
* Deleting xml property, "Display Units as Counters", and will replace it with a map.properties property "units.stack.size", because display options should not be in the xml, only game logic should be. (veqryn)
* Created new "map.properties" variable "map.scrollWrapY", and got TripleA to successfully scroll in the Y direction, as well as both X and Y at the same time seamlessly. (veqryn & frigoref)
* Created new "map.properties" variables: "map.showResources", and "screenshot.title.enabled". (veqryn)
* Creating a ConnectionFinder for the 'map' part of the xml. (edwin van der wal)
* Adding Mnemonics to menu options in game. (frigoref)
* Improved performance of Polygon Grabber and added a auto-grab to it to will attempt to grab any polygon that does not contain other polygons, based on the centers file. (edwin & veqryn)
* Set up UI for map creator, fixed it up to be able to run all utility files, including sending arguments to them. (veqryn)
* Creating a new Map Creator / Map Maker that is accessible from the Engine Preferences section of TripleA. (veqryn)
* Updating TileImageBreaker and PlacementPicker to include more notes on how to use them, as well as fixing some bugs and allowing arguments and remembering selections. (veqryn)
* Updating CenterPicker and PolygonGrabber and AutoPlacementFinder to include more notes on how to use them, as well as allowing arguments and remembering selections. (veqryn)
* Fixing Global 1940 to match 2nd Edition version. (veqryn)
* Preventing fighters that used up all movement to get to a battle, from getting to retreat. (veqryn)
* Allowing PlacementPicker and AutoPlacementFinder to accept two arguments (when run by command line), the width and the height, of the placements. (veqryn)
* Fixed issues preventing the smallMap from being updated after switching map skins. Also polishing up support for map skins that are totally different than the original map. (veqryn)
* Creating new "map.properties" variables: "units.width", "units.height", "units.counter.offset.width" and "units.counter.offset.height", allowing maps to use non-standard sized unit images. (veqryn)
* Fixing a bug in center picker, and fixing a bug where selecting a map skin didn't verify the map before changing the user preferences. (veqryn)
* Fixed bug where rockets could attack a factory multiple times. (veqryn)
* Deleting the game option "Rocket Attack Per Factory Restricted", and replacing it with its inverse, "Rocket Attacks Per Factory Infinite". (veqryn)
* Fixed issue with not being Java 1.5 compatible. (veqryn)
* Fixed null pointer error in getSkins method when user has installed triplea to the user folder. (veqryn)
* Fixed issue with showing Turn Summary from right clicking on the player's node while in the History mode, which showed the current player's territory summary instead of the selected player. (veqryn)
* Fixing movement validation bug that disallowed movement into a sea zone controlled by the enemy with subs, if the sea zone also had an owner, even if subs are being ignored. (veqryn)
* Adding new AI, "Moore N Able (2)", with ability to read a script file from map folder. (kmoore)
* Fixing Concurrent Modification error with getIsAmphibiousMarine method in battle display. (veqryn)
* Fixing comparison method in Easy AI (weak ai) so that adheres to the comparison contract. Also cleaned up a lot of code, fixed a lot of warnings. (veqryn)
* Fixing bug history panel bug caused by loading a savegame at the end of the last player's turn, causing a "Can not add event, not in step" error to be thrown. (veqryn)
* Adding new menu option "Focus On Own Casualties", which when selected will cause the default casualty selection to focused, allowing the user to hit spacebar to accept it. (hakon)
* Changed order of steps so that in games where Submarines may submerge before battle, the attacker is asked first, then the defender is asked. (hakon)
* Showed convoy blockade dice rolls in History Panel even if the blockade damage is zero. (veqryn)

## Changes for 1.6.1.2

* Fixed bug in Paratroopers code, causing paratrooper attacks in coast territories on maps with scrambling to never actually take the territory. (veqryn)
* Creating a simple Ping method inside of the Chat Controller, that will ping all computers once every minute, hopefully improving everyone's connections. (Sean Bridges & veqryn)
* Allowing people to hold SHIFT down while their mouse is over a territory in order to keep that territory in the Territory Panel, no matter where they move their mouse afterwards. (frigoref)
* Changed EndTurnDelegate so that Units Changing Ownership, and Hitpoint Repair, will still happen even if you have lost your capital. (veqryn)
* Getting MooreAI to submerge subs if only enemy air is left. (hakon)
* Fixing "Edit Unit Bombing Damage" for maps that use territory based damage, such as ww2v3\. (veqryn)
* Allowing new option for the Play By Email / Play By Forum poster, to "Include Overall Dice Statistics" in the post/email. (veqryn)
* Improving the menu "GAME -\> SHOW DICE STATS" to give information per player, as well as totals. (veqryn)
* Getting engine to record if the dice thrown is in Combat or not, for the dice statistics. (veqryn)
* Getting engine to record which player is rolling dice for the dice statistics. (veqryn)
* Adding scroll bars to edit place unit panel and non-tabbed purchase unit panel. (veqryn)
* Fixing non-serialization error when attempting to save the game after a successful aa gun roll, but before selecting casualties. (veqryn)
* Improved bombing result display to show ignored dice if there are any, and improving history panel to show the rolls for each target unit. (veqryn)
* Fixed integer array error in Strategy Bombing with Heavy Bombers, causing the second half of all rolls to not be rolled, thereby defaulting to one each. (veqryn)
* Fixed null pointer for undoing a placement made by UK in global 1940 maps, caused by the new no-air-checking delegate [players will need to update their 1940 maps though]. (veqryn)
* Creating framework for TripleA to use proxies to connect to the internet. Allowing map downloading, PBEM/PBF, and dice servers to use a proxy. (veqryn)
* Improving "Draw Territory Borders On Top" so that it will automatically switch to "medium" if you are on "low/default" and are zooming, and switch back once you stop zooming out. (veqryn)
* Changing lobby moderator ban/mute options to make more sense, by only giving 3 options: name only, everything, or cancel. (veqryn)
* Adding a backup lobby properties location on the tripleawarclub, in addition to the one on sourceforge. (veqryn)
* Fixed null pointer error in MovePanel.selectEndPoint when clicking to move a unit to a territory with no connections. (veqryn)

## Changes for 1.6.1.1

* Fixing in loading old engine jars caused by odd pathnames. (veqryn)
* Made AA Guns appear in battle, then disappear after firing if they could not participate any further. (veqryn)
* Fixed bug causing stacked aa guns to all fire with the attack power of the most powerful aa gun in the group. (veqryn)
* Fixed some math bugs in low luck picking of aa casualties for maps with non-standard aa guns. (veqryn)
* Made massive updates to 1.5.2.1 and 1.6 so that they can work as 'old' jars and be run from 1.6.1.1 or future versions. (veqryn)
* Disallowing starting of games if game data is null. (veqryn)
* Allowing hosts to load an old savegame, causing old engine to join lobby and host directly, if they have the jar to run it. (veqryn)
* Allowing members in online lobby to join games hosted by older versions of triplea, if they have the jar to run it. (veqryn)
* Adding game version (GV), and engine version (EV), columns to lobby. (veqryn)
* Fixing many bugs in the handling of command line arguments. (veqryn)
* Adding Passworded (PW) column to lobby. (veqryn)
* Making game notes non-modal (doesn't stop all action til closed) and making it always on top so that you can read it while you play. (veqryn)
* Fixing movement validation to allow submarines that are transports to carry land units through other ships. (veqryn)
* Forcing default map selection when TripleA starts to avoid the last file path uri used if it is not within the user's triplea folder or the program's folder. (veqryn)
* Fixing bug with connections being lost during end of Air Battles, resulting in a game that can not continue. (veqryn)
* Made xml exporter also add original territory owner as occupiedTerrOf until such a time as we can just use originalOwner. (veqryn)
* Fixed bug causing land units carried by air units (paratroopers tech) to blitz unoccupied enemy territories on route if going behind enemy lines. (veqryn)
* Fixing bug preventing renamed hardcoded techs from working properly. (veqryn)
* Fixing some errors with Sliding Tiles game, Tic Tac Toe, and Kings Table. (veqryn)
* Cleanup and abstraction of some AI classes and constructors and superclasses. (veqryn)
* Fixed string index out of bounds error with notifications, and also forced them to shorten for the history event record, to 150 characters if needed by removing all html code then truncating the string. (veqryn)
* Fixed issue with moving of old fighters to a new carrier by making sure it only used the producer territory. (veqryn)
* Updating build to include old jars. Updating framework to ignore micro version numbers, so that 1.5.2.1 will also load 1.5.2.0 savegames, etc. (veqryn)
* Created dialog to ask user if they want to load an old savegame. Fixed framework so that it can load any old savegame if it can find an old engine to match. And added 1.6.0.0 jar engine. (veqryn)
* Including old 1.5.2.1 jar file with slight modifications, so that 1.6.1.1 can play 1.5.2.1 savegames by simply running them with 1.5.2.1, but as a separate application. (veqryn)
* Creating framework for loading older savegames using older included jar files. (veqryn)
* Fixing some errors with command line options, and abstracting some game running utilities. (veqryn)
* Fixing display error in old paratroopers tech that caused the land unit to appear to die with the air unit even after it has landed and survived any aa fire. (veqryn)
* Making sure technology still has an effect even if it is not in a player's tech frontier. (veqryn)
* Make sure the game chooser menu is cleared from memory after closed. (veqryn)
* Created method to maintain savegame compatibility between 1.6.1 and 1.6.1.1 with regards to techs. (veqryn)
* Removing static instances of all hardcoded Technologies. Everything now done with locally created instances per game data. (veqryn)
* Changed choose how "best dice roll" / "LHTR heavy bombers" works with Low Luck on, so that it will add a bonus equal to the number of dice sides divided by 6\. (veqryn)
* Fixing scrambling again, so that even an amphibious assault on an undefended (blitzable) land territory, from an undefended sea zone, will still trigger scrambling. (veqryn)
* Removed game stopping message about unlimited purchases, whenever a unit or item cost so little that you can buy more than 10000 of it. (veqryn)
* Fixed errors in build.xml for java included version and mac version. (veqryn)
* Fixed null pointer error in Dynamix AI. (veqryn)
* Fixed bug in freePlacementCapacity when placing land units in a territory that previously placed sea units in a sea zone bordering more than one land producer. (veqryn)
* Increasing max memory from 512mb to 640mb, and up to 768mb for online games. (veqryn)

## Changes for 1.6.1

* Rewriting build file and including META-INF, hopefully fixing issue with Gmail play-by-email emailer on linux machines. (rain)
* Changing trigger property changes to use "-reset-" instead of clear. Can now be used with any attachment option. (veqryn)
* Creating a reset method for every single attachment property. These can now be used to return a property to its default value. (veqryn)
* Fixing some bugs introduced into AI with the factory switch. (veqryn)
* Fixing null pointer error in Easy AI purchasing algorithm for getting costs of units. (veqryn)
* Changing maxDamage to default to 2 instead of -1\. This is for bombing type damage, and it acts as either a multiplier of territory value or as a hard set number depending on canProduceXUnits. (veqryn)
* Fixing AIs to no longer use isFactory, and instead use things like canProduceUnits, etc. (veqryn)
* Abstracting isFactory setting and matches to use the component parts. (veqryn)
* Deleting unit attachment, "isFactory", but keeping the setter so that old xml's will not break.

* Created new game option, "Submarines Prevent Unescorted Amphibious Assaults", that prevent unescorted transports from conducting amphibious assaults. (veqryn)
* Created new game option, "Kamikaze Suicide Attacks Only Where Battles Are", and implemented it. (veqryn)
* Fixed bug where land units would disappear when conquering a sea zone. (veqryn)
* Making kamikaze and interceptor dialogs non-modal so user can move around map while choosing. Again, saving during the dialog then reloading might have odd effects. (veqryn)
* Making scramble dialog non-modal so that the user can move the map around before choosing what to scramble. Note that saving the game while in the middle of scrambling can result in weird effects, so it is not recommended. (veqryn)
* Undoing update to java Substance 7.1, in order to maintain compatibility with Java 5\. (veqryn)
* Created edit option to change the amount of unit bombing damage on any and all units which can be damaged by bombing. (veqryn)
* Created edit option to change the amount of unit hitpoint damage on any and all units which can take more than 1 point of hit damage. (veqryn)
* Created edit option to remove technology from a player, except that shipyards and industrial technology can never be removed, and any technology that uses triggers is pointless to remove and removing will not undo their effect. (veqryn)
* Created edit option to add technology to a player. (veqryn)
* Adding methods to ensure that any power sharing technology (like British to UK Pacific) will still roll for war bonds even if its capital is taken, so long as the shared power is not able to have the warbonds technologies. (veqryn)
* Allowing additional nations to share the cost of technology, and creating a good user interface that dynamically adjusts to show how much is being paid by each nation. (veqryn)
* Created an option in Play-By-Forum and Play-By-Email to send the move summary after the combat move phase, in addition to the summary at the end of the turn. This is to help with OOL and scrambling orders. (veqryn)
* Abstracted EndTurnPanel into AbstractForumPosterPanel, then created MoveForumPosterPanel. (veqryn)
* Created new game option, "Remove All Tech Tokens At End Of Turn", which will remove tech tokens after each tech roll. (veqryn)
* Make savegames for long games, games with many players, and games with many battles, much smaller. (veqryn)
* Changing how Battle Records get added and removed from game data through the Change Factory to be more memory efficient. (veqryn)
* Adding an option for "None" to the list of territory effects. (veqryn)
* Added List to Battle Calc so that you can manually select one or more territory effects, hold down shift to select more than one. List will automatically fill with starting territory's effects. (veqryn)
* Fixed battle calc to make it try to use the territory that we select. (veqryn)
* Fixing bug in Battle Calculator where damaged units got turned into healthy units before each battle was calculated. (veqryn)
* Fixed null pointer error in triggerSupportChange caused by having a hashmap of an attachment class, inside of another attachment class, then deserializing this (loading a savegame), resulting in the hashmap being resolved before all its keys are, giving the wrong hashcodes to those keys. (veqryn)
* Updating java Substance to 7.1, and adding 14 more skins. (veqryn)
* Updated embedded Java JRE for windows executable version to Java 6 update 33\. (veqryn)
* Added a drawing method and menu option to have territory borders drawn a second time on top of the map. (veqryn)
* Changing IDrawable calls to use highest level of graphics rendering available. (veqryn)
* Fixing game selector model to no longer return to default game if we have trouble loading the uri of previous xml, and will instead try to pick by name first. (veqryn)
* Added new sounds for air, sea, and land battles, rockets, politics, and tech. (veqryn)
* Fixed issue where fighters moving alone were not asked if they want to escort. (veqryn)
* Made DefaultAttachment extend GameDataComponent. (veqryn)

## Changes for 1.6

* Fixing Global 1940 bugs, and getting it to use Technology completely. (veqryn)
* Allowed downloading of multiple maps/games in one go, by holding down CTRL while selecting maps in the "Download Games" dialog screen, and out of date maps will show up in bold, and maps up-to-date will show in italics. (ddurham)
* Created new rules attachment option, "switch", which allows either "true" or "false", thereby giving all conditions a memory function. (veqryn)
* Fixed bug where dependents of an air transport were not dying when the air transport was hit by AA fire, in the case where the air transports could fly deep into enemy territory and flew over an AA gun. (veqryn)
* Fixed parsing error in player attachment options: placementLimit, movementLimit, attackingLimit. (veqryn)
* Fixed fatal error in HistoryLog, caused by clearing an array that potentially gets accessed later at a specific index number, from doing an edit during a movement phase then doing an undo later. (veqryn)
* Created new game option, "Subs Can End NonCombat Move With Enemies", which allows submarines to end their noncombat movement in a sea zone containing any enemy units. (veqryn)
* Added information on which units are doing the bomber to the question about what should each bomber bomb. (veqryn)
* Fixed error from trying to undo a battle move created using another player's units, using edit mode. (veqryn)
* Fixed null pointer exception when not selecting the target for a bomber after an air battle is finished. (veqryn)
* Allowed interceptors and escorts to benefit from attackRolls and defenseRolls and their bonuses. (veqryn)
* Created new delegate, NoAirCheckPlaceDelegate, which does everything the normal "PlaceDelegate" does, but does not kill any aircraft at the end of the phase. (veqryn)
* Fixed issue with not being able to blitz through units owned by a power to which you were neutral with. (veqryn)
* Allowed loading of transports in Sea Zones where all enemies just became hostile this turn due to politics. (veqryn)
* Fixed issue with loading transports in the same sea zone where a transport was previously unload in a previous phase. (veqryn)
* Fixed issue with having multiple support attachment affecting the same group of units. The order of preference is now: highest bonus support first, then lowest number of supported types to highest number of types. (veqryn)
* Created new techAbilityAttachment option, "bombingBonus", which will add additional damage after all dice are rolled, per unit. (veqryn)
* Created new techAbilityAttachment option, "defenseRollsBonus", which adds additional defense rolls. (veqryn)
* Created new techAbilityAttachment option, "attackRollsBonus", which adds additional attack rolls. (veqryn)
* Created new UnitAttachment option, "chooseBestRoll", which controls whether we select the best dice or use all the dice rolled, when there is more than one die rolled. (veqryn)
* Created new UnitAttachment option, "defenseRolls", which controls the number of defense rolls a unit has, so long as their defense is greater than zero. (veqryn)
* Created new UnitAttachment option, "attackRolls", which controls the number of attack rolls a unit has, so long as their attack is greater than zero. (veqryn)
* Abstracted Heavy Bombers technology. (veqryn)
* Changed History Writer setRenderData to be part of a new event, instead of being a separate method. Also fixed some display issues with event and child messages. (veqryn)
* Created new techAbilityAttachment, "airborneTargettedByAA", which is set by the attacker, controlling which airborne units are subject to AA gun fire and by what AA gun types. (veqryn)
* Fixing error message for when a game xml is not correctly formed. Also preventing errors from being thrown until we check the version number. (veqryn)
* Deleted "GivesPUsDelegate". (veqryn)
* Finished airborne movement delegate, and technology. (veqryn)
* Created new techAbilityAttachment, "airborneBases", which turns on the new airborne tech. (veqryn)
* Created new techAbilityAttachment, "airborneDistance", which turns on the new airborne tech. (veqryn)
* Created new techAbilityAttachment, "airborneTypes", which turns on the new airborne tech. (veqryn)
* Created new techAbilityAttachment, "airborneCapacity", which turns on the new airborne tech. (veqryn)
* Created new techAbilityAttachment, "airborneForces", which turns on the new airborne tech. (veqryn)
* Created new game option, "Airborne Attacks Only In Enemy Territories", to help control different behavior for airborne tech. (veqryn)
* Created new game option, "Airborne Attacks Only In Existing Battles", to help control different behavior for airborne tech. (veqryn)
* Created Validation for Airborne movement. (veqryn)
* Created AbstractMoveDelegate and abstracted MoveDelegate into it. Created SpecialMoveDelegate to extend it, for use with new Paratroopers/Airborne tech. (veqryn)
* Fixed error preventing AI Flat Income Bonus from happening unless the Percentage Bonus was also set. (veqryn)
* Fixed repair panel to correctly set the max for each unit. (veqryn)
* Fixed error with displaying discounts for repairing. Also fixed that you may not be able to repair with all your money if you had a discount. (veqryn)
* Fixed null pointer error from having Edit Mode on while AA guns fire. (veqryn)
* Started coding for new paratrooper tech, to be called Airborne Forces. (veqryn)
* Fixed blockade zones so that they never do more damage than the combined total of their neighboring territories, even if there are multiple sea zones blockading a single or set of territories. (veqryn)
* Allowed createsResourcesList to have negative values as well as positive values. (veqryn)
* Created new Unit Attachment option, "bombingTargets", which allows the unit to only target specific other units for rockets and strategic bombing. (veqryn)
* Disallowed Bombardment from any sea zone that had a kamikaze suicide attack. (veqryn)
* Fixed failing unit tests. (veqryn)
* Expanded Tech delegate UI element to use helpPayTechCost. (veqryn)
* Created new PlayerAttachment option, "helpPayTechCost", which will allow other players to help pay the cost of technology. (veqryn)
* Created new PlayerAttachment option, "shareTechnology", which will automatically give all technology to other players during tech activation phase. (veqryn)
* Changed priority of AA casualty choosing system to: chooseAACasualties -\> isRollAAIndividually -\> isRandomAACasualties. This means that "choose aa" overrides all, while "roll aa individually" will only override "random aa". (veqryn)
* Allowed "unitAbilitiesGained" to give "canBlitz" and "canBombard". (veqryn)
* Created new techAbilityAttachment, "unitAbilitiesGained", which allows units to gain abilities when technology is discovered. (veqryn)
* Created new techAbilityAttachment, "rocketNumberPerTerritory", which controls the maximum number of dice to be rolled per territory. (veqryn)
* Created new techAbilityAttachment, "rocketDistance", which controls the maximum distance rockets can travel. (veqryn)
* Created new techAbilityAttachment, "rocketDiceNumber", which controls the number of dice each rocket rolls. (veqryn)
* Created new RelationshipTypeAttachment option, "rocketsCanFlyOver", which allows rockets to fly over by default. (veqryn)
* Created new techAbilityAttachment, "warBondDiceNumber", which controls how many dice get rolled for war bonds. (veqryn)
* Created new techAbilityAttachment, "warBondDiceSides", which controls how large the dice are which are rolled to determine the war bonds bonus. (veqryn)
* Created new techAbilityAttachment, "repairDiscount", which controls the discount to repairing given by any technology. (veqryn)
* Created new techAbilityAttachment, "minimumTerritoryValueForProductionBonus", which controls the minimum value of a territory that a factory units must be in to receive the production bonus. (veqryn)
* Created new techAbilityAttachment, "productionBonus", which controls the bonus given to production by any technology. (veqryn)
* Created new techAbilityAttachment, "airDefenseBonus", which controls the bonus given to interceptors defense by any technology. (veqryn)
* Created new techAbilityAttachment, "airAttackBonus", which controls the bonus given to escorts attack by any technology. (veqryn)
* Created new techAbilityAttachment, "radarBonus", which controls the bonus to radar AA attack given by any technology. (veqryn)
* Created new techAbilityAttachment, "defenseBonus", which controls the defense bonus given by any technology. (veqryn)
* Created new techAbilityAttachment, "attackBonus", which controls the attack bonus given by any technology. (veqryn)
* Fixed error with "Should not be adding battle record for player ...", which was caused by creating a battle using edit mode for a player who's turn has passed already. (veqryn)
* Fixed error with Low Luck AA guns when the dice side is different than 6\. Was trying to roll zero random dice. (veqryn)
* Fixed issue with not being able to move through submarines during noncombat if they were on top of convoy zones. (veqryn)
* Created new game option, "Convoy Blockades Roll Dice For Cost", which will now allow dice to be thrown for all blockade damage. (veqryn)
* Allowed multiple airbases in a single territory to stack for their max scrambling number total. (veqryn)
* Allowed defenseless attackers to be able to retreat if they can, instead of being forced to die. (veqryn)
* Possible fix for "Record Battle Statistics" occuring multiple times. (veqryn)
* Allowed all defending or attacking units to die, when there are none left who are capable of throwing dice. (veqryn)
* Fixed issue with maxScrambleCount not keeping track of scrambles for different sea zones by the same land territory. (veqryn)
* Semi-Fixed issue with not being able to retreat from a scrambled air defense. You can now retreat anywhere that does not have enemies. User should know where they came from and make legal move. (veqryn)
* Fixed issue with unloaded ground units not dying or being removed, even if their transports die from a scrambled air defense. (veqryn)
* Disallowed any unloading of ground units to a friendly territory, during combat move, if we have scrambling or kamikazes turned on. (veqryn)
* Fixed issue with "Scramble To Any Amphibious Assault" not working at all. (veqryn)
* Created new game option, "Use Bombing Max Dice Sides And Bonus", which will control the unit attachment options: "bombingMaxDieSides" and "bombingBonus". (veqryn)
* Stopped "Low Luck for Bombing and Territory Damage" from controlling "bombingMaxDieSides" and "bombingBonus", and made it create a Low Luck situation on top of whatever dice sides and bonus the map uses. (veqryn)
* Fixing comparison method in weak ai. (veqryn)
* Allowed users to download maps even if they come with triplea. (veqryn)
* Fixed Null pointer errors in Turn Summary Poster, and also fixed up Politics to display better in the turn summary with indents. Also stopped the poster from showing certain things like: game loaded, recording battle statistics, and giving bonus movement. (veqryn)
* Fixed a ton of lock not held errors that had resulted from new technology code. (veqryn)
* Fixed Economy panel so that it would change when you click back through history. (tao nie)
* Created new techAbilityAttachment, "movementBonus", which controls the bonus to movement that is received from any technology. Also created default attachment for Long Range Air, which will now be set to give +2 movement to all air units, that are air units at the start of the game. (veqryn)
* Created framework for interpreting TechAbilityAttachment's, and also setting of default attachments for hardcoded technologies. (veqryn)
* Created new type of attachment, TechAbilityAttachment, which will control how all technologies work. (veqryn)
* Refactored TechAdvance and GenericTechAdvance to extend NamedAttachable, that way they can eventually have attachments. (veqryn)
* Fixed bug where a NonFighting battle was attempting to add the result as a child in the history panel, without creating the event first. (veqryn)
* Fixed bug preventing Moore AI from placing Transport type sea units whenever it did not buy non-transport sea units. (veqryn)
* Clearing all cached data for AIs once a game has been left. (veqryn)
* Clearing cached data for Dynamix AI once a game has been left. (frigoref)
* Fixed issue with battles showing who won twice in the history panel. (veqryn)
* Moved BattleRecord to its own class, and having BattleRecord, BattleRecords, and BattleResults all extend GameDataComponent. (veqryn)
* Possibly fixed the problems with Edit Mode, by fixing a previous refactoring that switched two variables up. (veqryn)
* Possibly fixed the problems with Edit Mode, by abstracting BasePersistentDelegate and separating EditDelegate from BaseDelegate. (veqryn)
* Generating Serial IDs for all classes that may need them. (veqryn)

## Changes for 1.5.2.1

* Updated 1940 test xml to allow Axis powers to declare war on Americans separately, and for Americans to declare war on each Axis power separately. (veqryn)
* Fixed null pointer error in Dynamix AI's determining of where to put a factory. (veqryn)
* Having the default loaded game be loaded separately from the game chooser list, and putting the loading of the list into a separate thread. (veqryn & frigoref)
* Removing game chooser list from memory when we start a game, or join a game, or join the lobby. (veqryn & frigoref)
* Removed restriction of not being able to land in land territories with pending battles (there is still a restriction of course on who owns the territory, and whether it was conquered this turn or not). (veqryn)
* Fixing possible error with using overriden placement delegates that were not triplea placement delegates, like using twoIfBySea place delegates. (frigoref)
* Fixing bug where a territory that was taken without a fight, could still trigger a scrambling, with the wrong player selecting who scrambles. (veqryn)
* Allowing air to end their movement over sea zones containing enemy units, if you own or will place a carrier there. (veqryn)
* Disallowing new usernames for lobby if they match case insensitive an existing user, instead of checking only case sensitive. (veqryn)
* Speeding up lobby login process. (frigoref & veqryn)
* More fixes for sea placement and requiresUnits placement. (veqryn)
* Prevented units with "requiresUnits" from being placed by territories not containing the required units, and also prevented them from being moved around by the "free-up-space" methods. (veqryn)
* Fixed many small rare bugs in AbstractPlaceDelegate. (veqryn)
* Changing look of main screen, and adding tool tips for all buttons. (veqryn)
* Fixed possible Null Pointer error for maps with a production frontier of null rules. (veqryn)
* Fixed possible IllegalStateException in Air Battles. (veqryn)
* Allowed "Edit Moving" of units not owned by you, to create a battle by the unit's owner. (veqryn)
* Fixed 'uses' for 'when' based triggers to be used up right after they are used, while triggers without when set get 'used up' at the end of each round that they are used in. (veqryn)
* Fixed Air Battle to only allow aircraft capable of intercepting into the battle, instead of also allowing infrastructure too. (veqryn)

## Changes for 1.5.2

* Fixed infinite loop in getAllProducers for a sea placement. (veqryn)
* Removing BattleResults from BattleRecord until we figure out the problem (probably non Serializable) with it always causing the BattleRecordsList to be null. (veqryn)
* Moved all AI related code to new package. (veqryn)
* Fixing the bugs introduced into the engine, and the failing unit tests due to changes in how battles were abstracted, and how they are now recorded when finished. (veqryn)
* Created new type of battle, FinishedBattle (scripted), to handle blitzed and conquered territories. (veqryn)
* Created new Rules Attachment and Condition Attachment option, "battle", which can be used to test for the presence of battles. (veqryn)
* Major abstraction and cleanup of all battle related classes. (veqryn)
* Fixing bad comparisons, and fixing missing hashCode methods. (veqryn)
* Forced user preferences for individual sound muting choices to be saved by each local vm. (veqryn)
* Allowed individual sounds to be muted, and separated simple Messenging from Slapping with different sounds for each. (frigoref)
* Rewrote the framework for how sounds are loaded and played, in order to allow more flexible expansion of sound options. Moved sound files to separate user visible folder. (frigoref)
* Temporary hack fix for bug where client computer can not use paratroopers at all, but hosts can. (veqryn)
* Finalizing Alpha rules for test xml. (veqryn)
* Improving in-game Help -\> Movement/Selecting Help menu tips. (veqryn)
* Holding down ALT key while selecting or deselecting units will now add/remove 10 units at a time. (veqryn)
* Possible fix for battle window disappearing after closing, with battle panel not becoming visible again. (frigoref)
* Abstraction of ClientGame and ServerGame into AbstractGame. (frigoref)
* Deleting duplicate m_bridge variables that were hiding the real m_bridge variables of the extended classes. (veqryn)
* Maintaining compatibility with Java 5\. (veqryn)
* Abstraction of Launcher code to an abstract class. (frigoref)
* Fixed bug where sea placement could be done in territories captured this turn. (veqryn)
* Fixed bug with bid placement of sea units, which was previously not allowing them to be placed anywhere at all. (veqryn)
* Changed Battle Calculator to only count units that can die in combat, in the unit totals. No longer counts AA Guns or other units like Factories, in the unit totals, even if they are present. (veqryn)
* Fixed infinite loop in Dynamix combat calculation routine, resulting from thinking battles that were lost were really won, then increasing the number of defenders to try to reach a "losing" battle, except that no losing battle ever came. (veqryn)
* Preventing Dyanmix AI from purchasing any infrastructure or maxBuiltPerPlayer units. (veqryn)
* Reduced calls to find map resource paths to a single time, when the map is first loaded. Should speed things up a little. (veqryn)
* Fixed TripleA to ignore if the user has multiple folders with the same name in both of the "maps" directories that it reads from. TripleA will pick first from the user's maps folder, and pick second from the program's folder. (veqryn)
* Fixed failing unit tests. (veqryn)
* Fixed bug where if a defender wins a battle in a seazone, but has aircraft that can not land anymore, the aircraft had to choose right away where they wanted to land, forbidding landing in a territory with a pending battle.

* Fixed bug where aircraft + destroyer attacking a submarine, if the submarine kills the destroyer, the submarine may not yet submerge but should be allowed to submerge. (veqryn)
* Fixed bug where if the defender only has subs left, and submerges them, the attacker can still retreat, but should not be able to. (veqryn)
* Fixed bug where units unloaded from a sea zone with enemy units, to a friendly territory, would not die when the sea transports died. Fixed by making such moves illegal, forcing user to wait til after combat is resolved to offload. (veqryn)
* Fixed bug in new Sea Placement code that incorrectly validated how many could be placed, and incorrectly switched placements to the wrong territory. (veqryn)
* Fixing "Not in an event, but trying to add child" error for placing a carrier and moving fighters to be on it. (veqryn)
* Fixing email/forum turn summary poster to use

    \<pre\> and \</pre\>

    tags, instead of  . (veqryn)
* Fixed null pointer error in BattleRecordsList getTUVdamageCausedByPlayer. (veqryn)

## Changes for 1.5.1

* A second possible fix for ConcurrentModificationException in BattleModel.refresh -\> DiceRoll.isAmphibiousMarine -\> BattleTracker.getPendingBattleSites. (veqryn)
* Changed Sea Placements to use all production for all surrounding Factories, if multiple factories touch that sea zone. Will now dynamically shift the production of other sea units away to other legal factories in order to allow the maximum production possible. (frigoref & veqryn)
* Fixed null pointer error in trying to place a construction to a sea zone. (veqryn)
* Locking the map when user's mouse is over the history panel, and then unlocking for each click on a history node. (frigoref) [edit: this is undone/rolled-back for now, pending finding a better way to lock/unlock a user's interface without writing to the cache/registry each time]
* Fixed bug where Rounds would not appear in a Client game. (veqryn)
* Creating a NullModeratorController class for locally hosted games. (veqryn)
* Fixed bug where steps appear out of order in a client game's history panel. (frigoref)
* Created new Trigger Attachment option, changeOwnership, which will allow a map to have the owner of a territory change by trigger. (veqryn)
* For Trigger Attachment option "removeUnits", now allowing the use of "all" in place of the territory name, and also "all" in place of the unit type. Can be used to remove all units from some or all territories. (veqryn)
* Correcting politics for Alpha xml. (veqryn)
* Changing game property, Selectable Tech Roll, to also work with WW2V3 Tech Model, allowing the user to select which tech they want after a successful roll. Also fixed the dice chooser to let you set the sides. (veqryn)
* Fixing bugs in new air movement validation, and improving speed and efficiency. (veqryn)
* Completely rewrote the validation of air unit movement, and moved it to a new class, AirMovementValidator.java (veqryn)
* More work on rewriting MoveValidation of air units. (veqryn)
* Allowed for the use of the Arrow Keys for navigating around the map. (frigoref)
* Adding [Mod] tags onto the names of any Admins in the online lobby. (veqryn)
* Possibly correcting some hidden bugs in MoveValidator. (veqryn)
* Created new CanalAttachment option, excludedUnits, which allows the specifying of specific units which will not be validated for. (veqryn)
* Created new RelationshipTypeAttachment option, canMoveThroughCanals, which allows a player to move through a canal owned by the other player. (veqryn)
* Removed restrictions that had canals only checked for Sea Movement. They now check for all movement, and therefore there can now be 'land' canals that require sea zones, or land requiring other land, or sea requiring sea, etc. (veqryn)
* Creating a better error message for when users do not have a map, but try to join the game anyway. (frigoref)
* Getting history panel to stop closing clicked on expanded paths every time a there is a new event or change, when your mouse is over the history panel. (frigoref)
* Correcting bad history log messages for Edit mode. (veqryn)
* Refactored Trigger Attachment class again to allow triggers to fire other triggers with certain options and properties. (veqryn)
* Created new Trigger Attachment option, activateTrigger, which will allow a trigger to fire other triggers. (veqryn)
* Preliminary work on ability to fire triggers from other triggers. (veqryn)
* Fixing NoSuchElementException in Kamikaze attack ui. (veqryn)
* Created new RelationshipTypeAttachment option, canMoveIntoDuringCombatMove, which stops combat-phase movement, but allows non-combat-phase movement. (veqryn)
* Fixing Chat Panel player name area to be correct size to hold all player names and national flags. (frigoref)
* Adding Alpha+3 National Objectives to xml. (veqryn)
* Added "originalNoWater" as an option for conditions that test territories. (veqryn)
* Fixed bug where paratroopers could not move over enemy sea zones or captured sea zones. (veqryn)
* Fixed bug with moving sea units through sea units belonging to a power not yet at war with. Also possibly fixed bug with Easy AI's comparison method contract. (veqryn)
* Adding Global 1940 alpha 3 as test xml. (veqryn)
* Fixing bug where the neutral (null) player might be asked if it wants to scramble, which gives an error. (veqryn)
* Adding Play-By-Forum method for TripleA War Club, http://www.tripleawarclub.org/ so that people can also play there. (qwertgold)
* Fixing Battle Calc to not include units that are irrelevant to combat. (veqryn)
* Made sure all m_variable types in attachments exactly match the new instance type that is used. This, combined with the previous 2 changes, should fix the history panel bugs that are being caused by not being able to find the correct setter. (veqryn)
* Changing the way the ChangeFactory uses PropertyUtil for getting the old value of properties. Previously relied on the "get" method for getting the old value. Now it will directly access and store the "m_" object. getRawProperty no longer used. (veqryn)
* Allowed changes to all attachments to be undone and redone in the history panel, by ensuring each setter has an additional setter for an object of the field's type. (veqryn)
* Preventing history panel from updating if moused over, and allowing it to scroll down if not. (frigoref & veqryn)
* Allowing route to recalculate if only air can make it. (frigoref)
* More optimizations of getBestRoute. Also changing "Parse Selected" to be default parsing strategy of maps. (veqryn)
* Changing getBestRoute to not use territories for which the owner's relationship with us does not allow us to pass. (veqryn)
* Fixing getBestRoute to never use impassible and restricted territories. (veqryn)
* Adding Global 1940 as test xml. (veqryn)
* Fixing weird tech attachment getters to use booleans rather than strings. (veqryn)
* Making sure that all attachment variables that start out as Null, can return to being null again through their setter. (veqryn)
* Fixing various errors introduced into casualty selection. (veqryn)
* Fixed null pointer error for players who have damaged units but no repair frontier. (veqryn)
* Adding Europe 1940 as test xml. (veqryn)
* Fixed more "Lock not held" errors, and a potential null pointer in the battle calculator. (veqryn)
* Possible fix for ConcurrentModificationException in BattleModel.refresh -\> DiceRoll.isAmphibiousMarine -\> BattleTracker.getPendingBattleSites. (veqryn)
* Fixing bug with displaying up total resources when more than one unit creates resources. (veqryn)
* Allowed users to use Edit Mode to create new units for normal players, based on both their production frontier and any units they have on the board. (veqryn)
* Allowing users to use Edit Mode to create and place new "Neutral" (null player) units, but only selecting from ones on the board. (veqryn)
* Allowing users to Battle Calc against any "Neutral" (null player) units that are still on the board. (veqryn)
* Fixing casting error bug introduced into battle calc. (veqryn)
* Changing airfields and harbours to stop being operational at 3 damage, instead of 4\. (veqryn)
* Fixed bug where you were not allowed zero (0) for the unitPresence count. (veqryn)
* Making the check to see if you can do the purchase phase, the same for both humans and AIs. (veqryn)
* Fixed null pointer error for when a player runs low on resources. (veqryn)
* Fixing a couple "Lock not held" errors. (veqryn)
* Fixed the Battle Calculator not displaying combat units with 'AA' abilities. (veqryn)
* Fixed the "Cant add an event, not a step" bug for adding AddBattleRecordsChange. (veqryn)
* Fixed bug with Air Battles where there were more hits than aircraft. (veqryn)

## Changes for 1.5

* Adding new Game-Play manual. (victor, veqryn, hepster)
* Fixing build xml to export new docs. (veqryn)
* Fixed major bug with new Delayed parsing method, it will now correctly handle maps with errors in them by removing them from the game chooser list. (veqryn)
* Creating better error messages for setting attachment options in xmls. (veqryn)
* Fixing bug where suicide attack units could target units in transports. (veqryn)
* Some major bug fixes to movement with paratroopers, including not allowing units with multiple movement to move through all enemies once you get paratroopers. (veqryn)
* Created new game option, "Paratroopers Can Attack Deep Into Enemy Territory", which will allow movement for air transports during combat move over enemy territories. (veqryn)
* Deleted Player Attachment stackingLimit and replaced with movementLimit, attackingLimit, and placementLimit. (veqryn)
* Deleted Unit Attachment stackingLimit and replaced with movementLimit, attackingLimit, and placementLimit. (veqryn)
* Fixing potential bugs with new .equals for all attachments. (veqryn)
* Disabled political action button when taking actions, to prevent taking multiple actions while waiting for confirmation of the first. (veqryn)
* Fixed major error preventing politics from working over the network, due to the new way condition testing works. (veqryn)
* Fixed Lock not held errors for politics. (veqryn)
* Changed political panel to use a split panel, and added the one-touch-expandable feature to all main game screen panels: map panel, chat panel, and history panel. (veqryn)
* Added scroll bars to main screen player selection area. (frigoref)
* Created option to have TripleA not parse every single xml at startup, and only parse as each game is selected. (veqryn & frigoref)
* Added new button to main screen, Engine Preferences, which lets a user select various properties specific to the the triplea engine, like setting the look and feel, etc. (veqryn)
* Added scroll bars to both political overview and political action screens. (veqryn)
* Fixed serious bug in DefaultAttachment.getRawProperty() and getFieldIncludingFromSuperClasses, and also updated attachment/annotation test to search super's fields. (veqryn)
* Making some small fixes to attachment/annotation test, and renaming any methods with attach to attach. (veqryn)
* Added wait window to TripleA's startup. (frigoref)
* Changed name of Dynamix to be Land-Only AI, at least until someone decides to start working on the AI again. (veqryn)
* Completely updated the game xml exporter to TripleA 1.5, except that attachments are just copies of what was parsed from the xml originally. (veqryn)
* Fixed null pointer error in Bid Placement when undoing a placement. (veqryn)
* Created new Player Attachment property, stackingLimit, which allows stacking limits to be enforced flexibly per player, with multiple rules allowed for owned, allied, and total units. (veqryn)
* Created new Rules Attachment property, players, which can be used with directOwnershipTerritories, directExclusionTerritories, directPresenceTerritories, or any of the other territory lists, to customize which players are required to own/occupy the territories. (veqryn)
* Fixing new attachment setter annotation tester, and renaming some isXX methods to getXX. (veqryn)
* Fixing a unit test by removing static instances from messenger classes. (qwertgold)
* Adding @InternalDoNotExport or @GameProperty onto all setter methods in all attachments, and also unit and tripleaunit. (veqryn)
* Creating annotations to be used for tracking and marking various setters for attachments and other game data. (qwertgold & veqryn)
* Changing how attachments are created by the game parser. (frigoref & veqryn)
* Changing build.xml and editing a test suite to ignore certain tests for the time being. Also setting svn to ignore 'classes.jar', 'fb.xml', and 'TEST-games.strategy.AllTests.txt/xml'. (qwertgold)
* Adding findbugs folder for use with ANT. (qwertgold)
* Creation of new xml entry, \<triplea minimumversion="1.5"\>, which should be used by ALL new maps. If an older TripleA tries to play a map built for a newer TripleA, then it will simply ignore the map instead of throwing tons of java errors at the user. (veqryn)\</triplea\>
* Complete rewrite of AxisAndAllies.org forum poster. Also added help html pages for the pbem / pbf system. (qwertgold)
* Creating some unit tests for purchasing with multiple resources. (edwin van der wal)
* Adding folders for future resources images, and filling with some general images. (veqryn, hepster, rofl)
* Finished phase 5 of refactoring of aaGuns, separating isAAforFlyOverOnly from isAAforCombatOnly, and creation of an option to force attacks at the end of a movement, and allowing attacks to be filtered based on accompanying units, thereby finally reaching compatibility with silly pacific rules. (veqryn)
* Created new game option, "Force AA Attacks For Last Step Of Fly Over", which will force isAAforFlyOver to shoot for the last step of a route, which it normally does not. (veqryn)
* Created new Unit Attachment, "willNotFireIfPresent", which will be used to prevent an AA unit from firing at all if the enemy has any of a list of units in the battle. (veqryn)
* Created new Unit Attachment, "isAAforFlyOverOnly", which will be used to determine if there are any AA shots for units passing through a territory. (veqryn)
* Finished phase 4 of refactoring of aaGuns, by allowing aaGuns to stack, overstack, and getting maxAAattacks to work, thereby allowing aaGuns to shoot a limited number of times instead of infinite. (veqryn)
* Created new Unit Attachment, "mayOverStackAA", which will be used to allow more AA shots than the total number of aircraft/targets. (veqryn)
* Created new Unit Attachment, "maxAAattacks", which will determine the maximum number of times an AA gun will be allowed to fire per round. (veqryn)
* Finished phase 3 of refactoring of aaGuns, by removing the artificial constraints placed on AA guns and allowing them to operate flexibly, targeting different kinds of units, and having multiple groups of aa guns firing separately. (veqryn)
* Created new Unit Attachment, "targetsAA", which determines what units may be hit by the AA fire of a unit. Defaults to all air units. (veqryn)
* Created new Unit Attachment, "typeAA", which determines which 'group' an AA unit belongs to. Each group gets to fire once, and only 1 unit in each group may fire. (veqryn)
* Fixed bug in Anti Aircraft low luck where engine ignored attackAAmaxDieSides completely. (veqryn)
* Finished phase 2 of refactoring of aaGuns, by removing internal references and variables for isAA for rockets, capturing, and aa for bombing and for combat. (veqryn)
* Finished phase 1 of refactoring of aaGuns, by removing isAAmovement and removing isAA from dealing with any aspect of movement validation and stacking limits in the engine. Both isAAmovement and isAA just call the two new methods below when they are created. (veqryn)
* Created two new Unit Attachment options, "canNotMoveDuringCombatMove" and "stackingLimit", which will take the place of previous isAA and isAAmovement abilities while making them more flexible. (veqryn)
* Allowed for Dice Skins, which can be placed in the "dice" folder of a map's directory. (crystalct & veqryn)
* Created new player attachment, suicideAttackTargets, which lets you set which units can be targetted during a kamikaze suicide attack. Also fixed null pointer error for neutral owned kamikaze zones. (veqryn)
* Created new game option, "Kamikaze Suicide Attacks Done By Current Territory Owner", which allows you to change from the default of the original owner, to the current owner. (veqryn)
* Cleanup of new PBEM code, and some bug fixing. (qwertgold)
* Added new Territory Effect Attachment option, noBlitz, which disallows certain units from blitzing in this effect, and also some general cleanup. (edwin & veqryn)
* Redoing PBEM system to fix bugs and add features. (qwertgold)
* Adding Pacific 1940 updated to use Kamikaze attacks to the test xml suite. (veqryn)
* Fixing bug where changing attachment properties of abstracted attachments failed. (veqryn)
* Created new ui for humans to select what they want to attack for these special attacks, and set the AI to just attack randomly. (veqryn)
* Created framework for performing special attacks at the beginning of the battle phase, using resources instead of units. (veqryn)
* New game option to enable kamikaze attacks, "Use Kamikaze Suicide Attacks". (veqryn)
* Created new Player Attachment, suicideAttackResources, which is the resource and attack value we will use for Kamikaze Suicide Attacks. (veqryn)
* Changed most iterator loops into enhanced for loops. (frigoref)
* Changed most instances of Node to Element in the game parser. (edwin van der wal)
* Created new unit attachment, fuelCost, which allows a unit to use up a resource for each point of movementCost they use. (edwin van der wal)
* Update of Export Stats to include information on all resources costs, not just PUs. Also fixed production screen to show all resources except techTokens and VPs. (veqryn)
* Creation of "Economy" tab, besides stats panel, which carries current information on all resources owned by the players. (edwin van der wal)
* Allowed resizing of the right side panel. (edwin van der wal)
* Created ability for Game Options to be saved as default options. (qwertgold)
* Updated Napoleonic Empires FFA to use the new destroyedTUV instead of upkeep. (veqryn)
* Created new RulesAttachment, destroyedTUV, which allows you to check if a player has destroyed at least X enemy non-neutral TUV this round or all rounds. (veqryn)
* Created methods inside BattleRecord related classes in order to record the TUV lost during all battles, for the attackers and the defenders. (veqryn)
* Created BattleRecordsList to keep track of all BattleRecords, and made it be updated after the BattleDelegate ends by use of the ChangeFactory. (veqryn)
* Created new data object, BattleRecord, in order to record more information about the battles that take place, and BattleRecords to keep track of these inside the BattleTracker. (veqryn)
* Completely re-wrote Convoy Routes to be flexible and work with any territories, not just sea zones. Can now be used to many any territory require any other group of territories in order to receive income.

* Updated Territory tab, beside stats tab, to carry significantly more information about the territory your mouse is currently over. Also put scroll bars on the list of units. (veqryn)
* Created new Territory attachment, "resources", which will allow territories to produce other resources besides PUs. (veqryn)
* Fixed engine to allow multiple resources for purchasing of units and repairs. Added new panel on stats tab to show additional resources. (edwin van der wal)
* Phase 4 of abstraction, RulesAttachment now abstracted into RulesAttachment, AbstractRulesAttachment, and AbstractPlayerRulesAttachment. (veqryn)
* Created a new overlay for territory effect images, that is enabled in map.properties map.useTerritoryEffectMarkers=true, territory_effects.txt, and territoryEffects folder. (edwin van der wal)
* Fixed bug where 'when' based triggers did not fire at all. (veqryn)
* Fixed bug where default based triggers were firing multiple times for each default firing location. (veqryn)
* Created new Trigger Attachment, removeUnits, which allows you to remove units from a territory for selected players. (veqryn)
* Created new Trigger Attachment, chance, which allows you to have a certain chance for a trigger to activate (tested only after all conditions are true). (veqryn)
* Phase 3 of abstraction of RulesAttachment and TriggerAttachment and PoliticalActionAttachment: the creation of an abstract class to hold all common cold related to conditions. (veqryn)
* Created new rules attachment for conditions, chance, which allows you to have a certain chance for a condition to be true. (veqryn)
* Temporary fix for the issues caused by only testing political conditions once. Now we test them after each political action. (veqryn)
* Updated political action attachments validation to only test once per politics phase for all the conditions for each action. (veqryn)
* Created new relationship attachment, givesBackOriginalTerritories, which lets a player give back originally controlled territories to another player. (veqryn)
* Changing PropertyUtil from using getClass().getDeclaredMethods() to using getClass().getMethods() for changing data inside game data objects, like units, players, attachments, etc. (veqryn & frigoref)
* Extended Objective/Condition attachment count "each" to work with Triggers "resource", "purchase", and "placement". (veqryn)
* Fixing null pointer errors and conceptual problems with my way of testing all conditions. (veqryn)
* Phase 2 of abstraction and refactoring of TriggerAttachments: now all triggers get called through a single method, collectAndFireTriggers. (veqryn)
* Created getAllConditionsRecursive and testAllConditions which will test get and test all ICondition, and now all RulesAttachments get tested through these. (veqryn)
* Had RulesAttachment, TriggerAttachment, and PoliticalActionAttachment all implement ICondition. (veqryn)
* Created ICondition, and interface for any Attachment that had conditions as a part of it. (veqryn)
* Moved actions for victory trigger and notification trigger to be part of the trigger attachment so that they will return void, and therefore can abstract easier. (veqryn)
* Deprecating TriggerAttachments "trigger", and changing name to "conditions" in order to match the other uses of condition attachments. (veqryn)
* Phase 1 of abstraction of TriggerAttachments, creation of AbstractTriggerAttachment. (frigoref)
* Fixed bug where I could move my tanks and all land units over water, so long as the end was land. (veqryn)
* Allowed players with canTakeOverOwnedTerritory to take over during noncombat move. (veqryn)
* Created new relationship type attachment, canTakeOverOwnedTerritory, which will allow taking over of an ally's territory. (veqryn)
* Fixing gamenotes for Lord of the Rings Middle Earth. (veqryn)
* Created new relationship type attachment, canLandAirUnitsOnOwnedLand, which decides if units can land in a player's territory or not. (veqryn)
* New Map Skin for Napoleonic Empires, which can be enabled in the View menu. (pulicat)
* Changed BattleModel to show air battle units with different stats then their normal attack/defense stats. (veqryn)
* Made sure units participating in air battles did not participate in any other battles. (veqryn)
* Created launching of interceptors component for air battles. (veqryn)
* Created dice rolling component for Strategic Bombing Air Battles, including for Low Luck. (veqryn)
* Moved 'Fire' out of MustFightBattle with the hopes of abstracting it and making it a general class one day. (veqryn)
* Created battle steps and interfaces for Air Battle, but still not done actual combat. (veqryn)
* Created ability for Air Battles to create Bombing Raids when they are finished if any bombers remain. (veqryn)
* Created new unit attachments, "canIntercept", "canEscort", "airDefense", "airAttack", which can be combined with new game option, "Raids May Be Preceeded By Air Battles", to allow air battles. (veqryn)
* Abstracted hashCode and equals methods from all battles and put into AbstractBattle class. (veqryn)
* Created StrategicBombingRaidPreBattle class, which will handle air battles and other things that occur before bombing raids. (veqryn)
* Changes to allow Strategic Bombing raids to have multiple targets, with units assigned to different targets. (veqryn)
* Some further abstraction of AbstractBattle class. (veqryn)
* Cleanup of some tests to use ChangePerformer to edit data directly, instead of Change.perform(). (frigoref)
* Allowed scrambling to any territory, and allowed moving the units after scrambling is completed, to anywhere. (veqryn)
* Allowed scrambling units to move to find new landing zones if their originating territory was taken or they are not forced to return to it. (veqryn)
* Wrote new Scrambling ui dialog from scratch, and made it work over the network. (veqryn)
* New game option, "AI Bonus Income Flat Rate", which gives a flat bonus every turn to all AIs. (veqryn)
* Changed PlayerID.getData() to be deprecated, and removed all uses of it that I could. (veqryn)
* Fixed various bugs in Scrambling, like not having dependent battles, not adding the units to existing battles, not removing units from old battles. (veqryn)
* Completely re-wrote how scrambling works. All scrambling now takes place before any battles begin. (veqryn)
* New game option, "Scramble To Any Amphibious Assault", allows bases not being attacked to scramble to defend bases that are being attacked amphibiously. (veqryn)
* Allowed double clicking on a game in the lobby to equal joining that game. (veqryn)
* Removing all scrambling code from the engine, in order to start over and code correctly. (veqryn)
* Created new TripleAUnit variable for keeping track of bonus movement, and eliminated use of unit attachment getMovement. In order to see a units movement, please use either getMaxMovementAllowed() or getMovementLeft(), both in TripleAUnit. (veqryn)
* Complete cleanup of all code, adding final on to everything that can take it. (veqryn)
* Redoing of movement validation to use movement costs, and completely rewriting the movement validation of carriers and aircraft for landing zones. (edwin van der wal)
* Refactoring Route class to use movement costs, rather than number of steps. (edwin van der wal)
* Changing the internal logic of scrambling to correctly test for the max scrambling length, and a new unit attachment, maxScrambleCount, which determines how many units can scramble. (bung)
* Allowed "each" as a count number for National Objectives, which then multiplies the bonus by the number of territories in that list who have their conditions met. (veqryn)
* Network menu option, "Show Who is Who", now shows players who are AI. (veqryn)
* Players who have both no movable attacking land units units, and either no factories or no land, will no longer be able to do any political actions, and any political actions affecting only them can not be done. They will now auto-accept any action from another player in addition. (veqryn)
* Allowed alliances to stop having war with each other. (veqryn)
* Allowed players to leave an alliance completely, with all members. (veqryn)
* Forced all alliance players to go out of war if one of them goes out of war, with a player. (veqryn)
* Forced players to have their ally's agreement when going into or out of war, and letting new people into the alliance. (veqryn)
* Created new relationshipTypeAttachment, isDefaultWarPosition and alliancesCanChainTogether, which handle if and when relationships will chain. (veqryn)
* Created new game option, "Alliances Can Chain Together", which causes anyone who is allied with your ally, to become your ally, and any of your ally's enemies to become your enemy. (veqryn)
* Created new game option, "Relationships Last Extra Rounds", which lets a player have relationships last additional or fewer rounds than default. (veqryn)
* Added ability for TripleA to remember which type of player you selected when you reload the game. And fixed bug where hosted online games did not remember your selection. (veqryn)
* Added methods for AI to cheat in all games, using new properties: "AI Bonus Income Percentage", "AI Bonus Attack", "AI Bonus Defense". (veqryn)
* Fixed "not all units can blitz" bug. (veqryn)
* Made the engine write who (ai/human/client) is playing each player, each time game is loaded, to the history panel. (veqryn)
* Adding political map skin, and reconstructed basetiles, for Napoleonic Empires. (veqryn)
* Stopped blitzing out of a combat into further combat, if you began in same territory. (veqryn)
* Allowed less strict Edit Mode options. (veqryn)
* Changed PlayerID to record if the player is Human or AI, and which type of AI. (veqryn)
* Allowed territories with now hostile units to be redrawn, and have red markup, at the end of the politics delegate. (veqryn)
* Fixed bug where you could capture territory from a power you were neutral or allied with, if you attacked an enemy on their territory. (veqryn)
* Fixed multiple bugs surround territories suddenly made hostile. And created a new class, "RouteScripted", which allows for Routes that do not follow the normal rules. (veqryn)
* Fixed bug where territories with no units, had enemy units in them from a previous turn, did not start any battle, and where therefore never taken over. (veqryn)
* Fixed null pointer in Moore AI for when it owns a factory in a territory it does not control. (veqryn)
* Created new unit attachment, "special", which currently allows for "canOnlyPlaceInOriginalTerritories". (veqryn)
* Fixed zoom out and zoom in on the map with the Mouse Wheel, by holding down the "ALT" key. (veqryn)
* Changing relationship type attachment, upkeepCost, to allow an integer percentage, which will effect all income gained during the end of turn step. (veqryn)
* Re-allow booting (boot-slapping) of admins. (veqryn)
* Allowed double clicking for selecting a game, and had the choose game list be cached, with a refresh button. (qwertgold)
* Fixed bug in stats and xml exporter where the file name contained illegal characters, causing the file creation to fail. (veqryn)
* Fixed bug where clicking cancel in order to look around the map, during casualty selection, generated an error. (frigoref)
* Fixed bugs in alliance tracker related to players not being in an alliance. (veqryn)
* Fixed bugs in 'example' maps: Tic Tac Toe, King's Table, and Sliding Tiles 8-number. (veqryn)

## Changes for 1.4

* Adding politicstext.properties for Napoleonic Empires. (veqryn)
* Massive update to Napoleonic Empires: FFA, to allow it to use Politics. (veqryn)
* Updating Pact of Steel 2 and Pacific test xmls. (veqryn)
* Added scroll bars to select casualties dialog panel. (veqryn)
* Sorted political actions based on player, type, and name. (veqryn)
* Capped Politics ui actions, and added scroll bars to the bottom button part. (veqryn)
* Fixed rendering issue where nations that were neutral to each other still caused red markup when in the same territory or sea zone. (frigoref)
* Fixed bug where victory city victories happened in FFA maps according to the current alliance rather than the player's alliance tracker. (veqryn)
* Added "upkeepCost" as an attachment for RelationshipTypeAttachment, which allows you to have a cost in order to maintain a relationship. (veqryn)
* Changed "invert" in rules attachments, trigger attachments, and political attachments, to work as a real logical negation. Now correctly follows boolean math. (veqryn)
* Added roundValue to relationshipInitialize, which is the beginning round a relationship starts out at. This should normally be "1", but if you have certain conditions set up, you may wish to change this to a negative or positive number to reflect what round you would like the condition to be true on. (veqryn)
* Made AI behavior towards politics to be a bit more random, allowing it to take any political action so long as it has 10x the amount of PUs as the political action's cost. (veqryn)
* Abstracting isMet logic for rules attachments into a single place, areConditionsMet, in RulesAttachment. (veqryn)
* Changed unitPresence to allow inputting of multiple units on one line for an OR relationship between those units. (veqryn)
* Fixed bug surrounding infinite loop caused by having nations A and B neutral with each other, but at war with C nation owning both subs and transports in a sea zone, attacked by the C nation. (frigoref & veqryn)
* Fixing bug introduced into must fight battle, by the battle class abstraction. Also slightly updating the dev documentation. (frigoref)
* Changed triggers "uses" to use up a single 'use' every round that they are used. So a trigger with 4 action types will use up a single use (instead of 4), assuming those four actions were done in the same round. (veqryn)
* Some code cleanup. (veqryn)
* Fixed null pointer error in Moore AI's rank territories method, due to politics change. (veqryn)
* Adding PoliticalActionAttachment to the list of attachments that triggers can change through players + playerAttachmentName + playerProperty. (veqryn)
* Adding invert and conditionType to Political Action Attachments, also changing conditions to allow multiple conditions. (veqryn)
* Changing Pact of Steel 2 to allow for politics, without greatly affecting the game. (veqryn)
* Adding baseAI code for AIs to declare war on people. (edwin van der wal & veqryn)
* Abstraction of various fighting battles into AbstractBattle, and renaming of Battle.java to IBattle. (frigoref)
* Added ability for BaseDelegate to keep track of whether triggers have fired or not, and changed all delegates to record and load super's saveState data when saving and loading. (veqryn)
* Some small ui fixes for politics. (edwin van der wal)
* Removing @Overrides for implemented methods, in order to maintain Java 1.5 compatibility. Also removing unnecessary casting. (veqryn)
* Adding web links to normal game menu bar, and also adding link for guides page on triplea homepage. (veqryn)
* Created two new game options, "Use Politics" and "Units Can Be Changed On Capture". (veqryn)
* Fixing bugs in last patch on politics. Deleted relationshipExistance and instead made it part of "relationship" setter. (veqryn)
* Added Politics UI. (edwin van der wal)
* Created relationshipExistance property in RulesAttachment, if this is set in combination with a relationship property, the relationshipExists property will indicate the number of complete rounds this relationship needs to have been in existance. (edwin van der wal)
* Created new attachment, politicalActionAttachment, which sets which actions are allowed during the politics phase for a player. (edwin van der wal)
* Removing trigger when notifications from TripleAPlayer (because no gamedata changing logic should ever be in TripleAPlayer), and moving them to basedelegate. (edwin van der wal & veqryn)
* Fix for Casualty Reset Bug 1730391, where casualty screen clears after saving and reloading. (frigoref & veqryn)
* Changed whenCapturedChangesInto to allow the transferring of combat damage and unit damage to the new units. (veqryn)
* Changed whenCapturedChangesInto to allow creating multiple unit types and multiple of a unit. (veqryn)
* Changed whenCapturedByGoesTo to not work when liberating an ally's territory. (veqryn)
* Created new unit attachment, whenCapturedChangesInto, which allows you to have a unit change into a different unit type when it is captured. (veqryn)
* Created new territory attachment, whenCapturedByGoesTo, which allows you to have a territory be given to another player when captured by a certain player. (veqryn)
* Workaround fix to screenshot export bug. (edwin van der wal)
* Code cleanup of needless casting. (veqryn)
* Code cleanup of warnings. (veqryn)
* Fixed bug in Increased Factory Production tech, where it discounted any units bought by half, so long as you bought only 1 type of unit this turn. (veqryn)
* Allowing the map to be redrawn if territory attachments are changed mid-game. (veqryn)
* Fixed null pointer error in Moore AI, and also an incorrect validation of warning the user when they have produced more than they can place. (veqryn)
* Fixing some bugs based on FindBugs, and general code cleanup. (veqryn & edwin van der wal)
* Fixed bug where memory for online and hosted games was set artificially low at 128, instead of being set to the max memory set by triplea run scripts and exe. (veqryn)
* Removing one memory leak from battle calc, it was recording the units is created to game data, inflating the savegame size. (veqryn & frigoref)
* Source code formatting on entire engine. (veqryn)
* Using cleanup to add @Override to anything that overrides something. (veqryn)
* Correcting problems with frig last patch to do with extended methods no longer overwriting super's methods. (veqryn)
* Removing more needless gamedata passing. (frigoref)
* Some general code cleanup, especially with iterators and rawtypes. (veqryn)
* Removed needless gamedata passing, and added methods to get game data out of bridge. (frigoref)
* Updated export stats to display far more information, about actual techs gained, and number of each unit type for each player, etc. (veqryn)
* Updated game data to record the playerIDs of whoever wins the game. (veqryn)
* Started making tests for all the features added in the last year. Made placeholder tests for everything revision 2800-3000\. (veqryn)
* Changing UIContext.m_mapDir static, so that is may be accessed anywhere. (frigoref)
* Added information on productionRules and UnitTypes to the export stats function. (veqryn)
* Changed some string comparing from == and != to .equals() and !.equals(). (veqryn)
* Created new rules attachment, placementAnySeaZone, that allows placing sea units beside any land territory owned at the beginning of the turn. (veqryn)
* Fixing bugs in old victory conditions and moving them to endRoundDelegate, and also fixing bugs surrounding strings in attachment property change triggers. (veqryn)
* Adding PactOfSteel2 and Pac40 xmls to test xml suite. (veqryn)
* Changed destroyedWhenCapturedBy to allow destroying when capturing from a player, not just by a player, by adding a prefix of "BY:" or "FROM:" and also created destroyedWhenCapturedFrom which calls destroyedWhenCapturedBy with a "FROM:" prefix. (veqryn)
* Changed unitAttachment toString to be much more informative, and include all values. (veqryn)
* Created new Relationship attachments for canMoveLandUnitsOverOwnedLand and canMoveAirUnitsOverOwnedLand, and set them to validate movement. (veqryn)
* Allowed conditionType for both triggers and conditions (objectives) attachments to have integer values, in addition to other values,

* Allowing html to be used for both triggered notifications and for triggered victory messages. (veqryn)
* Added ability for the defender to capture units if it wins on defense and the attacker brought capturable infrastructure units to the battle. (veqryn)
* Fixing bug in moving defending air to land when a carrier is damaged on defense. (veqryn)
* Fixing bugs surrounding unitsMayNotLandOnCarrier and unitsMayNotLeaveAlliedCarrier interacting with each other. (veqryn)
* Updated whenCombatDamaged to work with unitsMayNotLeaveAlliedCarrier. (veqryn)
* Updated whenCombatDamaged to work with unitsMayNotLandOnCarrier. (veqryn)
* Created new unit attachment ability to have a unit behave differently when damaged, using whenCombatDamaged. (veqryn)
* Adding notes about all properties to Pact of Steel 2 xml, and some code cleanup. (veqryn)
* Updated receivesAbilityWhenWith to work for "canBlitz". (veqryn)
* Created new unit attachment ability to have a unit receive an ability when in the presence or on the same route with another unit, using "receivesAbilityWhenWith". (veqryn)
* Created triggers for changing any attachment that is attached to a territoryEffect by using: territoryEffects, territoryEffectAttachmentName, and territoryEffectProperty. (veqryn)
* Created triggers for changing any attachment that is attached to a relationshipType by using: relationshipTypes, relationshipTypeAttachmentName, and relationshipTypeProperty. (veqryn)
* Created triggers for changing any attachment that is attached to a territory by using: territories, territoryAttachmentName, and territoryProperty. (veqryn)
* Created triggers for changing any attachment that is attached to a unit by using: unitType, unitAttachmentName, and unitProperty. (veqryn)
* Created triggers for changing any attachment that is attached to a player by using: players, playerAttachmentName, and playerProperty. (veqryn)
* Completely re-wrote how raw changes were done, and deleted attachmentToBeChangedName and attachmentToBeChangedProperty. (veqryn)
* Created new ability to set when a trigger fires, with "when", setting "before/after:stepName", that works with all triggers. Triggers still maintain a default step for firing. (veqryn)
* Finished work on making triggers for rules and trigger attachments, using attachmentToBeChangedName and attachmentToBeChangedProperty. (veqryn)
* Preliminary work on making new triggers for rules attachments, and fixing issue with clearing properties without setting. (veqryn)
* Created new triggers for changing player attachments, using players and playerProperty. (veqryn)
* Finished work on allowing triggers to clear data from properties that add rather than overwrite data, by adding "-clear-" to the beginning of the new property, in the triggered change. (veqryn)
* Fixed issue where stats panel and exported stats relied on the first game steps it saw to determine turn order, which meant it considered the order of bids as representative of turn order, instead of looking at things like movement. (veqryn)
* Preliminary work on allowing triggers to clear data from properties that allow multiple sets, in other words, properties that add data rather than overwriting. (veqryn)
* Created new triggers for changing territory properties, using territoryName and territoryProperty. (veqryn)
* Fixed unitProperty trigger change to accept properties with more than one colon. (veqryn)
* Created ability to make conditions and rules attachments that include other conditions in them, and the ability to set the relationship of these conditions to AND, OR, XOR. (veqryn)
* Fixed bug where getCosts in BattleCalculator was only returning the costs for the units that a nation could produce, instead of all units that nation could own. Changed to BattleCalculator.getCostsForTUV (veqryn)
* Fixed bug where TUV in stats panel showed units that had multiple given per production, like NWO's artillery was buy 2 for 7 PUs, incorrectly show on the TUV panel as 7 PUs each. Now it shows up as the rounded up value. (veqryn)
* Updating client game and server model to carry information on alliances and player order. (veqryn)
* Allowed the exporting of stats based on the individual phases in a players turn. (veqryn)
* Updating local player selection screen to show players in turn order, assuming xml was done properly, and to show their alliances. (veqryn)
* Updating 'Export Game Stats...' to give more general information about the game. (veqryn)
* Fixing bug where newly created battles now included duplicates of any units that were strategically bombing a territory. (veqryn)
* Allowed for units that were in territories suddenly made hostile by a change in politics to create battles in those territories. (veqryn)
* Fixed remaining unit tests. (veqryn)
* Engine code cleanup. (frigoref)
* Some small fixes for unit tests, and some small abstractions. (frigoref & veqryn)
* Changed combat filters to allow infrastructure with support or combat abilities to take part in combat. (veqryn)
* Fixing some unit tests, creating tests for Revised sub bug. (veqryn)
* Fixed casualty selection hang bug, and also abstracted CasualtyDetails. (veqryn)
* Fixing some unit tests. (veqryn & frigoref)
* Updated all test xmls. (veqryn)
* Fixed bug introduced into undoing moves, where undoing a sea placement generated an error. (frigoref)
* Created new trigger ability to add and remove production rules from a production frontier. (veqryn)
* Beginning work on territory effects, and some cleanup in the use of basedelegate. (edwin van der wal, with help from frigoref and veqryn)
* Adding ability to trigger notification messages to the players. (edwin van der wal)
* Some beginning work on Dynamix AI sea transportation methods. (wisconsin)
* Fixing of some matches to use new relationships, and some general code cleanup. (veqryn)
* Various code cleaning. (frigoref)
* Some changes to how politics gets initialized. (edwin van der wal)
* Cleaning up of relationships, have alliances auto-create relationships based on default war or allied, and creation of relationship interpreter class. (frigoref)
* Allowed basic html to be used inside unit tool tips. (veqryn)
* Created new unit attachment, createsResourcesList, which allows units to create resources like PUs and techTokens each turn for their owner. (veqryn)
* Created framework and objects for having individual relationships between players, rather than set alliances and war as the only option. (edwin van der wal, with some help from frigoref and veqryn)
* Created politics delegate, which will eventually be filled with the logic and ui elements to allow players to change their alliances and relationships with other players. (edwin van der wal)
\<delegate name="politics" javaclass="games.strategy.triplea.delegate.PoliticsDelegate" display="Politics"\>* Fixed inability to save games during placement phase. (frigoref)* Added ability to customize tooltips for units, using "tooltips.properties". (edwin van der wal)* Stop caching of production_tabs properties, will now read the file each time purchase screen is displayed. (edwin van der wal)* Small fixes to new production_tabs properties and display. User specified production tabs must include all units possible to be purchased by a player, or else an error will be thrown. (veqryn)* Added ability to customize production tabs for each map, using "production_tabs.properties" and "production_tabs.PlayerName.properties". (edwin van der wal)* Added matches for dependencies and transported by. (veqryn)* Fixed route finder to find better routes for units. Will stop finding sea routes for land units, and land routes for sea units. Will try to avoid enemies, AA guns, and neutrals. (veqryn)* Fixed bugs in canInvadeOnlyFrom. (veqryn)* Created new unit attachment, canInvadeOnlyFrom, which determines if a unit can conduct amphibious assaults or if it has to disembark in noncombat. (edwin van der wal)* Made placements appear as a list, just like moves do, and can now be undone individually. Abstracted undoable moves and placements. (frigoref)\</delegate\>

## Changes for 1.3.2.3

* Fixed bug where casualty selection window was never shown and battles hanged, due to infinite loop inside default casualty sorting process under special conditions. (veqryn)
* Fixed bug where units that had previously died to strat bombing, rockets, or scrambling, were still present in the battle if there was a conventional battle immediately afterwards in that territory. (veqryn)
* Fixed bug in validation of non-combat movement of paratroopers. (veqryn)
* Fixed error where allied air on defending carriers may not shoot at non-sub units under certain conditions. (veqryn)
* Fixed error where after a player got paratroopers, ships no longer had their movement validated correctly. (veqryn)
* Fixed error related to two-hit battleships in middle earth. (veqryn)

## Changes for 1.3.2.2

* Fixed infinite loops in purchasing methods for both Strong AI and Weak AI, for low cost units. (veqryn)
* Fixed null pointer error in Strong AI landing of air units for players with impassible capitals. (veqryn)
* Changed savegame-xml exporter to add occupiedTerrOf to any territory not owned by current owner. (veqryn)
* Fixed bug in validation of air that can't land for mixed allied and owned air attempting to land where there already is a carrier and a new carrier will also be placed. (veqryn)
* Fixed null pointer error in Strong AI sea movement. (veqryn)

## Changes for 1.3.2.1

* Added new button to main screen, "Rule Book...", which will open up the user's default web browser and go to the triplea sf page with our future rulebook. (veqryn [Mark Christopher Duncan])
* Updated "unitProduction" so when used in conjunction with "Damage From Bombing Done To Units Instead Of Territories" it sets the allowed number of units to be produced in that territory, thereby finally un-associating the PU production of a territory from the Unit production of a territory.

* Fixed bug related to territory damage in history panel, as well as a null pointer error for factories on territories with no attachments, and also fixed a bug that was not allowing canProduceUnits units to have same max damage as factory units. (veqryn [Mark Christopher Duncan])
* Added information on number of units being purchased to production panel. Also changed all upgrade/consumes type units to have their names displayed in blue. (veqryn [Mark Christopher Duncan])
* Added tabs option to production panel. (edwin van der wal)
* Fixed bug where upgrades of sea units could be placed same turn as the base unit. (veqryn [Mark Christopher Duncan])
* Fixed bug where air units may not participate in a battle if they had been on an allied carrier that was involved in a battle. (veqryn [Mark Christopher Duncan])
* Fixed bug where units with zero attack that were supportable never got to roll in combat. Also, re-wrote getRolls. (veqryn [Mark Christopher Duncan])
* Balancing fixes for LOTR Middle Earth. (ajmdemen)
* Small fixes to exporter classes. (edwin van der wal & veqryn [Mark Christopher Duncan])
* Balancing fixes for Pact of Steel 2\. (veqryn [Mark Christopher Duncan])
* Fixed issue with carriers that are also transports not allowing their land units to participate in battle when the sea unit has participated in battle. (veqryn [Mark Christopher Duncan])
* Added many new admin features to lobby server and client. (wisconsin)
* Added ability to export a savegame to an xml, thereby allowing in game editing of maps. (edwin van der wal)
* Added new game property, "Neutral Flyover Allowed", which like it says, will allow you to fly over neutrals. (veqryn [Mark Christopher Duncan])
* Fixed bug in movement validation that allowed paths over impassibles and restricted territories to be taken into account for landing zones. (veqryn [Mark Christopher Duncan])
* Fixed bug in movement validation that allowed both combat and noncombat flyover of neutrals. (veqryn [Mark Christopher Duncan])
* Fixed bug in movement validation for paratroopers and mechanized infantry techs when a unit has received bonus movement from an airfield or harbour. (veqryn [Mark Christopher Duncan])
* Several small changes to Middle Earth, Big World v3 rules, and Pact of Steel 2\. (veqryn [Mark Christopher Duncan])
* Fixed to allow old Mac OS X computers to connect to lobby, again. (veqryn [Mark Christopher Duncan])
* Small fix to validation of user data for lobby. (veqryn [Mark Christopher Duncan])
* Fixed bug where allied fighters on carriers were not moving with the carriers under certain situations, like when there was an transport ship in the same sea zone, or a harbour or airfield had modified their movement. (veqryn [Mark Christopher Duncan])

## Changes for 1.3.1.1

* Allowing lobby to parse user data more effectively. (wisconsin & veqryn [Mark Christopher Duncan])
* Fixed major bug in low luck support attachments, where units got up to double the support they were supposed to get. (veqryn [Mark Christopher Duncan])
* Fixed Dynamix settings menu to use java 1.5 compatible coding, instead of java 1.6\. With this change, and the removal of string isEmpty calls, TripleA is once again compatible with java 1.5 and Mac OS computers. (wisconsin)
* Updated then Added "Big World : v3 Rules" game, a mod of the original Big World mostly by Prussia, to triplea. (veqryn [Mark Christopher Duncan])
* Removed String .isEmpty calls, as they are not supported under Java 1.5, also called java 5\. (veqryn [Mark Christopher Duncan])
* Fixed fighters and air disappearing even if you bought a carrier, if there is another turn like china, between yours and the placement of the carrier. (veqryn [Mark Christopher Duncan])
* Fixed paratrooper loading creating multiple copies of units. Fixed bugs for deselection of paratroopers and air. (veqryn [Mark Christopher Duncan])
* Fixed minor bugs, including units having to roll to kill unescorted transports. (veqryn [Mark Christopher Duncan])
* Added more ways to get user info for connecting to the lobby on older max-os / unix machines. (veqryn [Mark Christopher Duncan])
* Got lobby actions to correctly be logged, and fixed bug in banning system. (wisconsin)
* Fixed all issues surrounding connecting to the lobby. (veqryn [Mark Christopher Duncan])
* Updated packaged java JRE to java 6 update 25\. (veqryn [Mark Christopher Duncan])
* Added ability to remove games from the lobby screen. (wisconsin)
* Fixed error for old java versions that were unable to access online lobby. (wisconsin)
* Created new unit attachment, createsUnitsList, which allows automatic creation of units by other units at end of turn. (veqryn [Mark Christopher Duncan])
* Fixed unitAttachment validation to allow factories to have maxDamage. (veqryn [Mark Christopher Duncan])
* Fixed build.xml to work for macRelease. (veqryn [Mark Christopher Duncan])

## Changes for 1.3.1.0

* Fixed "what should bomber bomb" AI error, in all AIs. Also fixed bug in easy ai where it would not place any units if some were bunkers. (veqryn [Mark Christopher Duncan])
* Fixed moore AI and easy AI to use new repairing method when trying to repair unit damage instead of territory damage. (veqryn [Mark Christopher Duncan])
* Some updates for Dynamix AI, and fixed AI bug caused by more than one map was opened per TripleA instance, and Added a Resource Collection Increaser cheat. (wisconsin)
* Finished making repair rules work for both damage done to units and damage done to territories.

* Initial work on making repair rules work for damage done to units. (veqryn [Mark Christopher Duncan])
* Fixed null pointer in moore ai for games which don't have carriers. (veqryn [Mark Christopher Duncan])
* Added method to unit class to find territory unit is in. (veqryn [Mark Christopher Duncan])
* Fixed moore AI and easy AI to not purchase any unit which has consumesUnits. (veqryn [Mark Christopher Duncan])
* Fixed bug in scrambling code where user was not being asked if they want to scramble. (veqryn [Mark Christopher Duncan])
* Fixed infinite loop introduced into original factory owner check. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, canProduceUnits, which allows a unit to produce other units, without being a factory. Therefor we can now have combat factories, flying factories, or aa gun factories, or w/e. (veqryn [Mark Christopher Duncan])
* Added the developer forum and the war club to the lobby help menu. (veqryn [Mark Christopher Duncan])
* Added tool tips for units to battle calculator. (veqryn [Mark Christopher Duncan])
* Fixed null pointer caused by using .getOwner().getData() and a word to anyone else who ever thinks about using this: don't, it causes null pointers if there are any neutrals, since neutral is a null player. (veqryn [Mark Christopher Duncan])
* Created new unit attachment, requiresUnits, which allows units to be placed only when certain units are in the territory. (veqryn [Mark Christopher Duncan])
* Changed it so that Territory production defaults to Zero instead of 2, and that unitProduction gets set to a territory's production, though you can still set unitProduction manually if you set it AFTER you set production. (veqryn [Mark Christopher Duncan])
* Created new unit attachment, consumesUnits, which allows units to be upgraded or placed on top of other units. (veqryn [Mark Christopher Duncan])
* Created new unit attachment, canOnlyBePlacedInTerritoryValuedAtX, which defaults to -1 meaning can be placed anywhere. (veqryn [Mark Christopher Duncan])
* Expanded 'disabled' logic to include airbases, repairsUnits, givesMovement, and combat units. Disabled units will not provide their abilities, like scrambling, movement, or repairing, to other units. Disabled combat units will not participate in combat, and will be destroyed if captured. (veqryn [Mark Christopher Duncan])
* Created the placement logic for canProduceXUnits, which now works properly. (veqryn [Mark Christopher Duncan])
* Fixed display error where units with unit damage were not having their damage amount displayed. Still some bugs though for groups of units. (veqryn [Mark Christopher Duncan])
* Created new unit attachment, canDieFromReachingMaxDamage, which will cause a unit to die if they reach max damage through strat bombing or rockets. (veqryn [Mark Christopher Duncan])
* Fixed bug in triggers that caused unit production damage to be done to a territory if a factory was placed via triggers. (veqryn [Mark Christopher Duncan])
* Allowed rockets to also damage a unit, rather than a territory. Further work on getting unit damage to work and display properly. (veqryn [Mark Christopher Duncan])
* Made disabled units actually work. (veqryn [Mark Christopher Duncan])
* Fixed bugs introduced into Strategic Bombing. (veqryn [Mark Christopher Duncan])
* Created new global property, "Damage From Bombing Done To Units Instead Of Territories", which when ON will have damage be done to units rather than territories, as territory damage was the old way of doing things.

* Created "canProduceXUnits" unit attachment. Set to "-1" if you want to produce the value of the territory the unit is in. Still working on the code for this. (veqryn [Mark Christopher Duncan])
* Removed "isCombatInfrastructure" and "unitDamage" from unit attachments, and also removed m_maxOperationalDamage from TripleAUnits. Unit damage is per unit, not per unit type, so it should never be a unit attachment. (veqryn [Mark Christopher Duncan])
* Stopped both Moore AI and Easy AI from buying any units that have maxBuildRestrictions. (veqryn [Mark Christopher Duncan])
* Added lobby rules web page to list of web pages available from the new help menu in the lobby screen. (veqryn [Mark Christopher Duncan])
* Fixed null pointer in unit drawer. (veqryn [Mark Christopher Duncan])
* Fix for Moore AI, it was choosing to never ever attack neutrals in some situations, even if they blocked the path towards the enemy. (veqryn [Mark Christopher Duncan])
* Abstracting MovePanel class. (frigoref)
* Removing constants that refer to specific units, as we should be using unit attachments instead. Also minor updates to unit attachment's new toString. (veqryn [Mark Christopher Duncan])
* Added "Reset" button to Map Zoom. (veqryn [Mark Christopher Duncan])
* Allowed for more information about units to be displayed as a tool tip on the territory panel. (veqryn [Mark Christopher Duncan])
* Created new toString in unit attachment to only display important information that is different from a default unit with no attachments. (veqryn [Mark Christopher Duncan])
* Allowed for more information about units to be displayed as a tool tip during production screen. Allowed tool tip to be displayed when hovering over unit icon, in addition to small info stats. (veqryn [Mark Christopher Duncan])
* Fixes for various null pointer errors. (veqryn [Mark Christopher Duncan])
* New unit attachment setter, "unitPlacementOnlyAllowedIn", which is the direct inverse of "unitPlacementRestrictions". (veqryn [Mark Christopher Duncan])
* Fixed issue [bug 3294118] where transports drop their ground units in the ocean when they engage in combat. (veqryn [Mark Christopher Duncan])
* Added new global property, "On Entering Units Destroyed Instead Of Captured", which if true allows units normally captured on entering to be destroyed. Does not affect non-combat units, only affects combat units with the canBeCapturedOnEnteringBy attachment. (veqryn [Mark Christopher Duncan])

## Changes for 1.3.0.0

* Added the new username banning system, which will help a lot on the lobby. Like to ban offensive usernames without necessarily banning the player. (wisconsin)
* Another patch for Dynamix AI (wisconsin)
* Added airfield_disabled.png and harbour_disabled.png for all nations (veqryn [Mark Christopher Duncan])
* Flipped all unit graphics. All axis sea and air point left, while allies point right (except russian air points left). All ground units for a country point same direction, left for japan and russia, right for everyone else. Non-combat units and aaGuns do not point any direction, or are same for all nations. (veqryn [Mark Christopher Duncan])
* Fixed Neutrals charge to work properly, without java errors, if the neutral is attacked and there is a battle. Will now display a message in history panel if there is not enough PUs to remove. (veqryn [Mark Christopher Duncan])
* Determine if units are 'disabled' and display a unique icon for them (ComradeKev)
* Initial work on Scrambling aircraft (ComradeKev)
* Fixed bug in StrongAI/MooreAI where it would never attack a player if it lost too much TUV, and the TUV calc thought the enemy had zero TUV. Also fixed bug where it calced for the offensive value of walk in territories, instead of defensive value. (veqryn [Mark Christopher Duncan])
* Added a global property, "Capture Units On Entering Territory", which if true allows units to be captured instead of fighting. (veqryn [Mark Christopher Duncan])
* Added new player attachment, captureUnitOnEnteringBy, which will allow this player to let some of the units be captured when a territory is taken over. (veqryn [Mark Christopher Duncan])
* Added new territory attachment, captureUnitOnEnteringBy, which will allow units in the territory to be taken when the territory is captured. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, canBeCapturedOnEnteringBy, which will allow a unit to be taken when the territory is captured. (veqryn [Mark Christopher Duncan])
* Changed Strategic Bombing to account for isSuicide units. Now isSuicide units will also die if they strategic bomb something. (veqryn [Mark Christopher Duncan])
* Fixed error unit display of unit graphics, where things that were \_hit needed \_it on the end instead of front, sometimes resulting in needing \_it_hit_it, etc. (veqryn [Mark Christopher Duncan])
* Fixed null pointer in game data getNeighbors match. (veqryn [Mark Christopher Duncan])
* Updating default maps to use latest properties. (veqryn [Mark Christopher Duncan])
* Rewrote entire RulesAttachment.java so that territory conditions could use "count" with options like "original", "controlled", etc. (veqryn [Mark Christopher Duncan])
* Added new rule property option, "map", for use with Presence and Exclusion conditions. If used, it will return the entire map's territories. (veqryn [Mark Christopher Duncan])
* Made it so that jet power technology and super subs technology no longer affect units with zero attack and zero defense. (veqryn [Mark Christopher Duncan])
* Completely re-wrote checkUnitExclusions and Made unitPresence work with directExcludedTerritories, alliedExclusionTerritories, enemyExclusionTerritories, enemySurfaceExclusionTerritories. (veqryn [Mark Christopher Duncan])
* Added new rule property and condition/objective, "directExcludedTerritories", which applies to the attached player. (veqryn [Mark Christopher Duncan])
* Added new rule property and condition/objective, "unitPresence", as well as "directPresenceTerritories", "alliedPresenceTerritories", and "enemyPresenceTerritories".

* Added new trigger option, "conditionType", which can be set to AND, OR, XOR. This option defines the relationship conditions in a trigger must have, when there is more than 1 condition in the trigger. (veqryn [Mark Christopher Duncan])
* Fixed bug in triggers where an inverted trigger would activate when it should not, when one condition was false but another true. (veqryn [Mark Christopher Duncan])
* Added the ability for any construction of type ending in "structure" not to be changed by setting global values for unlimited/more constructions. Also fixed issue with submarine suicide units able to attack aircraft. (veqryn [Mark Christopher Duncan])
* Updating UnitImageFactory to not rely on hardcoded unit names. Now any unit with isAA unit attachment will require \_r and \_rockets and \_rockets_r IF you have those technologies. Same applied for new aa gun rules and factories. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, isRocket, which will turn the unit into a rocket when the player has the rocket technology, without the unit being an AA gun.

* Added new unit attachment, isAAmovement, which when true the unit will follow the rules specified for movement of an AA gun, even if it is not an AA gun, or is a special kind of AA gun. (veqryn [Mark Christopher Duncan])
* Fixed issue where battle calc calls with AA units was generating divide by zero. (veqryn [Mark Christopher Duncan])
* Fixed bug where battles never ended between units with zero attack/defense power. (veqryn [Mark Christopher Duncan])
* Added new menu option during a game, "Roll Dice...", in the "Game" drop down menu. It allows a player to roll as many dice, with any dice sides, that they want, independant from playing the game. (veqryn [Mark Christopher Duncan])
* Added new unit attachments, \<option name="isAAforCombatOnly" value="true"\>and\</option\> \<option name="isAAforBombingThisUnitOnly" value="true"\>, allow units to be AA guns for only certain attack types. (veqryn [Mark Christopher Duncan])\</option\>
* Added new unit attachments, \<option name="attackAAmaxDieSides" value="6"\>and\</option\> \<option name="attackAA" value="1"\>, which allow you to independently set the attack values and max dice sides for AA units. Radar Tech changed to add "1" to the attack values.\</option\>

* Fixed a bug where a player with both Mechanized Infantry and Paratroopers technology could no longer do any mechanized infantry movement because the validator was checking for paratroopers first. (veqryn [Mark Christopher Duncan])
* Created Low Luck for Strategic Bombing and Rockets. New global property, "Low Luck for Bombing and Territory Damage", and new Unit Attachments, bombingMaxDieSides and bombingBonus. Can be used to set different values for strategic bombing and rocket attacks, separate from the rest of the game. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, \<option name="givesMovement" value="1:fighter"\>, and global property, "Units May Give Bonus Movement", which allow units to give movement to other units. (veqryn [Mark Christopher Duncan])\</option\>
* Fixed edit mode to allow changing ownership of sea territories, so long as it is not un-owned. (veqryn [Mark Christopher Duncan])
* Fixed convoy zone movement validation, and created new global property to manage it: "Naval Units May Not NonCombat Move Into Controlled Sea Zones". Previously was disallowing moves into convoy zones during non-combat, and was marking transported land units as having been in battle. (veqryn [Mark Christopher Duncan])
* Updates to Pact of Steel 2, so that Japanese make use of isKamikaze and isSuicide. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, isKamikaze, which will allow an air unit to use up all of its movement to go to a battle, if it wants to. (veqryn [Mark Christopher Duncan])
* Fix for bug 3052260, Ww2v2 revised subs should now roll dice correctly, instead of dying prematurely in cases where the enemy has a destroyer. (veqryn [Mark Christopher Duncan])
* Fixed suicide units combat to take into account subs and destroyers. Follows relatively simple rules compared with normal combat. (veqryn [Mark Christopher Duncan])
* Created new global property, "Defending Suicide and Munition Units Do Not Fire", which when true will stop defending suicide units from acting like suicide units: dying first round, shooting before everyone else.

* Fixed various matches and places in the code to do with non-combat units, so that they will now also include isInfrastructure. (veqryn [Mark Christopher Duncan])
* Finished work on isSuicide, and also created new game property, "Suicide and Munition Casualties Restricted", which stops casualties from returning fire if true.

* Beginning work on unit attachment "isSuicide", which will allow a unit to die at the beginning of combat. (veqryn [Mark Christopher Duncan])
* Changed "isInfrastructure" to NOT be bombable. Made it so that "canBeDamaged" is now the switch to make something bombable. (veqryn [Mark Christopher Duncan])
* Changed "isInfrastructure" to be captured when taken. isInfrastructure will now be used in place of the planned 'isNonCombat'. (veqryn [Mark Christopher Duncan])
* Added new unit attachment, destroyedWhenCapturedBy, which is a list of players who would destroy a unit rather than capture it. New global property to activate it, "Units Can Be Destroyed Instead Of Captured". (veqryn [Mark Christopher Duncan])
* Added new unit attachment, maxBuiltPerPlayer, which limits the number of a unittype that can be built for each player. (veqryn [Mark Christopher Duncan])
* Added history entries for many triggers. (veqryn [Mark Christopher Duncan])
* Updated ui and utilities to allow islands to be selectable if they are inside a sea zone that ends or begins with "Sea Zone". Previously only allowed water territories to end with, not begin with "Sea Zone". (veqryn [Mark Christopher Duncan])
* Updated giveUnits and takeUnits to not throw Java errors for older maps. Not backwards compatible, just ignore it if true or false. (veqryn [Mark Christopher Duncan])
* Dice change: now allows max dice sides to be set in the xml, \<dicesides value="6"\>. Defaults to 6 if not present. Can be any number between 1 and 200\. This will allow many new types of games to be made. (veqryn [Mark Christopher Duncan] and gansito)\</dicesides\>
* Bug fix in Trigger Attachments Tech change, was disqualifying techs based on attached player instead of aPlayer. (veqryn [Mark Christopher Duncan])
* Redid canBeGivenByTerritoryTo unit attachment to be a colon delimited list of players, who are the players this unit can be given to. Also added a missing toString. (veqryn [Mark Christopher Duncan])
* Completely redid giveUnitControl to be flexible. giveUnitControl and changeUnitOwners are now lists of players to give to, and a new unit attachment, canBeGivenByTerritory, and a new global property, "Give Units By Territory".

* New game property, "Triggered Victory", and new trigger option, "victory" value = victory message. Can be based on any condition. (veqryn [Mark Christopher Duncan])
* Dynamix AI patch, various small improvements and logic fixes. (wisconsin)
* New game property, "Low Luck for Technology", which will apply low luck rules to rolling for tech. (veqryn [Mark Christopher Duncan])
* Dynamix AI logging patch, should make logs easier to read. (wisconsin)
* Completely re-wrote NoPuDelegate, and re-wrote the Rules Attachment for productionPerXTerritories. Now looks like: \<option name="productionPerXTerritories" value="infantry" count="2"\>, and you can have multiple instances of this. (veqryn [Mark Christopher Duncan])\</option\>
* Small bug fix for Support attachments (squiddaddy), and a bug fix for the new placement logic. (veqryn [Mark Christopher Duncan])
* Dynamix AI patch, adding more features and improving some logic. (wisconsin)
* New Repair options. New unit attachment: \<option name="repairsUnits" value="battleship:bunker"\>will cause the attached unit to repair units in the list. New game properties: "Battleships repair at beginning of round" and "Two HitPoint Units Require Repair Facilities". (veqryn [Mark Christopher Duncan])\</option\>
* Created 2 new autosaves: autosave_round_even and autosave_round_odd, which will autosave at the beginning of each round. Provides only the last 2 rounds in order to keep file spam to a minimum. (veqryn [Mark Christopher Duncan])
* New Carrier-Fighter interleaver for AI casualty selection. Another patch for Dynamix AI. (wisconsin)
* Fixed bug where the NoPuPurchase delegate was calling the normal Purchase delegate if the player had PUs left over, Resulting in the player getting multiple purchase screens. (veqryn [Mark Christopher Duncan])
* New game property, "Unit Placement Restrictions", and new Unit Attachment option, \<option name="unitPlacementRestrictions" value="territory1:territory2"\>, prevent a unit or units from being placed in any given territory. (veqryn [Mark Christopher Duncan])\</option\>
* Beginning work on Unit Placement Restrictions. (veqryn [Mark Christopher Duncan])
* Moore AI's casualty picking fixed to work with all maps, not just ww2vX maps. (veqryn [Mark Christopher Duncan])
* Caching of game data to speed up dynamix ai and multiple battle calcing in one turn. And another patch for Dynamix AI. (wisconsin)
* Added new method for Moore AI to move unused transports back to factories. (wisconsin)
* Fix for Moore AI moving units towards capitals already conquered, and not letting units leave once they get there. (wisconsin)
* Fix for Null Pointer error in Moore AI's factory movement. (veqryn [Mark Christopher Duncan])
* Fix for Null Pointer error in Moore AI's movePlanesHomeNonCom. (veqryn [Mark Christopher Duncan])
* Fix for Moore AI's horrible purchasing of transportable land units, which often resulted in the purchase of no land units. This also fixes the 'moore ai buying too many sea transports' issue. (veqryn [Mark Christopher Duncan])
* Added new method for Moore AI to move landlocked units to coastal territories if amphibious (wisconsin), and fixed the purchasing of Transports to purchase land when needed and transports when needed, hopefully without over-purchasing either. (veqryn [Mark Christopher Duncan])
* Added new option for alliedExclusionTerritories: "controlledNoWater", which will not count water or impassible territories. (veqryn [Mark Christopher Duncan])
* Major patch for Dynamix AI. Updated battle calc to cache sorted casualty lists. (wisconsin)
* Created a map skin for Middle Earth based on the alterate relief tiles. (veqryn [Mark Christopher Duncan])
* Added Middle Earth 12 player map, thanks to original creators: (flanagany & ajmdemen)
* Balancing changes to Napoleonic Empires, removed a connection, added fortress to majorca, removed tower from catalonia, changed two fortresses in candia into chasseurs. (veqryn [Mark Christopher Duncan])
* Fixed battle calc to show correct results in battles where artillery and supportables had same attack power. (veqryn [Mark Christopher Duncan])
* Changed default casualty picker to choose optimal casualties based on artillery and supportability. (veqryn [Mark Christopher Duncan])
* Added relief tiles to Pact of Steel. (conarymor)
* Fixed a bug where Undo-ing the placement of a factory, to a territory that already had a factory, under ww2v3 isSBRAffectsUnitProduction rules, caused max damage to be done to the original factory. (veqryn [Mark Christopher Duncan])
* Completely re-wrote isConstructions to be completely customizable. Factories now count as constructions when being placed, eliminating placement code specifically for factories.

* Some work on completely rewriting isConstructions. (veqryn [Mark Christopher Duncan])
* Another patch for Dynamix AI. (wisconsin)
* Major patch for Dynamix AI, including new settings window to customize in-game certain variables the AI uses. (Wisconsin)
* Fix for serializing and techs java error. (squid daddy)
* Added Napoleonic Empires, a beautiful map created by veqryn [Mark Christopher Duncan] and Lssah. Updated to use triggers and combat transports. (veqryn [Mark Christopher Duncan] & lssah)
* Fix for support/triggers/rules java error. (squid daddy)
* New player attachments, "destroysPUs", which when set for a player means that player destroys their PUs rather than let them be captured. (veqryn [Mark Christopher Duncan])
* New player attachments to deal with multiple capitals, "retainCapitalNumber" and "retainCapitalProduceNumber", which be set to the number of capitals need to lose money and gain/spend it respectively. (veqryn [Mark Christopher Duncan])
* New player rule, "maxPlacePerTerritory", overrides both factory rules and infinite placement. Also fixed a bug in isCombatTransport that stopped the casualty picker from choosing it. (veqryn [Mark Christopher Duncan])
* Fixed bunker placement validation to work properly. No longer able to place infinite units by creative clicking orders. Also fixed a bug that allowed infinite placement. (veqryn [Mark Christopher Duncan])
* Bunker rules allowed by new unit property, isConstruction, and new game properties for it (crystalct), heavily modified and bugs fixed, with updated NWO and POS2\. (veqryn [Mark Christopher Duncan])
* Updating Pact of Steel 2, to take advantage of latest technology list abilities. (veqryn [Mark Christopher Duncan])
* Patch for technology lists, to allow creation of new technologies and renaming of old ones. Allows adding new technologies by trigger. (squid daddy)
* Created two new properties for map.properties, "map.showConvoyNames=true" and "map.useNation_convoyFlags=true". If useNation_convoyFlags is true, the flags folder of a game must have "\<nation_name\>\_convoy.png" for each nation with convoys. Convoy names can be moved in name_place.txt (veqryn [Mark Christopher Duncan])\</nation_name\>
* Increasing Max Memory to 512mb for linux/mac/windows, and to 192mb for the server. (veqryn [Mark Christopher Duncan])
* New Property, "Low Luck for AntiAircraft", will turn on Low Luck only for Anti Aircraft shots. (veqryn [Mark Christopher Duncan])
* Allowed blockade and convoy images to be moved with 2 new txt files: "blockade.txt" and "convoy.txt". Also fixed bug where a convoy zone that was occupied territory displayed the wrong owner, and the bug where a convoy route was displayed as a convoy zone. (veqryn [Mark Christopher Duncan])
* Added images to be displayed for Blockades. Default image is "blockade.png" in the misc folder of a map. (veqryn [Mark Christopher Duncan])
* Added new unit property, "isCombatTransport", which allows a transport to fight, be taken casualty, and not allow enemies to move through it, under ww2v3 rules. (veqryn [Mark Christopher Duncan])
* Added new property, "Multiply PUs", which will multiply all PUs gained or lost during a turn, but not yet multiply costs of units, repairs, or starting PUs. (squid daddy)
* Added Technology Frontiers, and ability to customize which tech is available to which player. (squid daddy)
* Changed Pact of Steel 2 to take advantage of new Tech choosing attachments. (veqryn [Mark Christopher Duncan])
* Added a new About... dialog box to main screen. Shows TripleA, engine version, authors, website, as well as a short how-to-play. (veqryn [Mark Christopher Duncan])
* Added a new AI, Dynamix AI, a scripted AI that seeks to be properly coded and easy to understand, as well as solving all problems in moore ai. (wisconsin)
* Added some flags made by veqryn [Mark Christopher Duncan], and some by Pulicat. Added "airfield" and "harbour" unit images to all nations, thanks to Hepster. (veqryn [Mark Christopher Duncan])
* Created Pact of Steel 2, a mod of pos that runs on ww2v3 rules but with drastic changes. Designed to show off every single feature TripleA has to offer on customizing maps.

* Added Pact Of Steel map to triplea, thanks to makers: TripleElk and others. Also fixed baseTiles, updated to current engine. (tripleelk, veqryn [Mark Christopher Duncan])
* Added New World Order map to triplea, thanks to makers: Sieg, ErnieBommel, and others. Also updated to remove special characters from name and files, and updated to take advantage of Triggers. (sieg & erniebommel, veqryn [Mark Christopher Duncan])
* Deleted unused uncoded game Properties. (veqryn [Mark Christopher Duncan])
* Made "LHTR Carrier production rules" completely over-ride the other 4 carrier-fighter properties, that way it is finaly a single switch toggle for the rules-set. (veqryn [Mark Christopher Duncan])
* Small bug in triggers, production changes were always occuring no matter what, missing brackets. (veqryn [Mark Christopher Duncan])
* Further updates to Trigger Attachments and Support attachments, as well as creating a new property to turn triggers on and off, defaults to false: "Use Triggers". (squid daddy)
* Bug fix in alliedOwnership and directOwnership NatObj's use of original and enemy, was returning a list of territories that did not exist. (veqryn [Mark Christopher Duncan])
* Trigger Attachment and Rules Attachment updates. (squid daddy)
* Added isLandTransport to support moving isInfantry land units using Mechanized Infantry tech, now separated from canBlitz and isMarine. (veqryn [Mark Christopher Duncan])
* Minor Updates to Big World and Great War, updates for bugs in the xml as well as small balancing changes. (veqryn [Mark Christopher Duncan])
* Added Purchases to the Trigger Attachment. (squid daddy)
* Fixed giving technology to be actually random, as previously when the list was smaller than 6, some techs had a higher chance of getting picked than others. (squid daddy)
* Changing LHTR Heavy Bombers with Low Luck to give strength+1 instead of 2*strength for attacks, maxing out at max_dice. (squid daddy)
* Triggered Rule Changes patch added. (squid daddy)
* Lobby Moderator Enhancement patch added. (wisconsin)
* Moore AI fix to Rank Territories, was considering islands as being closer to enemy capitols than other territories with a land route. Also much improved the defense of transports and trasporting locations. (veqryn [Mark Christopher Duncan])
* Moore AI improvement: created a new method so that the AI will attempt to defend the beginning and end of its transport chain. (veqryn [Mark Christopher Duncan])
* Fixed a null pointer errors in Moore AI's rank territories method. (veqryn [Mark Christopher Duncan])
* Combined isTerritoryEnemyAndNotNuetralWater AND isTerritoryEnemyAndNotNeutral INTO isTerritoryEnemyAndNotUnownedWaterOrImpassibleOrRestricted. (veqryn [Mark Christopher Duncan])
* New Territory Attachment, blockadeZone, and Unit Attachment, blockade = value, will allow sea units to blockade territories. (squid daddy)
* national objectives addition of 'uses' and 'atWarPlayers'. Still needs some work on atWar. (squid daddy)
* directOwnershipTerritories National Objective added, ownership by an ally doesn't count. (astabada/franz)
* Enhanced Combat Support attachments. (squid daddy)
* Moore AI purchases tweaking and speeding up. Will no longer consider for purchasing units with zero movement, units with 3 or more attack than defense or defense than attack,

* Null Pointer Exception fix in StrongAI transporting. (veqryn [Mark Christopher Duncan])
* Moore AI fixes for previous update. (veqryn [Mark Christopher Duncan])
* Create new CompositeRouteFinder.java, which will find a route based on 3 territory composite matches. (wisconsin)
* Moore AI fixed several of the reasons why ai can't seem to transport units intelligently or at all. Also made it buy more transports if it needs them. Added new matches and renamed findCertainShips to findTersWithUnitsMatching. (wisconsin)
* Moore AI out of bounds exception fixed in SUtils.removeUnit(). (veqryn [Mark Christopher Duncan])
* Moore AI speed fix, and added combined getNeighbors() to GameMap.java. Moore AI now as additional logging properties, comments, and several methods updated to work much faster. (squidbait)
* New Unit Option: "isAirBase" allows units to scramble to combat (ComradeKev)
* New Unit Option: "maxOperationalDamage" sets max damage to be sustained before unit is disabled (ComradeKev)
* New Unit Option: "maxDamage" sets total max damage for a unit (ComradeKev)
* New Unit Option: "isInfrastructure" infrastructure units can be bombed (ComradeKev)
* New Unit Option: "isCombatInfrastructure" units can be bombed or taken as casualties in regular combat (ComradeKev)
* New Property: "Display Units as Counters" (COUNTERS_DISPLAY), will make stacks out of units up to a certain amount. (Edwin van der Wal)
* Moore AI SUtils fix, findNearest() and distanceToEnemy() completely re-written to be much faster. (squidbait)
* Moore AI and Easy AI repair rules fix, will now repair intelligently, and never under repair at all, or over repair by more than a couple pu's. (veqryn [Mark Christopher Duncan])
* Moore AI fixed a bug in SUtils.distanceToEnemy() so that it will return the minimum distance, rather than the first distance it finds. (squidbait)
* Moore AI will now move factories if they can move them and there is more than 1 in a territory (veqryn [Mark Christopher Duncan]), and some non-combat fixes and logging (squidbait)
* Moore AI will now bid single units to territories, and bid to all it territories before cycling over to bid to the first one again. Starts with territories touching the enemy. Also fixed a bug in SUtils.distanceToEnemy(). (veqryn [Mark Christopher Duncan])
* MustFightBattle was removing all movement from all units (including air) that stopped to kill an undefended transport, and should not remove movement of air units. (veqryn [Mark Christopher Duncan])
* Moore AI and Weak AI fixes, they were not repairing any factories when they had multiple damaged factories. Both will now repair correctly, and limit repairs to half of total PUs, and limit individual factories to a repair of one quarter total PUs. (veqryn [Mark Christopher Duncan])
* Moore AI fixes, will now return immediately if it has nothing to do for moves and purchasing (wisconsin), and will now repair damaged factories correctly (veqryn [Mark Christopher Duncan]).
* Moore AI major fix, was considering defender's attack values instead of defense values under some circumstances. Formula to remove casualty units was returning the list as is without properly sorting first,

* Moore AI major fix, was disqualifying all land units from attacking when those land units did not have artillery, isInfantry, or blitz. Much improved performance on 270BC. (veqryn [Mark Christopher Duncan])
* Moore AI SUtils getExactNeighbors() fix, was returning incorrect data for any distance greater than 2\. (veqryn [Mark Christopher Duncan])
* Moore AI logic fix, calculations for taking enemy capitol with allied help included owned strength when looking at allied strength, also

* Easy AI major fix, was considering all water territories on the map in the list of territories to attack with land units. (veqryn [Mark Christopher Duncan])
* Easy AI will now purchase units for bid, however it will only purchase land units, and only place them in the capitol. (veqryn [Mark Christopher Duncan])
* Easy AI bug fix, was purchasing zero units when it had to repair a factory and also had at least 1 other factory with no repairs. Also fixed AI not using all of its money when it had enough left to buy one more unit. (veqryn [Mark Christopher Duncan])
* Fixed Moore AI not puchasing anything when it has placeanywhere rules and no factories, and fixed it placing everything inside a capitol which is impassable (bug 2965154),

* More work on Moore AI's purchasing and placing. Will now sort territories into a list which represents both production ability and closeness to enemy.

* Added a swap sides button to the battle calculator, corrected a misspelled class, and reduced default calcs from 5000 to 3000 (dav_eagle)
* Moore AI purchase fixes. AI was buying factories then trying to place them in water. When rich it was purchasing only the cheapest unit (bug 2989178),

* Moore AI logic fix, will now attack alone transports correctly, and some small tweaks (veqryn [Mark Christopher Duncan] & wisconsin)
* Moore AI logic fixes, including amphibious attacks, and clearing of data in loops (squidbait)
* Small balancing change to minimap. Russians -6 PUs, Italians +9 PUs. (veqryn [Mark Christopher Duncan])
* MoveValidator fix, was returning true if route contained subs/trans in part of route, and surface warships in another part of route. (squidbait)
* logic bug fix for easy ai: it was checking for the att value for def units in territories to walk into. (veqryn [Mark Christopher Duncan])
* logic bug fix for the weak/easy ai, so that it will not try to move zero movement units. (daral)
* logic bug fix for the moore ai, which tries to move units out of range. (wisconsin)
* Adding a browser launcher utility that works with java 5 and 6\. (veqryn [Mark Christopher Duncan])
* Adding buttons to the map download dialog, as well as the lobby menu, that when clicked open a web browser to the

* Allowing any country name which begins in "AI" to be automatically set to be AI (in addition to "Neutral"). (veqryn [Mark Christopher Duncan])
* Added a few new properties to start to support next gen engine (ComradeKev)
* limit status message length and remove combining characters (sgb [Sean Bridges])
* better server side INode validation (sgb [Sean Bridges])
* fix null pointer when selecting various air transport loads (ComradeKev)
* Added Great War reliefs (Pulicat)
* Updated BigWorld game (veqryn [Mark Christopher Duncan], Uboat, Pulicat, and others)
* fix part of bug 3012752 - unitSupportCount not working (ComradeKev)
* fix bug 3081799 air units capable of landing on land included in carrier landing calculations (ComradeKev)
* add SELECTABLE_ZERO_MOVEMENT_UNITS property support (veqryn [Mark Christopher Duncan])
* fix bug 3043828 pending sea battles with transports causes crash (ComradeKev)
* set attacking units' movement to 0 when they stop to kill undefended units (ComradeKev)
* fix bug 3007142 Carriers that are also transports (ComradeKev)
* fix bug 3028106 fighter landing bug (ComradeKev)
* another fix for 2998846 & 3012752 Kamikaze fighters and unloaded troop edit-removal (ComradeKev)
* fix bug 2998846 kamikaze aircraft not working (ComradeKev)
* add isAirTransport(able) to support air dropping units, now separated from isStrategicBomber (ComradeKev)
* fix bug 2994004 air landing on newly produced carrier in multi-national SZ disappears (ComradeKev)
* feature request (2799840) add tech tokens to status tab (ComradeKev)
* update .ico and .png icons (veqryn [Mark Christopher Duncan])
* feature request add dialog showing results of War Bonds (ComradeKev)
* fixed load of PacificTest.java (ComradeKev)
* fix bug 2987400 remove ww2v2 from isNavalBombardCasualtiesReturnFire calculations (ComradeKev)
* fix bug 2981507 isNeutralsImpassable not considered for air non-combat movement (ComradeKev)
* fix bug 2975757 paratroops walking on water with movement \>1 (ComradeKev)
* fix bug 2986683 add bombard property to control bombarding attack power (ComradeKev)
* feature 2802942 artillery supporting \>1 inf, defaults to 1 (ComradeKev)
* feature 2969513 configurable tech roll cost by player, defaults to 5 (ComradeKev)
* fix bug 2979946 AA Always On only recording last territory casualties (ComradeKev)
* fix bug 2983390 continued battles (subs) not fought when transport bridge used (ComradeKev)
* fix bug 2981407 Can't edit-remove transported units (ComradeKev)
* fix bug 2827064 unload/load trn bug (ComradeKev)
* fix type in battle screen (Bung)
* update cruiser and Italian infantry (veqryn [Mark Christopher Duncan], crystalct)

## Changes for 1.2.5.5 stable

* better server side INode validation (sgb)

## Changes for 1.2.5.4 stable

* ask users to restart after downloading a map as workaround to 2981890 (sgb)
* replace japanese_fade gif with png (veqryn [Mark Christopher Duncan])
* new free french flags (veqryn [Mark Christopher Duncan], crystalct)
* fix bug 2981512 game hangs during purchase units phase with mooreAI (sgb)

## Changes for 1.2.5.3

* fix bug 2979108 Multiplayer LL AA guns Java Error (sgb)

## Changes for 1.2.5.2

* fix bug 2977842 Black sea zone movement bug (sgb)
* fixed bug ConcurrentModificationException (sgb)
* low luck air now works according the to the veqryn [Mark Christopher Duncan] rules (sgb)
* validate zip file on map download (sgb)

## Changes for 1.2.5.1

* fix bug 2973990 repair rules bug plus new lock not held bug (sgb)
* fix bug 2969991 lock not held bug, 1.2.5.0 (sgb)
* fix bug 2970332 low luck aa casualties don't work when movement varies (sgb)
* fix bug 2971204 moore AI out of bounds exception when no transport rules (sgb)
* partial fix for bug (2971193) to-hit of 6 causes dump- need to revisit when moving to Dx (ComradeKev)
* Re-fix bug (2965453) convoy centers/routes with original owners (ComradeKev)

## Changes for 1.2.5

* Re-added Japanese_fade.png flag file for use as kamikaze markers in Pacific (ComradeKev)
* Fix bug (2965453) occupiedTerritoryOf doesn't work with Convoy Centers (ComradeKev)
* Add new isTransportAndNotDestroyer match so DDs that can transport don't fall into normal transport rules (ComradeKev)
* Fix bug(2961038) Can transport armor or more than transportCapacity on bomber with paratroops (ComradeKev)
* fix bug stack overflow in NWO 1.7.7 on Hard AI (sgb)
* updated german, italian and neutral flags (veqryn [Mark Christopher Duncan])
* better packaged windows icon file (veqryn [Mark Christopher Duncan])
* fix bug 2964947, minimap AI error (sgb)
* allow choosing aa casualty option to work with low luck (sgb)
* fix crash where unloading attacking transports to allied nations when a defending transport was present and the allied transport dies in the battle (sgb)
* fix crash with unloading units to multiple allied territories and multiple transports die (sgb)
* fix low luck aa casualty selection when different plane types are present (sgb)

## Changes for 1.2.4

* fix bug (2960696) Strategic Bombing Crash in 1.2.3.0 (sgb)
* fix bug 2961673 crash in strong ai (sgb)
* fix bug 2943370, lock not held (sgb)
* fix exception with casualty selection in low luck (sgb)
* fix bug in strong ai when there are no transport production rules (sgb)
* fix null pointer in strong ai (sgb)

## Changes for 1.2.3

* fix downloaded map skins (sgb)
* Add default AI setting for 'Neutral' players in remote games (ComradeKev)
* remove nwo map in default install, this allows it to be updated independently (sgb)
* update xml for big world,great war, update misc images for great war, update flags for great war, update italian cruiser image, update chineese and american aa gun,

* add optional version number to map listing xml file. This version number will be saved when the game is downloaded. When the user is asked to delete

* Tweaked version error message and aircraft landing on CV validation (ComradeKev)
* Patch bug () Dump in EasyAI non-combat movement (ComradeKev)
* Patch bug (2953997) Dump in StrongAI non-combat movement (ComradeKev)
* Fix bug (2955224) Low Luck casualties not being taken (ComradeKev)
* Fix bug (2951839) reporting that non-blitzed neutrals are charging fee, causing dumps (ComradeKev)
* Fix bug (2951882) amphib units being ignored (ComradeKev)
* increase max java memory to 256m (sgb)
* new icon for triplea.exe (ubernaut)

## Changes for 1.2.2

* update flag images in the base flags folder (u-boat,veqryn [Mark Christopher Duncan])
* allow flag images to be gif or png, gif's will be preferred if both are available to prevent new images in the base folder from overriding images in mods (sgb)
* Fix null pointer in new AA dice rolling code (ComradeKev)
* Add default AI setting for 'Neutral' players (ComradeKev)
* Fix bug related to paratroops and blitzing tank movement (ComradeKev)
* Fix bug (2947241) combined land/amphib blitz with associated sea battle throws exception (ComradeKev)
* Add additional unit png files to most base/images/units folders (ComradeKev)
* Fix bug (2945150) 'Neutrals Are Impassable' only valid for aircraft (ComradeKev)
* Fix bug (2943002) AA firing rules with and without low luck (ComradeKev)
* Fix bug (294300) Victory Conditions tweaked (ComradeKev)
* Check 'Allied Air Dependents' property to see if allied air can participate in attack (ComradeKev)
* Fix bug (2936271) Bombers allowed to continue to more battles after dropping (blitzing) paratroops (ComradeKev)
* Fix bug (2939602) Allied fighters on attacking carriers (ComradeKev)
* Fix bug (2939915) by tweaking route finding logic (ComradeKev)
* Fix bug (2938275) AA on trns firing at passing aircraft (ComradeKev)
* Change 'No Economic Victory' game property to 'Economic Victory' (ComradeKev)
* Fix displayed Victory City victory message (ComradeKev)
* Fix null pointer if trying to select factory in edit mode (ComradeKev)
* Update NWO map to version 1.7.2 (OnanTheBrBr)
* Fix bug (2933998) null pointer in MoreNAble IA Non Combat movement through sea zones (ComradeKev)
* Fix bug (2933797) Battle Calc in Edit Mode- removed unnecessary checks for edit mode (ComradeKev)
* Allow submersible subs to travel under enemy ships in combat and non-combat (except DDs) (ComradeKev)
* Update options panel height to 15 items to fit on smaller screens (ComradeKev)
* Fix bug (2933341) Exception if paratroop transport cost \> bomber capacity (ComradeKev)
* Fix bug (2932947) paratroop checking code allowing naval ships to move through enemy SZ (ComradeKev)

## Changes for 1.2.1

* Update game icons (ubernaut)
* Fix subs being able to move through enemy fleets in noncombat for WW2v2 (ComradeKev)
* Fix broken code around pacific test cases for new properties (ComradeKev)
* Remove the hardcoded productionRules for non-sea units during Shipyard initialization (ComradeKev)
* Fix bug 2925146 options panel overflows screen in a single column (ComradeKev)
* Fix GameParser to correctly read optional flag for players in the xml playerList (ComradeKev)
* Fix bug 2926226 fighter movement with owned carriers (ComradeKev)
* Update NWO xml to use the new figher/carrier properties (ComradeKev)
* Break up Fighter/Carrier production rules into atomic components and added several new game properties for them (ComradeKev)

* Add game property support for configurable Victory City thresholds 'xxx Total Victory VCs', 'xxx Honorable Victory VCs', & 'xxx Projection of Power VCs' with xxx being alliance name (ComradeKev)
* Add support for game property to define economic victory conditions in the form of 'xxx Victory' with xxx being alliance name (ComradeKev)
* Abstract victory conditions to read teams/players from XML rather than hardcoded values (ComradeKev)
* Add negateDominatingFirstRoundAttack option for RulesAttachment- negates dominatingFirstRoundAttack for player (ComradeKev)
* Add dominatingFirstRoundAttack option for RulesAttachment- defenders roll at 1 (ComradeKev)
* Add placementInCapitalRestricted option for RulesAttachment- restricts unit placement to capital (ComradeKev)
* Add unlimitedProduction option for RulesAttachment- bypasses limitation of unit placement to factory production (ComradeKev)
* Add 'Neutrals Are Blitzable' property with value of TRUE to NWO (ComradeKev)
* Fix bug 2919694 non blitzing units allowed to incrementally make 2nd move (ComradeKev)
* Fix bug (partial) 2860602 Allied air on carriers group together when carriers move through one another (ComradeKev)
* Fix bug 2922798 transports with mechanized infantry aboard can move 3 spaces (ComradeKev)
* Fix bug 2921117 can't blitz neutrals- added Neutrals Are Blitzable property (ComradeKev)
* rename nwo map to new_world_order_eb, this is all lowercase which works on linux, and matches the other map names (sgb)
* rounded neutral flags (veqryn [Mark Christopher Duncan])
* Fix bug 2919513 units with 0 attack not getting artillery support (ComradeKev)

## Changes for 1.2

* Fix display of factory damage when unit name is "Factory" rather than "factory" (ComradeKev)
* Add more test cases (ComradeKev)
* update to Great War 3.0 (Jason Clark)
* Fix bug 2915452 Shouldn't be able to blitz with non-blitzing units by incrementally moving (ComradeKev)
* Fix bug 2915057 Bombers shouldn't be able to move then pick up paratroops (ComradeKev)

## Changes for 1.1.2

* Add more test cases (ComradeKev)
* Upgrade NWO to NWO EB (OnanTheBrBr)
* Fix bug 2909898 2-move units allowed to move 'through' enemy forces (ComradeKev)
* Fix test cases for LHTR rules revisions below (ComradeKev)
* Fix bug 2905542 LHTR HB not adding +1 to SBR rolls (ComradeKev)
* Fix bug 2908897 occupiedTerrOf not working when liberating allied capital (ComradeKev)
* fix null pointer in move with Twilight Imperium (sgb)
* Create/use Properties for various entries in Constants for consistency (ComradeKev)
* Fix invalid property used in isTransportUnloadRestricted of TransportTracker (ComradeKev)
* Fix bug 2907042 Revised submerged subs don't fight in subsequent defending battles (ComradeKev)
* increase download map panel size (sgb)
* if a url in the download games xml starts with !, ignore it and disable download button. this allows better formatting (sgb)
* game engine prevents ai from repairing a territory more than the number of times it was hit (sgb)
* fix bug 2899005, Long air range icon works only with "fighter" and "bomber" (sgb)
* fix bug 2905298, Wrong message Cant place sea unit on land (sgb)
* fix bug 2905986, occupiedTerrOf don't work with capital (sgb)
* skins can be downloaded/read from the users map folder (sgb)

## Changes for 1.1.1

* new neutral flag images (veqryn [Mark Christopher Duncan])
* allow users the option to replace downloaded maps when downloading (sgb)
* don't allow downloading a map with the same name as one that comes with the default TripleA install (sgb)
* fix bug 2893890, fighters with no movement left can hover in sea zones where carriers can be placed (sgb)
* fix bug 2887488, Add "Display Sea Names" property to display sea zone names (ComradeKev)
* Add 'Multiple AA Per Territory' property (ComradeKev)
* Fix nonCombat movement into enemy SZ 2 zones away (ComradeKev)
* Remove Economic Victory from NWO, Great War, and Big World (ComradeKev)
* Add French Rocket to NWO units (ComradeKev)
* Fix WW2V3_Tech_Model constant (ComradeKev)
* Fix buyCruiserIndustrialTechnology unit for Big_World (ComradeKev)
* Various map utility fixes (Stephen Wicklund)
* Right clicking on center picker removes the dot (Stephen Wicklund)
* Center picker displays the name of the center next to the dot (Stephen Wicklund)
* Fix bug in getStrengthOfPotentialAttackers for planes. Reduced frequency of tech purchase. (Kevin Moore)
* fix bug 2831083, WW2V3: Retreat from undefended transports (sgb)
* fix bug 2892836, aa radar in low luck (sgb)
* fix bug 2893144, null pointer on startup (sgb)
* fix bug 2898135, where unloaded infantry could move as mechanized infantry (sgb)
* various paratrooper fixes (sgb)
* fix bug 2892469, paratroops in first enemy territory (sgb)
* StrongAi, Cleaned out unused code. Minor tweak to getStrengthOfPotentialAttackers. (Kevin Moore)
* Fix bug in zip url parsing (Stephen Gallagher)
* StrongAi, Fix bug in ship movement. Modify territory selection for non-combat transports (Kevin Moore)
* fix bug where paratroops could walk on water, bug 2867358 (sgb)
* remove isParatroop UnitAttachmant property. (sgb)
* fix Allied fighter on AC bug, bug 2890919 (sgb)
* fix infinite loop in odds calculator, bug 2853353 (sgb)
* better logic for determining which odds calculator player should be used if no units are in the territory (sgb)
* better isolation of units in odd calculator from units in the game (bug 2820761) (sgb)
* download file notes shows top of notes by default now, rather than scrolling to the middle (sgb)

## Changes for 1.1.0

* update StrongAI files for PUs (ComradeKev)
* update to substance 5.3 (sgb)
* remove troublesome maps (sgb)
* Add code to allow downloading and installing games from the network. An Exampe site is here,

* add utility for updating game.xml files (sgb)
* Strong AI Changes (Kevin Moore)

* Scrub Production Units (PUs)(ComradeKev)
* Fix bug 2827014 Air forces route through impassables if length = valid sea route (ComradeKev)
* Fix bug 2829876 BB bombards when only air attacking from SZ (ComradeKev)
* Fix bug 2827394 renamed Neutral.GIF to Neutral.gif (ComradeKev)
* Fix bug 2820547 faulty mechanized inf and paratroop capacity (ComradeKev)
* Scrub xml and source (ComradeKev)
* fix bug 2818614 include substance jar in build.xml (Seidelin)
* fix bug 2818578 partial amphib attack with air asked to retreat twice (Seidelin)
* fix bug 2820382 Undoing/redoing amphibious attack can allow too many bombard (Seidelin)
* Don't allow aa guns in blitzed territories to fire rockets (sgb)
* Improved land and sea unit purchasing. Changed parameters on factory purchase. Extensively modified ship handling in combat and non-combat. Modified battle prediction to improve land unit attack. (Kevin Moore)
* fix bug 2818023 again moving unit to carried-over battle causes existing units to be ignored (ComradeKev)
* new flag images for Italy and Russia (U-Boat)
* fix partially repaired factories showing as completely repaired (ComradeKev)
* Changed testCanRetreatIntoBlitzedTerritory() to allow retreat into blitzed territory (ComradeKev)
* fix bugs 2815448 defending subs not getting sneak attack (Seidelin)
* fix bug 2813511 naval units not asked to retreat (Seidelin)
* fix bug 2807885 fighters asked which transport to load (Seidelin)
* Partial refactor of validateAirCanLand (ComradeKev)
* add isInfantry marker to infantry units for all mods (sgb)
* fix bug where strat bombers hit by aa en route to a battle lives (sgb)
* fix bug 2816632 Marine unit doesn't work with LL (sgb)
* fix bug 1888062 multinational transport bug (sgb)
* remove non working "Use Destroyers and Artillery" in Iron Blitz (sgb)
* fix bug 2815448, Defending subs don't get sneak defense (sgb)
* fix bug 2803021, NWO PUs to spend don't display (sgb)
* move copies of blank_relief to images/relief tiles, this allows all maps to share a copy (sgb)
* change labels/dialog on repair screen to make it clear we are not purchasing units (sgb)
* fix bug 2802962, bug where units loaded onto transports in a pending battle zone do not die when their transports do (sgb)
* fix bug 2807875, Factories count towards production limit (sgb)
* fix bug 2815801 Bid placement Error (sgb)
* Complete gutting of NonCombatMoveSea; Removed most plane analysis code and replaced with calls to invitePlaneAttack in SUtils;

* Add some missing units for NWO and activate tech for extra 4 players in NWO-9 (ComradeKev)
* Check if SBR damages unit production before displaying factory damage (ComradeKev)
* Fix bug 2801738 just use Infantry instead of chineseInfantry so they stack properly (ComradeKev)
* Add victory conditions to game notes (ComradeKev)
* Add NOs to game notes for AA50 (ComradeKev)
* Fix bug 2807397 Revise NWO 9 Player placements for E/W Romania (ComradeKev)
* Fix number of paratroops shown loading on to bomber (ComradeKev)
* Change default route finding to try land routes first (ComradeKev)
* Fix allMatch and someMatch returning true on empty collections (ComradeKev)
* Add victory conditions to game notes (ComradeKev)
* Enable turning on/off relief tiles on AA50 (ComradeKev)
* Add Relief Tiles for AA50 (Much thanks to Imperious Leader)
* Fix bug 281534 fighter movement calculation (ComradeKev)
* Moved capitol markers to better fit with AA50 reliefs (BraveHamster)
* Fix bug 2810759 Non-amphib units taken as casualties before amphib units (Seidelin)
* Fix bug 2807878 Planes attacking w/ amphib units can't retreat (Seidelin)
* Strong AI fix bid purchasing and put in code for blitzing empty territories (Kevin Moore)
* show line/column of xml errors when a game fails to parse (sgb)
* Modify AI: Apply purchasing changes to sea units (Kevin Moore)
* Show user ip/port lobby server tries to connect to when hosting a game fails because the computer is not reachable from the lobby server (sgb)
* Modified AI: purchasing for seaLion, improved blitzing, tweaked combat and non-combat to better protect capitals and factories, add comments in SUtils (Kevin Moore)
* fix bug 2808834 online games suddenly fail (sgb)
* fix bug 2806095, missing files in mac build (sgb)
* Add some test cases
* Fix bug 2459410 Fighters on carriers with allied fighters can't attack (ComradeKev)
* Fix bug 2807115 Air improperly calculating max distance with existing carriers (ComradeKev)
* Fix exceptions when undoing a paratroop attack move (ComradeKev)
* Fix aircraft being able to fly too far when building carriers (ComradeKev)
* Fix bug 2806723 ships allowed to move through enemy navies during combat move (ComradeKev)
* Fixed stopping in zone with ignored units causes movement to end (ComradeKev)
* Added AA50 Technology Tree to game notes (ComradeKev)
* Check defending units for attack power before popping kamikaze message (ComradeKev)
* Add method to land paratroops (remove dependence on bombers) (ComradeKev)
* Fix 1 AA hit kills all paratroops (ComradeKev)
* Fix paratroops refusing to fight (ComradeKev)

## Changes for 1.0.3.4

* Better internet ip detection (sgb)
* Fix bug where a territory could not be strategic bombed and conquered in the same turn (sgb)
* Fix bug 2804677 Retreating into enemy spaces (sgb)
* Add menu to change look and feel (sgb)
* Fix bug 2799810 Admin right-click menu (sgb)
* Fig bug 2801742 Rockets throw error in NWO (sgb)
* Fix bug 2801740 java error in every roll in a PBEM game. (sgb)
* Fixed not being able to place bid units at non-factories (ComradeKev)
* Fix bug 2675636 Crash when ignoring enemy units (ComradeKev)
* Fix bug 2779955 Cause battle when new/ignored units are in contested zones (ComradeKev)
* Minor change to the Strong AI calculation of the strength of sea units near a territory (Kevin Moore)
* Fixed the connections or E/W Romania in NWO9 (ComradeKev)
* Added name_place.txt for NWO (ComradeKev)
* Updated rockets.png for Russians in NWO (ComradeKev)
* Fixed some connections in Europe.xml (ComradeKev)
* Added name_place.txt for Europe (ComradeKev)
* Fixed neutrals not able to be captured after a failed attempt (ComradeKev)

## Changes for 1.0.3.3

* put game name in window title (sgb)
* fix bug 2753571 - Unloaded cargo not being removed when transport sinks, also odds calculator fails with transports in revised (sgb, gruetzdark)
* fix bug 2779959 - Stay in the Mobilization Zone (sgb)
* fail when loading game where xml case and file name case differs (sgb)
* fix map name/unit case in nwo maps (sgb)
* mark territories with battles (sgb)
* Make it so map utility programs can find the centers, polygons, and map.properties files by using the

* Make it so the user can specify the unit's scale when using the 'Auto Placement Finder' utility.(Stephen Wicklund)
* add a setting to "Lock" the map, so you can observe a game without the map moving all around (Stephen Wicklund)
* add a setting to suppress the showing of battles between two AIs (Stephen Wicklund)
* add a setting to choose how long the AI pauses between each movement (Stephen Wicklund)
* add a better ai (Kevin Moore)
* limit number of units in one row of production panel to 8 (sgb)
* The following list of bugs were fixed- (Comradekev)

## Changes for 1.0.3.2

* The following list of bugs were fixed- (Comradekev unless otherwise specified)

## Changes for 1.0.3.1

* update docs to correct how to run TripleA from the command line using the ant run command.
* The following list of bugs were fixed- (Comradekev)

* Fix for tech tokens (Seidelin)
* Add ShowMapOnly mode for passively viewing games (Smutt)
* Added 'Neutrals Are Impassable' property to eliminate neutrals from pathfinding (ComradeKev)
* on windows, put saved games in users home folder, rather than the triplea install directory. this works better on Vista. (sgb)
* fix [ 1945380 ] battle calculator window buttons lost (sgb)
* update launch4j generated exes to use launch4j 3.0.1 (sgb)
* updated embedded jre to 6_11 (sgb)

## Changes for 1.0.3.0

* Disable game properties button if there are no game properties (Chris McIntosh)
* Fix spelling in classic xml (Chris McIntosh)
* The following list of bugs were fixed- (Comradekev)

* 2006022 Undo movement jumps back to top of list (Chris McIntosh)
* 1910223 Ability to cancel odds calculator (Chris McIntosh)

## Changes for 1.0.2.0

* Maps images, and XML for AA50 (Zero Pilot and Black Elk)
* Update game notes (sgb)
* Better error message if no server properties for this version (sgb)
* Mods can now be installed without unzipping anything. Simply create a zip file with contents that look like any of the folder in maps. (sgb)
* Add new Game chooser dialog that shows games notes. (sgb)
* Move xml files from games folder to /maps/\<mapname\>/games. For example, revised.xml is now in maps/revised/games (sgb)\</mapname\>
* Add chat ignore feature, thanks to Tango for the icon - [http://tango.freedesktop.org/Tango_Icon_Library](http://tango.freedesktop.org/Tango_Icon_Library) (sgb)
* Add full TripleA 50 support (ComradeKev)

* Add Choose AA Casualties property (value=true) to Revised.xml (President Douchebag)
* Break up rulesets into individual rules (while keeping overall ruleset setting) (ComradeKev)

## Changes for 1.0.1.4

* Add blank_relief.png to various maps to fix exceptions and fix misspellings in POS \*.txt files (ComradeKev)
* Fix bug [ 2153973 ] BattleCalc during EDIT hangs the game (ComradeKev)
* Fix bug [ 1228661 ] Fighters can't move to combat unless carrier moves in range (ComradeKev)
* Fix bug [ 1951595 ] edit mode, fgt and inf placement in sz (ComradeKev)
* Tweak blending code to account for missing base/relief tiles (ComradeKev)

## Changes for 1.0.1.3

* When executing sql in headless lobby, show error messages on the console (sgb)
* Update Great War map to remove small country markers (Jason Clark)
* Add Revised relief tiles (Zero Pilot)
* Update Revised colors (President Douchebag)
* Set max memory for mac release (sgb)
* Fix abend when there are no original owners in a territory (ComradeKev)
* Change so only original owner gets the faded kamikazi zone marker (ComradeKev)
* Fix display of Convoy Route text (ComradeKev)
* Fix PlacementPicker abends (ComradeKev)
* Fix Null Pointer [ 1068223 ] for non-required files in AutoPlacementFinder app (ComradeKev)
* Fix bug [ 1937303 ] casualty window shows all casualties as defending nation (ComradeKev)
* Fix bug [ 2066114 ] Industrial Tech advancement crashes stats tab (President Douchebag)
* Add code to identify offending territory in AutoPlacementFinder exceptions for centers.txt (ComradeKev)
* Add code to allow Relief Map Blending (Overlay, Linear_Light, Multiply, Difference) via map.properties settings includes 3 parameters (ComradeKev)

## Changes for 1.0.1.2

* Fix territory connections in Pacific
* Fix bug where hasLandRouteToEnemyOwnedCapitol causes abend for players with no Capital. Returns none for 'optional' players
* Re-create code to change ownership of units so British/Australians can play on same turn in pacific
* Fix thrown exception with neutral blitz/flyover. (Comradekev)
* Fix bug [ 2005292 ] LHTR planes not able to land on produced carriers. (ComradeKev)
* Add ability to manually select AA casualties via "Choose AA Casualties" game property. (President Douchebag)
* Fix bugs [ 1668008 & 1683940 ] Fighter ability to move one space to land when CV is sunk (ComradeKev)
* Fix territory connections in Pacific (ComradeKev)
* Fix bug [ 1809209 ] transport retreat/die after unload leaves unloaded units in place (ComradeKev)
* Change BattleStepStrings names to match text for clarity (ComradeKev)
* fix null pointer that leads to potential lobby crash (sgb)
* update great war map (Jason Clark)

## Changes for 1.0.1.1

* Replace code for using the Large flags for Capital markers and tweak their placements in Pacific (ComradeKev)
* Fix abend when capturing Commonwealth Convoy Center (player with no capital) (ComradeKev)
* allow lobby server to run in headless mode (sgb)
* fix lobby.properties. If a lobby.properties file is in the root TripleA directory, use that to connect to the lobby (sgb)
* reduce lobby backup frequency to 7 days (sgb)

## Changes for 1.0.1.0

* Fix bug [ 1830015 ] transport load/unload after being in combat (ComradeKev)
* Add Convoy Centers & Convoy Routes, as well as labels (ComradeKev)
* Add Tokyo Express - Ability for DDs to carry one inf in Pacific (ComradeKev)
* Fix amphib marines combat display (ComradeKev)
* Add name_place.txt for pacific to clean up territory name placement (ComradeKev)
* Add Australian player purchases (units transferred to British control for combined play after buy) (ComradeKev)
* Add Australian capital and territories (ComradeKev)
* Add partial support for Commonwealth Convoy Center cash distribution (ComradeKev)
* Add Naval and Air bases (ComradeKev)
* Add partial support for Kamikazi zones (ComradeKev)
* Fix lhtr strategic bombing (dav eagle2)
* fix [ 2015235 ] Compilation error under OpenJDK (karrde712)

## Changes for 1.0.0.3

* allow factories with non 0 movement to move (sgb)
* update great war to 2.2 (Jason Clark)

## Changes for 1.0.0.2

* Fix dice click problem, reopen bug [ 1673719 ] right-click-drag should not deselect unit upon release (sgb)
* Fix bug where selecting unit and transports and moving to a sea zone may move a transported unit more than once (sgb)
* Fix bug [1988219] lhtr fighters cant land on new carriers (sgb)

## Changes for 1.0

* add tdice dice servers (sgb)
* lock warnings don't show error dialog (sgb)
* fix bug [ 1962058 ] fighter move in non combat (sgb)
* allow selection of text on chat panel (sgb)
* remove non existent irony dice server (sgb)

## Changes for 0.9.4.2

* in edit mode, don't always ask the user to choose the units to remove (sgb)
* add game id, to be used in future pbem server (sgb)
* remove uneeded base tiles, this fixes the white space near algeria (sgb)

## Changes for 0.9.4.1

* fix bad anti aliasing effects when scaled at 100% (sgb)
* increase max heap size to 196M (sgb)

## Changes for 0.9.4

* simplify right click map dragging (sgb)
* reorganize menus slightly, add export menu (sgb)
* turn antialiasing on for map drawing, makes scaling look better on windows (sgb)
* fix spelling mistakes in revised (zero pilot)
* updated revized map (zero pilot)
* fix bug 1890628 freeze in triplea 0.9.3 (sgb)
* fix bug 1905413 can't move units with a warning (sgb)
* fix bid (all bid PUs were being added to the player) (sgb)
* In europe incomplete, changed the transport cost of artilery to 2, so 2 may be transported (comradekev)
* fixed bug[ 1896778 ] In Pacific game cannot move between sea zone 37 and Kiangsi (comradekev)
* fixed bug [ 1910221 ] Undone Movement Null Pointer (sgb)
* update great war to version 2.0 (Jason Clark)
* fix highlight unit drawing bug (sgb)
* fix null pointer when ai plays in capture the flag (sgb)
* improved game notes button (sgb)
* fix null pointer when attacking neutral countries (sgb)
* add ant run command for running from command line (sgb)

## Changes for 0.9.3

* fix [ 1870424 ] can't leave tic tac toe game after the game is over, also fix tic tac toe networked mode (sgb)
* disable main button on startup screen, as it overrides send message send (sgb)
* more PBEM posting fixes (tclayton)
* re-add screenshot overlay settings to map.properties in revised (tclayton)
* fix bug [ 1860285 ] solutions chooser offers no solutions (tclayton)
* fix bug [ 1851498 ] id should not be required in pbem games (tclayton)
* fix bug [ 1668015 ] disallow neutral territories in route in revised (tclayton)
* fix bug [ 1878700 ] edit mode: remove unit bug (tclayton)
* fix bug [ 1875092 ] Missing "No place for unit to land" warning (tclayton)
* fix bug [ 1862922 ] foreign planes on carrier (tclayton)
* fix [ 1867299 ] Initial industrial complexes have limited production (comradekev)
* fix bug [ 1746101 ] defending units in pacific show incorrectly in battle display (comradekev)
* change Load new game to Choose Game on startup screen. (sgb)
* fix bug [ 1855420 ] Unable to move fighters during non-combat movement (tclayton)
* fix bug [ 1856374 ] movement panel crash (tclayton)
* put engine version in system properties for debugging (sgb)
* mark kamikaze moves as such in the history (sgb)
* fix bug [ 1856656 ] IllegalState exception (sgb)
* disable chat time menu in non networked games (sgb)
* add limited chat flood control (sgb)
* [ 1837246 ] deploy troops phase window behavior (sgb)
* fix bug [ 1855427 ] submerged subs prevent air units from moving (sgb)
* add japanese, british, russions rockets, australian, canadian, neutral puppet state marine and neutral cruiser unit images (zero pilot)
* use rocket images when a player has rocket tech advance (sgb)

## Changes for 0.9.2

* fix bug where if your capital fell, and you captured another players capital, you could buy units (sgb)
* PBEM posting fixes and cleanup (tclayton)
* don't proxy PBEMMessagePoster, remove serialization (was broken in multi-player)
* fix EndTurnDelegate serialization
* only show Turn Summary Posting widgets if posting is enabled
* fix bug [ 1825831 ] in multiplayer mode, all players can edit (tclayton)
* fix bug [ 1825841 ] comment mode split bar visible (tclayton)
* WeakAi improvements (masch)
* fix in land route calculation (does not take neutrals into account)
* improvement in Non-combat move. Moves towards enemy territories even if there are no units.
* purchase 20% transports if player is amphibious. Can boost that - buy
* only transports if landing point is heavy armed e.g. UK or Japan
* Try to capture unprotected land in amphibious combat ( 1 transport on different route )
* Ignore channel feature for sea routes, if endpoint is on channel territory ( otherwise you cannot attack that)
* patch [ 1827892 ] Fix NPE crash when loading PBEM game (rrowell)
* for installer with java, update embeded jre to 1.6 (sgb)
* fix bug [ 1823400 ] Filename typo causes Exception to be thrown (sgb)
* fix bug [ 1825576 ] Missing entry in four_if_by_sea.xml (sgb)
* fix bug [ 1767304 ] Great War v.1.5 sz67 to sz57 bug (sgb)
* fix bug [ 1563219 ] Possible to buy more units than can be placed (sgb)
* fix bug [ 1535135 ] loading save game bug (sgb)
* fix bug [ 1718350 ] AA guns on LL fire once (sgb)
* upgrade to looks 2.1.4 (sgb)
* partial fix for bug [ 1750148 ] Transport error unloading to enemy territory from hostile water (sgb)
* fix bug [ 1753871 ] SaveGameFileChooser bug (sgb)
* fix bug [ 1692668 ] AI UK loads US troops on UK turn (sgb)
* new Territory/Production summary options for Turn Summary (tclayton)
* fix game xml files and PlayerList class to preserve proper player ordering (tclayton)
* new Comment Log feature for adding comments/trash talk to game history (tclayton)
* new PBEM Turn Summary posting feature (tclayton)
* new "Edit Mode" feature (tclayton)
* add PersistentDelegate support and IDelegateHistoryWriter interface to engine (tclayton)
* new UnitAutoChooser feature (tclayton)
* create UnitAutoChooser class to translate chosen categories into possible unit solutions
* update MovePanel to use UnitAutoChooser for unit selection and route planning
* update UnitChooser to support UnitAutoChooser and solution browsing
* fix existing UnitChooser arrow icons and add left/right icons for solution browsing
* MoveDelegate cleanup (tclayton)
* move all validation methods to MoveValidator so they can be called on client side
* make helper functions in MoveDelegate static, so they can be called on client side
* fix a few spelling mistakes in symbol names
* partial fix for bug [ 1742775 ] Operating system freeze on Windows 98 with Ati Graphics Card (sgb)
* Added support for "color" property, including color picker UI (dowobeha)

## Changes for 0.9.1

* implemented minimax AI and alpha-beta AI; currently used in Tic Tac Toe and King's Table (dowobeha)
* implemented new King's Table game and Tic Tac Toe game (dowobeha)
* created common code package to minimize code duplication between different games (dowobeha)
* enhanced game framework to allow easier implementation of new grid-based games (dowobeha)
* show time in chat panel, default is to show chat time in lobby, but not in game (gansito)
* bug fixes (tclayton):
* [ 1204024 ] Missing Sea Zone
* [ 1510049 ] unloading troops bug
* [ 1640658 ] fighters in classic attacking on friendly carrier
* [ 1641051 ] Transport Unloading Bug
* [ 1652870 ] each phase should begin with focus on tabs panel
* [ 1655181 ] clean up history log entries
* [ 1659713 ] Java Exception
* [ 1661095 ] MovePanel should dynamically select best units for route
* [ 1662464 ] null pointer exception when skipping move phase
* [ 1662938 ] shadow units don't appear in map overlap sections
* [ 1671750 ] improve logic for transport load order
* [ 1672743 ] exceptions thrown by delegates get mangled by proxy
* [ 1696749 ] Unload problem from allied transport after undo
* [ 1753866 ] load and unload should have default selections
* feature [ 1749993 ] new "History Log" feature (tclayton)
* feature [ 1746894 ] Save Screenshot feature (tclayton)
* feature [ 1673208 ] show move validation warnings/errors when moving mouse (tclayton)
* feature [ 1661088 ] code cleanup - implement MovePanel getMovableMatch() method (tclayton)
* new revised map (zero pilot)
* in revised, remove connection between 25 Sea Zone and 43 Sea Zone (zero pilot)
* new vc image (zero pilot)
* japanese tanks defend at 2 in pacific (comradekev)
* non jopanese units defend at 1 in first round of pacific (comradekev)
* fix empty sea zone in gulf of mexico in classic,battleship_row,four_if_by_sea,and iron_blitz (Scarbrow)
* four if by sea turn order changed (Scarbrow, rodthegod)
* add attack/defense/movement to production panel (gansito)
* move test classes to test directory (sgb)
* add export game setup charts menu (gansito)
* show battle casualties in battle display (ahmet)
* mark remote players as remote (ahmet)
* allow multiple canals per sea zone (tekkyy)
* allow centering map on battles (ahmet)
* alt mouse scroll zooms the map in and out (ahmet)
* new unit images (lssah)
* add moderator functions, moderators can boot players, change passwords, and ban ip addresses (sgb)
* better logic for determining attacker defender in odds calculator (Gansito)
* add uninstaller (Gansito)
* allow odds calculator to specify simulation count (Gansito)
* banned ips and banned words are stored in lobby database (sgb)
* the lobby server can now ban ip address (sgb)
* add serialversionuid's to several classes (dagon)
* add unit icon to unit images on the territory tab (dagon)
* add menu to show/hide units (Gansito)
* lobby game table doesn't loose selection when games are added/removed or updated (sgb)
* better route finding logic (sgb)
* added six nation free for all mod for revised map (the_devil_inside)
* fix bug [ 1655283 ] Java 6 reserves java.awt.Window method getWindows() (sgb)
* update to great war 1.3 (Jason Clark)
* add canals to Great War and Big World (Black Elk)

## Changes for 0.9.0.2

* fix bug [ 1640596 ] 0.9.0.1 Revised Map Wrap Issue (sgb)
* Fix bug where dissapearing networks players would not be removed from the game (sgb)
* allow lobby server to ping clients to ensure the are still there (sgb)

## Changes for 0.9.0.1

* Adjusted British starting units (Jason Clark)
* fixed infantry defense in Classic (sgb)

## Changes for 0.9

* improve great war map (Jason Clark)
* improve great war african markers (Jason Clark)
* fixed orientation of french zeppelin in great war (Jason Clark)
* In great war, the US now has a starting transport, 1 inf and 1 cav. 1 us cruiser removed. (Jason Clark)
* In great war, removed connection between Tanga and Weidmannshiel. (Jason Clark)
* focus on action button when battle window is activated (sgb)
* lobby server checks client's computer is network accessble when client hosts a game (sgb)
* fix [ 1611289 ] map scrolling bug (sgb)
* client only waits 10 seconds for connection to servr to be made before aborting (sgb)

## Changes for 0.8.6

* fix infantry in classic (sgb)
* make convoy zones stand out better (sgb)
* read output of exec'd lobby games (sgb)
* Saved games in user.home/triplea (not .triplea) for linux and user.home/Documents/triplea for mac (sgb)
* better logic for finding local ip address (sgb)
* fix loby where clients could not find real server address (sgb)

## Changes for 0.8.5

* allow neutrals to have different unit types (sgb)
* fix bugs where all bombers in lhtr defend at 2 (sgb)
* update big world map (surtur2)
* alt click/unclick selects 1/10 the type (Nate)
* allow weak ai to move into empty nuetral territories (Nate)
* make dialog clearer for planes can't land (sgb)
* handle marti dice server error messages (sgb,clausewitz)
* allow setting of lobby server lookup url in a file called lobby.properties with a key server in the root triplea directory (sgb)
* fix max select when more than one type of unit present (sgb)
* fix some click to continue to press sapce to continue (sgb)

## Changes for 0.8.4

* change click to continue text to press space to continue on battle screens (sgb)
* add an option in battle calculator that at least 1 attacking land unit must survive (sgb)
* fix transport capactity in europe, add connection between adriatic and central med, make saudia arabia nuetral (sgb)
* change network to use nio (sgb)
* fix bug where units originally in a sea zone with a submerged sub that is attacked by another unit cant leave the sea zone (sgb)
* show battle calculator on current territory when pressing ctrl B (sgb)
* ctrl+ and ctrl - zoom in and out (sgb)
* mark lhtr as complete. low luck rules for heavy bombers still need to be added for all versions (sgb)
* allow fighters to hover in sea zone where carriers can be produced under them for lhtr (sgb)
* move dice server config into properties file (sgb)
* allow controlling of name placements using name_place.txt (sgb)
* fix sea zone boundaries when map is scaled (sgb)
* add great_war mode (surtur2 and Triplelk)
* update triplea_linux.sh (Daniel Roethlisberger)
* show messages when people join/leave chat (sgb)
* fix scroll bug where map would jump when mouse scrolled in non wrappable maps (sgb)
* make convoy zones more transparent (sgb)
* fix neutral fighting bug (sgb)
* fix spelling mstakes in classic map (sgb, RogerCooper)
* add max button to place dialog where number of units that can be placed is limited (sgb)
* fix bug [ 1563239 ] Bad scroll increment for scrollbars (sgb)
* fix bug [ 1563227 ] Continue button does not show up (sgb)

## Changes for 0.8.3

* make odds calculator use MustFightBattle, update ui (sgb)
* allow scaling of auto placement finder. On the command line, type the scale after the command,

* add map decoration images. create a file called decorations.txt in the map directory. The format is the same as place.txt, with an image name, then list of points where

* disable territory name drawing for territories listed in map.properties with a property like dont_draw_territory_names=Germany,Japan (sgb)
* allow for map scaling (sgb)
* let ai play in multiplayer games (sgb)
* fix [ 1533252 ] problem clearing out pbem (sgb)
* make the game look better on a mac (sgb)
* better factory images (eleazar)
* lhtr hb rules (not sure if low luck is correct) (sgb)
* lobby server/client (sgb)
* you can kick players out of a game on startup screen (sgb)
* add odds calculator (zengland)
* fix bug [ 1505192 ] air land in conquered territory (sgb)
* allow networked games to be password protected (sgb)
* for mac and linux, save games in home folder (sgb)
* add convoy centers in europe map (iron cross)
* put saved games in users home directory (sgb)
* fix misspelt territory names in revised and lhtr (Jeffrey Henning)
* add lhtr victory citries (sgb)
* super subs defend at 3 in lhtr (sgb)
* make lhtr aa guns not fire in non combat move (sgb)
* pacific and europe map fixes (Opurt, FlyingSpaghettiMonster)

## Changes for 0.8.2.1

* fix installer with embedded java to actually use the embedded java (sgb)
* default sound to off (sgb)
* fix nz territory in four if by sea (rod the god)

## Changes for 0.8.2

* fix bug where observers joining mid game may ignore some updates (sgb)
* lock game data before switching to history (sgb)
* fix bug where casualty selection would sometimes appear before the battle panel (sgb)
* fix bug where naval bombardment doesnt work for the first player to fight in round 0 (sgb)
* change two if by sea to four if by sea (rod the god)
* remove nuetral player in capture the flag (sgb)

## Changes for 0.8.1

* add capture the flag map (iron cross)
* let ai place in places other than the capitol if not all units can be placed in the capitol (sgb)
* fix move bug when no units are selected with pop up (sgb)
* fix "Not enough units in starting territory" bug when hitting done (sgb)
* documentation updates (sgb)
* fix history update bug in multiplayer (sgb)
* fix bug where if A has 1 carrier and no fighters in a sea zone and is allied to B with 1 carrier and 3 fighters in the saem sea zone, when A moves his carrier out of the sea zone, B's 1 fighter doesnt move with it (if A moved his carrier in the sea zone after B moved his carrier into the sea zone)
* show strategic bombing raid casualty notification (sgb)
* fixed bug where deselecting game-confirm enemy casualties would also stop confirming your own automatically selected casualties (sgb)
* europe and pacific map fixes (zero pilot)

## Changes for 0.8

* save last used map skin and unit size (beagle)
* add next and back buttons to history (sgb)
* renamed game xml files (sgb)
* moves canal info to the xml file (if you have a mod based on revised or classic, canals will be broken unless you add them in the xml, do a search for canal in classic.xml or revised.xml to see how it is done) (sgb)
* fix bug where aa guns in retaken allied capitols werent reverting to there original owner (sgb)
* replace random ai with weak ai (sgb)
* fix pbem saved emails not always showing up on the start screen (sgb)
* highlight units on mouse over when moving (sgb)

* when changing to a skin that has relief images, always show the relief images (sgb)
* add destroyer production to europe map (sgb)
* fix map skins in zip files on windows (sgb)
* map skins must use - not : to seperate skin from map names (eg revised-Coal, not revised:Coal). Windows doesnt allow : in file names (sgb)
* if user presses done when no moves were made, confirm that they do not want to move (sgb)
* fix bug [ 1440134 ] rockets shouldnt move after firing (sgb)
* add tripleawarclub dice server (clausewitz, pughead, sgb)

## Changes for 0.7.4

* remove autosave... from console output (sgb)
* allow map skins to depend on each other (add a dependencies.txt file to the skin, with a single line dependencies=skin1,skin2,skin3) skin1 is the name of the skin (eg pact_of_steel:coal, if pact_of_steel:coal is in a zip file, do not include the .zip)
* better retreat dialog (sgb)
* allow map to have PU images. Images should be in the map folder, in a folder called PUs. They should be named 1.png, 2.png... if no png image is found for a given number, a string will be drawninstead. (sgb)
* maps (and skins) can be zip files (sgb)
* map skins can override unit,flag and vc images (sgb)
* map skin directories must now be named original_map_name:Skin, rather than original_map_nameSkin as before (sgb)
* move images and maps to top level folders (these are not on the classpath). (sgb)
* allow defining where to place PU markers using pu_place.txt. The x,y location is such the point is the bottom left of the image. (sgb)
* allow turn off drawing map names in map.properties using, map.showTerritoryNames=false (sgb)
* move chat panel to main window for networked games (sgb)
* fixed bug where autosave game would add too many PUs at start up (sgb)
* fix bug where attacking air units couldnt retreat if all attacking subs moved to attacking sea zone via submerged route (sgb)
* allow clients to save a networked game (sgb)
* game menu to show who is playing what player (sgb)
* when a player (not an observer) leaves the game, the game is saved automatically, and the game ends (sgb)
* observers can join and leave the game (server can optionally ban new observers) (sgb)
* new startup screen (sgb)
* add minimap (map by Clausewitz)
* add delegate execution manager, block delegates from executing while save in progress (sgb)
* make game data lock into a read/write lock, extend the game data lock to history (sgb)
* add random ai (sgb)
* if two players with the same name join the game, add a \_1 to the second player (sgb)
* remove ISaveableDelegate, all Delegates are saveable (sgb)

## Changes for 0.7.2.4

* move some code into swing event thread (sgb)
* dont let players press dont place once player selection is done (sgb)
* should read you need java \>= 5.0, not java \> 5.0 (sgb)

## Changes for 0.7.2.3

* make battle window a dialog (it will always be in front of the main window!) (sgb)
* fix invalid roll count in multiplayer games when all bombers are hit by aa guns (sgb)
* fix null pointer when placing units in sea zone with enemy units (classic game only) (sgb)
* fix null pointer when when selecting null territories during movement (sgb)

* fix convoys (adam_j)
* fix bid purchase (sgb)
* Iron blitz mod (ic)
* fixed string index out of bounds when rolling pbem dice (sgb)

## Changes for 0.7.2.1

* fix stat panel in europe (sgb)
* fix bug 1357768 0.7.2 dead defenders firing (sgb)

* on PBEM screen, add id field (for challenge id) (sgb)
* when clicking on a battle in history, center map on that territory (sgb)
* allow unloading units from a battle zone into newly conquered territories (sgb)
* allow saving games during battles (sgb)
* shift click on a unit (or territory) to select all units in the territory (sgb)
* rename attachment to attachment (sgb)
* remove singleton image factories, move to UIContext (sgb)
* when retreating from a sea zone, if a fighter has no movement, the fighter gets a 1 movement bonus (sgb)
* battleships can only bombard if they are in a sea zone where transports unloaded (sgb)
* fix bug [ 1277099 ] map refresh problems undoing move with captured aa gun (sgb)
* Japanese victory points for a&a pacific (Adam_J)

* updated readme and user docs (George_H)
* if we have multiple transports that unloaded troops to an amphibious assault, then the transports

* various no pop up movement bugs (sgb)
* fixed chinese tech in big world 1942 map (sgb)
* partial fix for marines (marines still do not show up correctly in battle table) (sgb)
* fixed missing connection from solomon in pacific map (sgb)
* fixed bug [ 1259381 ] Bid purchasing (sgb)
* fixed no pop up movement for scaled units (sgb)
* removed territory attachments for sea zones in big world map (sgb)
* Fixed missing connections in big world map, north to south brazil, and sea of Okhotsk to West Bering Sea (kc1189)
* More email validation (Adam_J)
* Chinese infantry mechanism added for a&a pacific (Adam_J)
* Convoy Zones implemented (Adam_J)
* Add code for marines (Adam_J)
* Add code in for kamikaze (Adam_J)
* fix bug located [__brokenLink__] (Adam Jette)

## Changes for 0.7.0

* add movement help to help menu (sgb)
* remove hints menu (sgb)
* movement now done without pop up dialogs (sgb, lnxduk)
* only allow transports to unload units to 1 territory (sgb)
* fixed bug [ 1238910 ] PBEM mode cannot accept subdomains (sgb)
* add "click" to select casualties button, many users are confused and dont know to click to select casualties (sgb)
* reduce network traffic somewhat by more efficient serialization (sgb)
* autosave now happens at the end of a turn, after combat move and before non combat (sgb)
* use annotations to determine when to autosave (sgb)
* change to jdk 1.5, 1.5 is now required to build and to run (sgb)
* fix bug where versions like 0.6.0.1 would be displayed as 0.6.1 (sgb)

## Changes for 0.6.0.1

* fix bug [ 1225276 ] Aircraft unable to attack or land (sgb)

## Changes for 0.6.0

* updated developer docs, incomplete for now (George_H)
* draw a line under overflow units so you can tell what belongs in a territory (sgb)
* fixed bug where you could retreat subs if all your opponents destroyers were destroyed in one round of combat (sgb)
* fixed bug where damaged battleships would not repair while viewing history (sgb)
* fixed small map refresh (whole map goes white) when switching skins (sgb)
* fixed bug where sometimes dice would not show up on the select casualties panel (sgb)
* removed "Heavy Bombers Pick best of X Dice" option from classic and wandering head big world, it didnt work (sgb)
* Fixed bug where transport moves could be undone before moves where the transport had been loaded/unloaded (sgb)

## Changes for 0.5.4

* fixed bug where units could blitz through territories with an aa gun if they blitzed in 2 steps (sgb)
* fixed bug [ 1188411 ] Missing client text (Chat window) 5.2.2 (sgb)
* fixed bug [ 1205387 ] Saving game during combat 0.5.3 (sgb)
* fixed bug [ 1205775 ] 0.5.3 eMail Bug - hyphens not allowed in emails (sgb)
* fixed bug [ 1205504 ] Units can land in amphibious assaults when transport is sunk (sgb)
* fixed bug [ 1198828 ]Heavy Bomber Tech Broken 0.5.3 (sgb)

## Changes for 0.5.3

* added europe and pacific maps (incomplete versions) by iron cross (George_H)
* added extra dice statistics such as, median, variance, and standard deviation (George_H)
* fix bug [ 1023326 ] Fig Landing Problem, J1 (sgb)
* more flexible validation for planes landing on carriers (sgb)
* add stat export menu item Game-\>Export Game Stats (sgb)
* upgraded plastic look and feel to version 1.3.1 (sgb)
* add vc drawing and added vc cities to stats (sgb)
* better email address ui and validation, allow up to 5 emails in to and copy (sgb)
* added white factory images (zero_pilot)
* added drawing capitol markers (capitol markers contributed by black elk) (sgb)
* added junit.jar file to lib and removed it from .ant.properties (sgb)
* fixed bug [ 1070176 ] Mistakes in calculating Battlescore (change in TUV) (sgb)
* fixed bug [ 1116632 ] v0.5.1.1 TripleA skipping battle in Borneo (sgb)
* fixed bug [ 1145318 ] Another Error on 5.2.2 (sgb)
* fixed bug [ 1157717 ] 0.5.2.2 Error with question : Sumerge subs (sgb)
* fixed bug [ 1175467 ] game "stuck" when doing multiple battles with same units (sgb)
* fixed bug [ 1171596 ] Rocket Tech bug v0.5.2.2, we now always ask what territory to attack with rockets, even if there is only one choice, this allows the user to decline a rocket attack (sgb)
* during battles the dice are sorted according to unit type so that when you review the dice rolls, you can tell what unit rolled for which dice (sgb)
* fix bug [ 1144356 ] alter email header on PBEM (this is really a feature request) (sgb)
* added new chinese units and cruiser, halftrack, marine units (iron_cross)
* fixed [ 1158469 ] Missing units in Purchase Menu when odd number of choices (sgb)
* you can now specify victory cities in xml using a territory attachement (sgb)
* added tile map drawing (sgb)
* add a copy to clipboard button on the console (sgb)
* if available, console will print stack traces when enumerating threads (sgb)
* put neutral player color in map.properties (sgb)

## Changes for 0.5.2.2

* fixed Dont play button on client screen. (sgb)
* threading fixes. (sgb)

## Changes for 0.5.2

* add switch in map.properties to disable scrolling map around the edges (sgb)
* added scripted random for debugging (sgb)
* added new map by WanderingHead (wandering head)
* add confirmation prompt when exiting the game (sgb)
* jdk 1.4 - 1.5 compatability (sgb)
* Add has relief property to map.properties (sgb)
* Add default unit scroll size to map.properties (sgb)
* Changes to make TripleA compile under Sun JDK 1.5.x (George_H)
* Added better unix shell scripts for TripleA, thanks DMan for the scripts (George_H)
* Added better path search so TripleA can run from any directory (sgb)
* Now all map utils have proper "save as" dialogs (George_H)
* Added new class to prompt user to select a directory so map utils won't save files to a hardcoded dir (George_H)
* Define player colour in map.properties to allow easy modification and adding new players (sgb)
* Added option to limit PUs lost in a territory during one round. This is necessary to implement LHTR ruleset. (Ali Ibrahim)
* Fixed bug in Irony PBEM random source: It did not use the max parameter passed to the random methods. This fixes the AA casualty selection problem in PBEM. (Ali Ibrahim)
* Added new technology activation delegate to allow control of when technologies actually take effect. This is used to allow delay of technology activation in LHTR. (Ali Ibrahim)
* Changed mouse behavior such that only the left button is used to select a territory to put units in. (Ali Ibrahim)
* Added more options for unit size using submenu. (Ali Ibrahim)
* Changed ordering of properties in the launcher properties tab to use ordering in game XML file. (Ali Ibrahim)
* Added Map Skins code to allow multiple (1 and greater) map skins to be used for each game based on a directory search pattern. Skins must be in maps folder with game name as prefix (ie. revisedMySkin). (Beagle)
* Changed how bombardment works. Now users pick where to bombard before any battles are resolved. This allows users not to bombard with a unit (for example if they wish to move it during non-combat) by picking "None". This also fixes the bug where a a unit could retreat from a battle and bombard in the same turn. It also allows user to divide their bombardment shots however they like when there are multiple bombardment targets. (Ali Ibrahim)
* Fixed bug #1067768 concerning the border of seazone 27 and Belgian Congo. (George_H)
* Fixed bug #1067331 by removing the connection between seazone 51 and 56 for Pact of Steel mod. (George_H)
* Fixed bug #1067073 by removing the connection between seazone 15 and 16 for Pact of Steel mod. (George_H)
* Fixed bug #1043826 concerning missing sea zone border & missing pixles on border. (George_H)
* Added channel and remote messengers. (sgb)
* Added game vault. (sgb)
* Fixed bug [ 1053071 ] No non-combat movement (sgb)
* Fixed bug where properties werent being updated on client (sgb)
* Fixed bug [ 991810 ] Internet Bid Problem (sgb)
* Fixed bug [ 1051937 ] Number of bid PUs displayed (sgb)
* Fixed bug [ 1102812 ] flag image names not based on xml names (sgb)
* Fixed bug [ 1102225 ] Error by adding better error messages (sgb)
* Store pbem emails in saved game (sgb)
* Fixed bug [ 1095206 ] AA Firing too quickly v0.5.1 (sgb)
* Fixed bug [ 1092852 ] bug in 2bysea Version .5.1 (sgb)
* Fixed bug [ 1021352 ] advanced tech prob (sgb)
* Fixed bug [ 1021350 ] Tech Prompt (sgb)
* Fixed bug [ 1006050 ] Unable to conquer territories (sgb)
* Fixed bug [ 1021351 ] No Buy Confirmation (sgb)
* Add micro to Version, ie version can now be xx.xx.xx.xx (sgb)

## Changes for 0.5.1

* Fixed bug where defending transported units were not correctly removed when their transports were killed. (Ali Ibrahim)
* Fixed bug where transported AA guns fired in naval battles. (Ali Ibrahim)
* Added a new developer document with map utils info. (George_H)
* Added menu option to use small unit images on map. (Ali Ibrahim)
* Large improvement and re-organizing of user documentation. (George_H)
* Fully implemented Pact Of Steel mod (by Black Elk/Beagle). (George_H)
* Improved map directory structures and code for triplea concerning TerritoryData class. (George_H)
* Small iteration fix applied to PolygonGrabber to prevent crash. (Beagle)
* Improve all map utilities so they are user friendly and better to use. (George_H)
* Fixed bug where air units could define retreat paths (they still can in some games). (Ali Ibrahim)
* Added MersenneTwister Thread Safe (MT199937) Random Number Generator with Permission from Sean Luke. (George_H)
* Added Low Luck option following DAAK rules. However, the low luck rules were not implemented for sbr's and tech rolls. Also it is incompatible with the heavy bomber downgrade option. (Ali Ibrahim)
* Allowed transports carrying aa guns to move in combat, although the aa guns still cannot be loaded/unloaded in the combat move. (Ali Ibrahim)
* Fixed map bugs (missing connection between sz25, sz43, wrong connection between sz51, sz56, misspelling of Angola). (Ali Ibrahim)
* Added logic to prefer routes without neutral countries. (Ali Ibrahim)
* Fixed bug which did not allow placement of bid units. (Ali Ibrahim)
* Fixed bug which did not allow placement of units in classic. (Ali Ibrahim)
* Fixed bug which did not allow placement of AA guns correctly. (Ali Ibrahim)
* Fixed bug which did not correctly reload transports which had conducted an amphibious assault and then retreated. (Ali Ibrahim)
* Added capability to bid for allies. (Ali Ibrahim)

## Changes for 0.5.0

* Added TUV (total unit value) column in statistics panel. Added TUV lost in battle as part of battle end message. (Ali Ibrahim)
* Fixed bug in statistics table when adding a player such as Italy (George_H).
* Added logic to check production limits to display in production panel. (Kevin Sanders).
* Added logic to not consider moving land units into water if there are no transports there. (Ali Ibrahim)
* Added game defintion file, flags, color for Italian player. (George_H).
* Fixed bug where allied air units which are cargo attacked. (Ali Ibrahim)
* Changed game logic to allow destroyers to pass over submerged subs. (Ali Ibrahim)
* Fixed bug which didn't allow fighters to consider landing in gibralator due to issue with pathing and neutrals. (Ali Ibrahim)
* Added warning for users using Java 1.5 about some serialization problems which cause an incompatibility with saved games in Java 1.4\. (George_H)

## Changes for 0.4.9

* Fix for bug #1010428 bypassing the unit selection popup message when there is only 1 unit to be moved. (Ali Ibrahim)
* AI rules added,experimental. (Sean Bridges/Troy)
* Stack trace when starting triplea after a saved game fixed. (Sean Bridges)
* Fixed bug when defending subs get first strike fire, even if an enemy destroyer is present. (Sean Bridges)
* Changes in Battle Panel relating to SWING event thread to stop game from freezing in battle mode. (sgb [Sean Bridges])
* Fix for Bug #1001946 fixed for units crossing water. Now crossesWater only returns true if the route starts and ends on land and also contains a water territory. (James Damour)
* Fixes for Points 1,4 (and possibly 3) for Bug #1003736\. (Ali Ibrahim)
* Clean up of neutrality violation messages. (Ali Ibrahim)
* Now defending planes can land in any adjacent territory if their carrier is lost in combat. (Ali Ibrahim)

## Changes for 0.4.8

* Automatic casualty selection has been also added (Ali Ibrahim)
* Drag scrolling and mouse wheel scrolling (since 0.4.7). (lnxduk)
* TripleA Chat improvements. (lnxduk)
* Fix for null network interface on IRIX 6.5 OS. (George_H)
