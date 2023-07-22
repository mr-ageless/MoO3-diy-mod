V1.2.5 Code Patch

THROUGHOUT
Fixed a lot of typos and misinformation. 

CRASHES/HANGS
Fixed a hang in space combat which seemed to occur sometimes if a client was watching the last combat to be resolved.
    The screen would go blank after combat and just sit there (on the client). Everyone else would hang waiting for
    that client.
Removed the ability control bombardment after ceding/watching space combat in multi-player due to hang conditions caused
  by this functionality (it wasn't working on the clients any way) - may be revisited in the future. 
Fixed a bug where if the military build queue was open and then the Shipyards screen was opened on top of it and then
   a turn was processed, the game would crash.
Fixed a bug where if one of the tabs on the ship design screen was open and then the fleets tab was open and then escape
   was used to exit, the game would crash.
Fixed a bug on the Forces tab where the colony and outpost buttons would not be disabled if there were no planets in
   the system (could lead to a crash).
Fixed the crash when you open one of the tabs (weapons, engines, etc), switch to the fleets tab *without closing the 
   foldout tab first* and press the escape key to return to the galaxy screen the game would crash.
Fixed a bug where if the Sitrep was open when one of the build queue panels was open behind it, pressing the turn button
 would not advance the turn until the Sitrep was closed.

AUTORUN
Removed the line of code which was preventing bombardments from occuring during auto-runs. 

COLONIZATION
Modified the calculation which determined how many population points were en route to a user requested colony to
  use the population value for a colony pod instead of an outpost pod. THis should fix the problem sending too many 
  colony ships to fill a player request.
When attempting to land colony ship, ignore dead or retreating task forces.
Change rules for landing colony ships such that ships with a defensive alliance are ignored in neutral or owned
  systems (only will fail if the allied empire has a planet and you don't).
Added code to issue an AI colony request for each planet which reverts to unowned or outpost status to all civs which
 have sufficient scan information. This should make the AI colonize bombarded planets (still testing). It will NOT cause
 the AI to colonize these types of planets in an old save game (since the notice is made at the time of destruction) 

MILITARY AI
Made planet destroyer viable mission ship in long range task force so that AI may actually deploy planet destroyer ships. 
Rebalanced ground troop unit priorities to get support troop numbers more in line with requirements. 
Corrected an error in the spreadsheet which prevented the AI from building Infantry and PsyOps

SPYING AI
Remove AI preference for spying on human players (treat human players and computer players the same). Increase
  likelihood of AI building scientific spies. 

PLANETARY ECONOMIC AI
Add code to make AI build CorrCap buildings on its own.
Corrected a problem which was not deleting the system seat and related buildings when a new system seat was built on
  another planet. Corrected the problem that the new system seat would have to be built twice to stick. MOdified the AI
  to not move the system seat if a mobilization center was already built. Increased preference for not moving the Imperial
  Seat when it is destroyed.

PLANET SCREEN
Ship info on the military build queue of the planet screen now displays the hull size in addition to the ship class 
(orbital, system, star). 

SITREP
Changed planet hyperlinks in the sitrep so that changing the planet or star name will be reflected in the sitrep
   (sitreps in save games will not work).
Corrected behavior of sitrep in multi-player resume so that the hosts sitrep will not show up on the other machines.
 Note that sitrep information is only saved for the human player, so when a game is resumed and copied across the net,
 only the player playing the empire which was the human player on the host will get a sitrep on the first turn.

TECHNOLOGY
Slow down tech advance by about 33%.
Swapped CorrCap and GovCap modifiers to make the effects match the descriptions better.

DEV PLANS
Fixed a dev plan bug where if a planet classification has all three policies set, then none of the policies can be
   changed. 

DIPLOMACY
Fixed the bug which caused traded achievements to fail when they were not already in the tech tree. 
Correct Diplomatic text generator to use Intelligence Agreement text. Also will now use Demand War text for fulfill
 obligation message. The message will not have the targeted empire, but at least will make some sense now. 

ORION SENATE
Fixed a few bugs on the Orion Senate screen where scrollbar thumbs were not being reset when the text for a bill's
 closing, a bill's details, a law's details, or the details of a bill to propose were displayed. 

SHIP DESIGN SCREEN
Tech descriptions on the Ship Specials panel are now displayed in a scrollbox. 
Fixed a bug where the Clear Queued button would not clear a ship design from the build queue if the second item was not
 a ship and the third item was a ship design to be cleared. 
Added a shift-key modifier to the Mark Obsolete button so that the ship design being marked obsolete would be cleared
 from the build queue or marked for scrap if it had already been started on. 
Added a shift-key modifier to the Clear Queued button so that ship designs already started on would be marked for scrap
 as well as clearing out ship designs that have not been started on. 

HISTORY SCREEN
Fixed a bug on the history screen where a Y-axis scale value of 0 would send the game into an infinite loop. 
Increased the max value of the Y-axis scale on the history graph to 6.0. 

SPACE COMBAT
Removed the ability control bombardment after ceding/watching space combat in multi-player due to hang conditions caused
  by this functionality (it wasn't working on the clients any way) - may be revisited in the future. 
Modified the code in space combat so that the number of missile volleys remaining will be the max of all racks, rather
  than the most recently fired ones. 
Correct a problem which caused the same empire to always win the coin flip when both sides chose assault planet
 in space combat. 
Changed AI space combat retreat logic to use casus belli instead of current relations (should make them a little less
 likely to retreat, especially later in the game)
Clean up destroyed ships and task forces at the end of space combat to prevent improper behavior during bombardment
  and beyond.(For example, destroyed troop transports can no longer land their troops).

GROUND COMBAT
Corrected ground combat gravity preferences to match habitability preferences. 


V1.2 - Code Patch

THROUGHOUT
Improved behavior under alt-tab. Application normally will auto-refresh now.
Improved behavior of scroll bars such that they reset their position at appropriate times.
Modified behavior of sliders so that when clicking on the area outside of a slider arrow to set its
 position, the slider arrow is moved five pixels in that direction instead of to the point where the
 mouse was clicked. 
Effectively rewrote/reworked help text/tool tips, including right-click support and increased time-out
 value for mouse-over text.
All of the main UI tabs now remember the last sub-panel and return there.
Removed some unused tables from code and spreadsheets.
Fixed a bug where pressing the Esc key while the "Exit Game" dialog was open would cause the
 "Quit Current Game" dialog to appear. 
Fixed the bug that prevented the values for the UI background music in the spreadsheet Music.txt from
 being used. 

STARTING SCREEN
Swapped the positions of the Quick Game button and the Options button on the Main Menu screen to reduce
 the problem of accidentally hitting quick game when load was intended. 

TIMER
Fixed the 30/60 minute reminder such that it now actually works. 
Fixed the bug where the 30/60 minute reminder or alarm clock reminder would cause the game to hang if
 either was triggered while a Master's Note was being displayed (the reminder will be displayed after
 the Master's Note is closed). 
Fixed the bug where the 30/60 minute reminder would not work when loading a save-game from the Main Menu.
The Esc key now closes the Alarm Clock and the 30/60 Minute Reminder dialogs. 
Fixed the alarm clock to pay attention to the am/pm setting and allow it to trigger again in the same
 game if the time is changed in the options. 

SAVE GAMES
Added sitrep information to the save game. 
Modified the save game dialog so that files do not show up on the list if they are not valid save games,
 even when their extension is '.gam'. Modified header record of save game to be able to distinguish
 obsolete save games from new ones.
Added data set directory name and language directory name to save game header.
Fixed a bug where the Esc key wouldn't close the load and save game dialog panels. 
Added Ctl-S and Ctl-O (cmd-S and cmd-O on Mac) as hotkeys to save and load a game, respectively.
Changed sort algorithm to remove crash when displaying a list containing between 81 and 83 save games.

MULTIPLAYER
Command buffers and Save Games are compressed for sending over the net. 
Fixed bug causing unnecessary copying of auto save games when resuming a multiplayer game. 
Player entries in multiplayer lobby are colored blue when save game will be copied. 
Fixed bug with assigning players to empires when resuming a multiplayer game. 
Added destination options to multiplayer chat for sending messages to allies, enemies, and a specific empire. 

NEW GAME OPTIONS
Added interface to choose player color (active in single player only) 
Modified code to actually use playercolors.txt. 
Quick-game data partially loaded in to use as the defaults for the New Game Options screen. 
Quick-game data now not saved when creating a new multiplayer game. 
Added option to auto-run game for x number of turns. This will cause the AI to take over for the specified
 number of turns, after giving the human player time to do any initial setup in turn 1.

GALAXY CREATION
Modified Splinter Colony/Magnate Civ code so that splinter colony will only occur if the habitability zone
 is as good as any magnate. So, if it would be Green for a splinter, but is Sweet Spot for a Magnate, the
 Magnate will now get the planet (previously it would have been a splinter). This should make all Magnates
 available for all Species, although they will still not get the same distribution.
Magnate Civ population is now spread out across half of the planet instead of one region to reduce the
 overpopulation push that causes them to spread like wildfire when first colonized. 
New Orions home system now uses the best home system in the galaxy algorithm that the other empires use when
 creating the galaxy. 

HARVESTERS
Modified code so that a negative number in the spreadsheet indicates that a race has no value to the
 Harvesters. Apply this number to the non-corporeals. 
Added unrest factor for Harvester victims (anyone but non-corporeals). Amount based on number of Harvesters
 on the planet. 
Added unrest factor for Harvesters living on a planet with no "free-range" food available. 

COLONIZATION/MILITARY BUILD AI
Fixed a bug in the colonization AI that was not properly reducing the desirability of systems containing
 colonies of other empires. 
Fixed a bug in the colonization AI that was detecting magnate civilizations in most cases. 
Fixed a bug in military construction AI that was improperly calculating the amount of transport capability
 in the empire, therefore causing it to build WAY too many transports.
Modified transport needs assessment to ignore deployed troops. Now will shoot for 80% of capacity required for
 troops in reserve or being built. 
Correct a problem which caused the AI to build system colony ships when none were needed (or usable).
Modified military AI so that when considering building an orbital, it will look for a design of a size that
 the planet can already build rather than insist on the planet having the capacity to build the largest ship
 in the empire.

COMPUTER PLAYER AI
Modified AI to utilize "set migration" 
Modified military AI to not keep ships in the reserve automatically when defending. 
Added calculation to deploy ground troops defensively when in a shared system or adjacent to another civ. 
Increased size of ships built by AI.
AI now obsoletes old designs and removes obsolete designs from build queues when it redesigns. 
Fixed a bug where AI task forces sent to attack would not when the border policy is defensive front (they
 now will engage if they have attack orders) 
Fixed a problem in the lottery hopper that caused really attractive targets to be ignored, sometimes causing
 AI fleets to not engage. 
Modified lottery for selecting a civ to attack to increase the odds of attacking a human player (as opposed
 to another computer player) in hard or impossible. 

PLANETARY ECONOMIC AI
The Planet AI will no longer immediately put an item back in a build queue if the user has removed it. It will
 absolutely avoid adding that item into the queue for about 10 turns after the user has removed it from the
 queue. (Does not yet apply to military AI)
Planet AI should be a little less likely to keep building if the planet's population is too low to fully run
 the buildings already on the planet. 
Increased range of numbers used when doing cost/benefit analysis so that fewer items would be resolved as
 having no value, especially when HFOG is high. 
Increased priority of picking the best regions for building farms and mines and increased consideration of
 biodiversity when picking a region for farms. 

GALAXY SCREEN
Added menu item to game menu to view the race picks chosen for the current game. 
Modify galaxy screen so that star names and empire flags remain visible up to the halfway zoom point when
 zooming the galaxy map out. 
Fixed bug that allowed a task force to fly through a Guardian system without stopping. 
Added ctrl-click to force direct travel to another star (off-road if no starlane).
Fixed a bug where enemy task forces would sometimes be visible when far away in a star lane instead of when close. 
On the galaxy map, a small colored chevron is drawn in the lower-right corners of the task force icons to
 indicate which empire they belong to. 
Added range of turns so that when you select a bunch of fleets and tell them to go somewhere it will say
 "ETA:1-2 turns" instead of just giving you the fastest time. 
The task force information window on the galaxy map now shows the ground troop and ground unit information
 for any transports. 
Fixed a bug with the 'Prev/Next Fleet' hotkeys where it wouldn't work sometimes if no fleet was selected and
 sometimes fleets not belonging to the player were included. 
Fixed a bug where pressing the Turn button while the galaxy map was in empire borders mode would cause the
 galaxy map on the next turn to display a combination of the regular map and empire borders. 
On the galaxy map in empire borders mode, if deployment centers exist in a star system but the player has
 none in there, the color of the icon is changed to grey. 

SYSTEM SCREEN
Added button to rename star systems at the System Level display in a single player game (note: max 20 chars,
 the player currently has to have at least one colony in the system when renaming, and no duplicate star names
 allowed). Only visible when no planet is selected. 
Fixed the system / planet transition animation so that systems with one or two planets are proportional in
 speed to systems with 6+. 
Moon sizes displayed next to size of the planet in the survey screen.
Corrected display of moons so that size is appropriate for the now listed moon size. 
Dominant species for a planet displayed on the system level view. 
Player flag icons added to the set of planet status icons on the System Level view to indicate which planets
 have an imperial and / or system seat. 
Add turns left to completion to the display on the System Econ panel for the items
currently being built by the planet. 
Icons of build queue items in System Econ panel have mouse-over help text dynamically added to them to display
 the name of the item plus the description. 
Added migration orders button to the System Forces panel. 
Added buttons to the System Econ panel to go straight to the build queue(s) (without having to drill down manually). 
Fixed some planet selection bugs in the forces view of the system screen, including the crash when you leave
 the screen with the flashing "select Planet" message. 
Fixed a bug on the System Forces display where the names of unexplored stars would be shown as the destination
 for a task force. 
Fixed a bug on the System Forces display where the destinations of ships / task forces that didn't belong to
 the player would be shown. 

PLANET SCREEN
Fixed a bug where hitting the ESC key to close a planet information sub-panel would prevent the planet panels
 from being opened again with the TAB key. 
Fixed bug that would improperly classify planets as frontier, and another which would allow set both the primary
 and secondary classification to the same thing. 
Added button to rename a planet from the Planet information screen (note: max 20 chars, may not be available
 in multiplayer depending on how testing goes). 
Added code to remove the Rescue Leader and Random Tech specials after they are used. 
Added magnate species to environmental preference lists.
The Planet Environment panel displays the species preference of the dominant race on the planet instead of the
 player's race when the panel is collapsed. 
Moon sizes displayed next to size of the planet.
Temperature and atmosphere values of the moons of a planet displayed on the planet environment panel.
Icons of build queue items in the Planet Econ panel have mouse-over help text dynamically added to them to
 display the name of the item plus the description. 
Added button to lock a planet's military build queue so that when an item finishes building, another of its
 type gets placed immediately into the queue again. This has the side-effect of keeping the military AI from
 adding anything into the queue of that planet. 
Estimated system tax income is now included in the income numbers in the econ panel. 
Added a new expense "Gift to Empire" to the Planet Econ panel plus a checkbox so that the player can set whether
 or not the planet gives its excess money to the empire. Excess money is any bank balance in excess of 10x the
 planet's income (the 10 is in a spreadsheet). 
Corrected coloring of the overdrive indicator on the economic and research sliders. Color was changing at
 multiples of AU instead of multiples of PP (or RP). 
Fixed a bug where the game would crash if you were at the System Level display with a planet selected and then
 you loaded a save game and attempted to go to the Planet Level display of a planet. 
The race populating a region is now displayed as well as the unrest level of that region. 
DEA improvements and regional buildings in progress are now displayed in the infrastructure panel. 
DEAs that have organic FLUs have them listed under the buildings the DEA contains. 
Effect of government DEAs on the overall infrastructure of a planet now shown. 
Selecting a region in the Planetary Infrastructure panel will display data about the region. 
Added option to replace an existing DEA with another one by marking it to be scrapped and then submitting a DEA
 request once the existing DEA has been scrapped. 
Fixed the bug where the progress of Space Port DEAs being built would not be shown.
Corrected the display of the amount of money generated by a spaceport. 
Corrected a problem where the effect of some buildings was sometimes lasting after the building was destroyed. 
Recalculate regional population density after gathering all modifiers. Previously, the value was calculated
 (and cached to avoid recalculation) before the ecosystem density, moon mods and any regional buildings were considered. 

SITREP
Added filters for Construction, Military Construction, Espionage and Planetary Migration. 
Any items that are built in the Military build queue are now considered a military item (shipyard buildings,
 planetary bases, etc.) by the Sitrep and are a) hyperlinked to the Military build queue and b) use the Military
 construction filter. 
Clicking on the hyperlinked system name on the sitrep issued when the task force has reached its destination
 will center the map on that star (shift-click will open the system screen instead). 
Issue sitreps when AI bombards for you or when AI bombards you. 
Added text for bankruptcy warning sitrep (will warn when current spending will result in bankruptcy within ten turns) 
Moved planet bombardment, planet destroyed, and defenseless planet bombarded sitreps to spreadsheets
 (text was in the code). 

TECHNOLOGY
The tech level of a school is now displayed next to it's funding level. 
Fixed some problems with fighter and missile armor costs which had prevented the creation of new starting ships
 in the data patch. Created new starting ships. 
Rebalanced tech tree to get more techs into the lesser used schools 

FINANCE
Added a line to the finance ledger for gifts from planets (see previous update)
Corrected the overdrive calculations for empire research grant money, so that the proper number of RPs are generated.

HEAVY FOOT OF GOVERNMENT
Reworked HFOG calculation so that it is based on population and number of systems. Effect of economic FLUs
 and any modifiers from leaders or government type (or race picks) are still applied. (No longer is reset by
 government change and no longer grows automatically) 

DEVELOPMENT PLANS
Fix Dev Plans UI such that it acts more dynamically in the adding, replacing, and removing of plans. 
Added loading and saving of Dev Plans to external file. 

PERSONNEL SCREEN
Changed the default of the Leaders screen to be the Espionage tab. After the first visit it will default to the
 last visited tab. 
Fixed an error that would allow a fifth, invisible leader to be acquired via a rescue leader special. Limit is
 now hard set at four. Any additional leaders will not be acquired. 
Added min and max luck range values to the leader spreadsheets so that each leader can have a different, moddable
 lifespan. Modified code to use those values and allow the lifespan to be greater than 127 (previous limit). 
Fixed diplomatic spies so that they blow up Government buildings and modders can add diplomatic spy missions. 

DIPLOMACY
Fixed a bug where pending diplomatic offers were not cleared when contact was lost, which could cause empires to
 be allied (or have other agreements) when not in diplomatic contact. 
Removed a divide by zero crash processing a "Demand Gift" message when the receiving empire's GDP is 0.
Treat all duplicate trade agreements (of all types) as improvements to the original, preventing multiple
 agreements of the same type. 
Moved application of trade modifiers so that sanctions, embargoes and open borders would affect existing trade agreements. 
Externalized value used to determine when a trade or research agreement can be improved. (Currently requires a
 25% increase in the limit, which is calculated using the lesser or the two civs) 
Corrected an initialization problem which was causing the Fullfill Obligation agreement to not actually cause
 the proper war to be declared. 
The target civ of a Fulfill Military Alliance message is now shown.
Tech exchange items on the Diplomacy screen now have help text dynamically generated to display the school, tech
 level, and description of the tech. 
Corrected a bug in which an AI players counter offer would ask you for things it already has instead of things you have.
Externalized parameters for minimum number of turns before a war can lapse, and the minimum number of turns
 after a lapse that the AI can redeclare a war based just on low casus belli. 
Added a "means war" counter value to the diplomatic effects of combat loss table and set it to add one to the counter
 when a planet is lost to ground combat or bombardment.
Modified "means war" counter trigger values so that each civ/civ relationship uses the sum of the two sides values,
 making more diplomatic races affect the trigger points of the less diplomatic races in their contacts. 
Reset the "means war" counter when at war, count items which increment the counter as if combat had occurred. 
Externalized some parameters used to calculate the diplomatic effects of combat. Added planets lost values to those
 already existing for hull spaces, troops, buildings and population.
Fixed a bug in the Foreign Matrix screen where the drop-down menu to show which empires you have a specific
 relationship with would also include empires that you had diplomatic contact with but was subsequently lost. 
Perceived casus belli of the empire selected for diplomatic information to the empire currently selected for
 the center of the Foreign Matrix screen is now displayed. 

ORION SENATE
Externalized parameters for Orion Senate presidency election, including a value for number of stars in galaxy to allow
 the Orion's vote to scale with galaxy size. Multipliers for number of system, planets and pop points are in a table,
 and Orions and other civs have separate values. 
Changed the code to set the Orion senate presidency election vote immediately when the player casts their vote,
 removing the ability to change your mind, but fixing some cases where it was not cast. 
Removed the line of code which was improperly clearing the "ignore senate law" information during turn processing,
 causing the ignore command to only stick for one turn. 
Fixed a bug where if there was more than one type of a proposed bill that the player can second (and probably vote on),
 then seconding that bill would prevent the player from seconding other bills of that type. 
Fixed a bug where clicking again on a bill or law would cause the details of it to disappear. 
Split senatelaws.txt table into two tables and added fields to proposals to affect relations for proposing, seconding
 or voting for the various actions which are aimed at a particular civ. 

NEW ORIONS
Corrected the logic of Orion Great White Smackdowns to remove multi-player synchronization problems (these were mostly
 introduced in the patch, but I think at least one of the smackdown triggers had this problem previously). 

PLANETS SCREEN
Added pulldown to specify the information in the last column. In addition to the current build items, it can list
 (one of) specials, economic slider percentages, classification, or military (orbitals, ground troops, bases). 
Added buttons to the Planets screen planet details to jump to their respective info panel. 
Added Econ AI check box to planets screen listing. 
Specials that are listed in the Planets screen planet details have the description of the special as the help text. 
Added magnate species to environmental preference lists. 
Moved the migration/colonize/outpost command buttons to the main panel on the Planets screen and removed the tabs.
Added sort by species/race(uses species number) and sort by empire. 
Planets whose military build queue has been locked by the player has the text of the contents displayed in light-blue. 

SHIPYARDS - FLEETS
Fixed a bug where the name of an unexplored star system would be shown as a task force's destination if the star was
 the only one that task force was going to. 
Fixed a bug where you were unable to scrap system ships of more than one design on the fleets screen. 

SHIP DESIGN
Fix Ship Design screen so that the pulldowns do not reset when attempting to start a second design. 
Fix Ship Design screen so that the equipment list scrolls when it exceeds the size of the panel. 
Added button to Ship Design screen for clearing out the currently selected ship design from all planetary queues but
 only if no money had been spent on building it yet. 

VICTORY SCREEN
Added a "History" tab to the Victory screen that displays graphs over the course of the game for the number of planets,
 population, tech level and victory points of all the known empires in the game (living or dead). 
Fixed a bug where victory conditions wouldn't be displayed properly on the Victory Conditions screen after loading
 a save game. 

TASK FORCE ASSEMBLY
On the Task Force Assembly screen, ships with colony pods in the reserves list now have the race name of the population
 inside the ship appended. 
Fixed a bug on the Task Force Assembly screen where changing the parameters to auto-build a task force would recreate
 the unit list of reserves. 
Fixed a bug on the Task Force Assembly screen where the task force name could not be highlighted. 
Task force assembly screen now remembers the last auto-build settings used.
Auto-build of task force will build the maximum size force and the fastest available ships
Detachment is changed to only one ship and Squadron is now 2-4 ships (otherwise the auto-build used to create the
 starting task forces puts two ships in the first task force built)
On the Task Force Assembly screen, pressing the Enter key while the text edit field for the task force name is active
 will trigger the button to accept the task force (assuming a valid task force has been built). 
On the Task Force Assembly screen, holding down shift while accepting a task force resets the task force builder and
 readies the UI for making another task force and will open the Ground Force Assembly screen if deploying ground forces
 to troop transports. 

GROUND FORCE ASSEMBLY
Added drop-down menu to the Ground Force Assembly screen to filter the units by species. 
Fixed a bug on the Ground Force Assembly screen where changing the parameters to auto-build a ground force would
 recreate the unit list of reserves and the army. 
Fixed a bug where opening the Ground Force Assembly screen would not clear the list of available unit types before
 recreating it. 
Fixed a bug on the Ground Force Assembly screen where the sizes of the lists of the army being deployed and the
 list of ground force reserves would not be set properly. 
Ground force assembly screen now remembers the last auto-build settings used.
Auto-build of ground forces will now mix the support units as much as possible.
On the Ground Force Assembly screen, pressing the Enter key while the text edit field for the ground force name
 is active will trigger the button to accept the ground force (assuming a valid ground force has been built). 
On the Ground Force Assembly screen, holding down shift while accepting a ground force resets the ground force builder
 and readies the UI for making another ground force. 

SPACE COMBAT
Fixed a problem selecting combat options when system ships were still in a system that had no colonies (but still
 had outposts) 
Modified military pre-combat AI so that it will defend a planet (if it has one) rather than attack in a system when
 outnumbered, even at holy war border policy. 
Corrected a problem which could hang the game in "resolving space combat" when there were multiple overlapping combats
 involving five or more civs. 
Fixed a bug in which only the stats for the first three orbitals were brought into combat and only those three
 orbitals would get killed.
Routine which applies damage after a hit will now consider the armor piercing mod.
Increased range and frequency of target acquisition logic for point defense weapons. 
Reworked retreat logic in space combat so that AI controlled ships retreat before they are completely destroyed.
Eliminated some redundant missile explosion message traffic in multi-player games.

BOMBARDMENT
Enabled user control of bombardment without controlling combat. Bombardment control will not be allowed if control
 of space combat was ceded to an ally (includes watching). (Removed from multi-player in 1.2.4)
Fixed bombardment so that ground forces take damage. 
Fixed a bug in which bombardment would leave the population species and race set on a region after killing all the
 inhabitants. This was showing up when viewing planets by dominant species on the planets screen, because the planet
 would still report a dominant species despite having no population.

GROUND FORCES/GROUND COMBAT
Removed code which degraded ground unit experience while in the delay box or the reserves, so that it is possible to
 get a unit higher than "experienced". 
Modified ground combat results so that capturing a planet also gives you a chance of acquiring a random tech from the
 other empire, based on the univalue of the captured planet AFTER ground combat completes. 

