# Patch notes

## alpha 0.8.2 (2026-11-09)
- New: Tower ranking. On the main screen, TOWER RANKING shows the best floors of all players (top 20, and your own place). Choose a name there; when a Tower run ends, your best floor and time are sent (a score waits in the save if there is no name or no internet). Only the name you type, the floor, the time, the game version and a random code of your device are sent. A floor that is impossible for the time played is refused.
- New: Tower return point. A Tower run is saved every 10 seconds, when a floor falls, when you leave the app and when you leave through the pause window. If the game reloads or you close the app, CONTINUE TOWER appears on the main screen (with the floor, the time and the class) and brings you back a few seconds before: floor, time, level, skills, orbs, health and coins. The enemies of the floor start again. Dying, or starting a new Tower, deletes it. A continued Tower counts for the ranking.
- New main screen layout: Shop, Pets (the collection), How to play and Ranking are icons at the sides of PLAY. The caster and the two foes stand higher, and the Look button and the version text follow the bottom of the screen, so nothing hides behind them on tall phones.

## alpha 0.8.1 (2026-11-09)
- Fix: the game could reload by itself on an iPhone during a Tower run (the browser took the graphics away). The cause was the power orbs that drop when a Tower boss falls: 120 pictures were made at once (+165 MB of graphics memory and a freeze of several seconds). They now use 3 shared pictures, tinted and moved. Nothing else changes in how they look or work.
- Fix: the pictures of the previous run (another stage, class or boss) were kept in graphics memory when a new run started, so a long session grew. They are now freed when a new run replaces the scene, and made again while the loading screen is up.
- Coin and orb animations use 16 stored frames instead of 24.

## alpha 0.8 (2026-11-08)
- New menu. PLAY opens a flow: mode (Traditional or Tower), a short text about the mode with OK, the stage list (Traditional), the character, the companion and START. Every step has Back. The Tower button left the main screen: the Tower is a mode now. QUICK START repeats the last mode, stage and class. A loading screen covers the moment the game reloads for another stage or class and for Play again.
- The stage list shows the rules of each open stage (a harder start, a better pay, walls) and a tip.
- Character screen: a card for each class, with its picture, description, starting skill, health, speed and pickup range, and the looks of the chosen class; a locked look says how to unlock it.
- New stage 1-2, Frozen Reach (opens by clearing stage 1-1 with any class): snow, five new enemies (Rime Lurker, Frost Imp, Hoar Dart, Glacier Brute and the Sleet Archer, which keeps its distance and throws ice shards), and low stone walls with snow that block you, the enemies and the enemy shots, so you can hide behind them. It starts with the enemies of minute 2 of stage 1, so it pushes you to buy shop upgrades first, and it pays 1.5x coins and account XP and a bigger victory bonus.
- New boss, Kaldrun the Glacier Warden (stage 1-2 only): he marks the line of a dash on the ground, and a dash that hits a wall breaks it and stuns him for 2 seconds (he takes 30% more damage then); below half health a broken wall also bursts into ice shards.
- New look for the Dark Knight, the Rime Sovereign, earned by clearing stage 1-2 with him. Beating a stage with a class is saved per class.
- XP: from level 35 each level needs 15% more XP than the one before (it was 23%), so the levels past 40 no longer stall.

## alpha 0.7.4 (2026-11-08)
- Steadier game on iPhones: the effects, pets, pickups, joystick and arrows are no longer redrawn every frame; each picture is made once and only moved, turned and faded. Redrawing shapes every frame filled the memory of iPhone browsers until the page reloaded by itself. A 40 minute test on an iPhone ran without a reload, with flat memory and 60 frames per second even with 100 enemies on screen. Nothing was removed or made easier: the same effects, enemies and damage.
- Smoother on phones with a sharp screen: the game is drawn at its own size and the picture is stretched to the screen, instead of drawing every pixel of the screen. On a 1440x3120 phone this gave 10-20% more frames per second, far fewer slow frames and about 75 MB less memory; an iPhone gained 10-15%. Computers keep the screen's own size. Only the picture changes, the game is the same.
- No sound for now: music and effects are off on every device and their buttons are hidden. On iPhone browsers the game engine (Godot 4.3) leaks memory with every sound until the page reloads by itself after 12-17 minutes; the fix comes with a newer engine version.
- Campaign boss fight: when the boss arrives the horde thins to 35 enemies (the farthest ones leave) and fewer enemies come during the fight, and the boss has 15% less health. The Tower does not change.
- Test builds only: a long play bot (soak test) that plays by itself for an hour and reports frame rate and memory, with a black box of the last 30 seconds if the page crashes.

## alpha 0.7.3.1 (2026-11-06)
- Fix: in the automatic low quality mode a skill effect (the Ash Nova ring, for example) could be left on the screen, following the character, instead of fading away. Effects are now always cleared when they end.
- Fix: XP orbs stopped dropping in a part of the map after you had left many orbs behind in another one (the new orb merged into a far one). Now the limit counts the orbs around you; when there are too many around you a new orb flies to you at once, and orbs left far away never stop new ones from dropping.

## alpha 0.7.3.1 (2026-11-06)
- Fix: in the automatic low quality mode a skill effect (the Ash Nova ring, for example) could be left on the screen, following the character, instead of fading away. Effects are now always cleared when they end.
- Fix: XP orbs stopped dropping in a part of the map after you had left many orbs behind in another one (the new orb merged into a far one). Now the limit counts the orbs around you; when there are too many around you a new orb flies to you at once, and orbs left far away never stop new ones from dropping.

## alpha 0.7.3 (2026-11-06)
- Pets: one pet only. The pet skills no longer add more pets: the single pet grows stronger with the levels and gives you a small bonus. Only one collectible companion can be equipped.
- Cone skills now fire toward the direction you are walking, not at the nearest enemy.
- Boss fight: the stage clock stops while the boss is alive, so the stage ends when he is beaten. A boss that you run from for 3 minutes gets 25% stronger (and again every minute), with a warning on the screen.
- Tower and menus: bigger test jumps for testers, and the pictures of the enemies and the ground are made while the menu is shown, so the first seconds of a run are smoother.
- Smoother game on weak phones: the fire and lightning patches on the ground, the enemies, the gems and the ground are drawn from stored pictures, and many small jobs were made lighter. On the phones we measured the frame rate of the heavy moments went from about 15 to about 30 frames per second.
- Automatic low quality: if the game stays under 36 frames per second for 30 seconds, it switches itself to a lighter look (no death bursts, no wobble, fewer gem pictures, half of the ground patches not drawn, smaller pictures, effects redrawn every second frame) and remembers it on that device. The game is NOT easier: the same enemies, the same damage, the same XP.
- Fire trails of the Ash Summoner last 2 seconds and hit harder, so the total damage is the same with fewer patches on screen.
- The Rime Cleave of the Dark Knight hits everything that steps into its fan, and the whole fan is drawn. The Storm Ring of the Shaman is easier to see. The Tower coin counter shows what the floors paid.
- Test builds only: an Auto test button in the debug panel plays 12 heavy situations by itself and reports the frame rate of the device.

## alpha 0.7.2 (2026-11-06)
- Every class now has eight active skills to choose from and holds four of them, like the eight passives.
- Shaman: fights with a new Sky Bolt; Chain Spark and the Ash Totem are his now, plus Rime Jolt and Storm Ring. The Spirit Wolf is a choice, not the start.
- Ash Summoner: new Soul Siphon and Ashen Hound.
- Dark Knight: an ice look with new names (Rime Cleave, Winter Gale, Frost Spikes) and the same numbers; new Bone Ward, Blood Pool, Wyrm's Breath, Winter Pulse and Risen Thrall.
- The sword sweep now always starts at the character, at any level.
- The XP bar takes the whole width, with the Pause and Help buttons under it.
- Performance: enemies, XP gems and the ground are now drawn once into pictures and reused (at 120 enemies the frames cost about a third as much and the draw calls fell from 3500 to 850 on a PC); lightning trails of the Shaman last half as long and hit twice as hard per tick; fewer gems on screen (they merge); far-away crates are removed.
- Skills are smaller: Wide Flames gives +10% area per level (was 15%), and the big radii of the area skills and their combinations were reduced (a maxed area skill no longer covers the whole screen width).

## alpha 0.7.1 (2026-11-05)
- Tower power orbs: pickups that make you stronger only inside the Tower: Power (damage), Vitality (max health) and Swiftness (move speed). Each boss defeated drops one of each, and a random orb drops near you every minute. Each kind has a limit per run. The campaign and the skills are untouched.
- Tower pacing: enough kills call the next boss early, so strong players climb faster. The first floors are gentler (first boss at 5 minutes, with less health and damage) and the climb gets very hard past floor 6. Enemies also get faster with time.
- General balance after more than 1100 bot runs: Ash Summoner a bit stronger (more health and Cinder Bolt damage; Ash Nova, Ember Orbit and Chain Spark hit harder). Shaman weaker (wolf, health, healing and shield). Dark Knight weaker (health and Cleaving Strike). Vessa and Haskor hurt less, and there are fewer enemies during the boss fight.
- Smaller download: images that were not part of the game are gone from the web build.

## alpha 0.7 (2026-11-05)
- Classes: choose your class in a new Class window (button on the start screen). Two new playable classes besides the Ash Summoner:
  - Shaman: leads a Spirit Wolf pack, with Mending Spring (heals) and Stone Ward (shield). Looks: Storm Shaman, and Forest Shaman at account level 2.
  - Dark Knight: tougher, no ranged attack; fights with Cleaving Strike, Whirling Blades and Grave Slam. Has his own look.
  - Each class has its own skills, level-up cards and new skill combinations.
- Tower mode: an endless climb with a boss every 4 minutes; each boss defeated is a floor, and enemies get stronger with floors and time. Records for best floor, time and damage.
- Tower rewards: coins and account XP only for floors beyond your best of the season (no XP for time). Titles at floors 5, 10 and 20, and a Tower-only look, the Tower Champion (floor 10).
- Share result: after a Tower run, copy a text with your result to send to friends.
- Play Again restarts the Tower right away.

## alpha 0.6 (2026-11-05)
- Looks: choose your character's look in a new Looks window (button under the character on the start screen); locked looks show the account level that opens them.
- Backup: a code with your whole progress that you can copy and paste on another device (Backup button on the start screen, with a Paste button).
- Sound: separate Music and Effects switches (start screen and pause window); lower volume and a limiter so loud moments no longer crackle.
- End of a run: mobs defeated and XP collected, with a NEW RECORD mark when you beat your best.
- The game pauses by itself when you leave the app, and Android's Back button closes windows and opens the pause window.
- The pause window is bigger, and the end-of-run window scrolls when it has a lot to show.

## alpha 0.5 (2026-11-04)
- Account level (1 to 20): every run gives account XP, also when you quit from the pause window; each new level pays coins, and some levels unlock new looks.
- Looks: a Look button on the start screen; first new look is the Ash Mage.
- Companions: enemies drop souls (glowing marked enemies drop rare ones); collect them to unlock and level up companions that fight at your side. New Collection window to see and equip them.
- Lighter start screen, and the health bar at the top is gone (the one over the character stays).
- The first three minutes are a bit harder.

## alpha 0.4 (2026-11-04)
- Coin shop: six permanent upgrades bought with saved coins, on the start screen.
- Retro sound effects and music, with a Sound on/off button (start screen and pause window).
- Health bar over the character, which blinks red when hit.
- Main Menu button after a run and Quit to menu in the pause window.
- Shields drop more often; the boss now appears at 12:30.

## alpha 0.3 (2026-11-04)

**Gameplay**
- A big banner and a red flash announce the boss when it appears, with a line of its own for each of the four bosses.
- Ash Totem: the cooldown now starts when the totems vanish, so there are always gaps between them; all the totems you are allowed plant at once, spread around you. A pulse takes at most 40% of a regular mob's health (three pulses to kill one); the boss takes full damage.

**Fixes**
- Level-up cards no longer grow wider than the screen when a skill description is long.
- The HUD timer is centered on the bars and the coin counter ends where they end.

## alpha 0.2 (2026-11-04)

**Visuals**
- New graphics across the whole game: the caster, the enemies, the four bosses, the ground, crates, urns, items, XP gems, skill effects and the icons of all 16 skills.
- New mobs in the horde: the Bog Lurker (marsh amphibian) in place of the beetle, the Ash Imp, and the ember wasp in place of the small "rocket" mob. The golem now has flames.
- New interface: health and XP bars, level-up cards with icons, an animated start screen, and an edge vignette that pulses red at low health.
- Pause now opens a window with time, coins, a short list of your skills and a Continue button.

**Gameplay**
- A smoother horde: the number of enemies rises gradually, without sudden jumps in the middle of a run.
- Enemies left far behind are moved back around the player, so mobs keep appearing when you run in one direction.
- The horde is thinner during the boss fight.
- Auto-aimed skills (bolt, cone, spark, rain and familiars) pick the boss first when it is in reach.
- More food drops from crates and urns when health is very low.

**Skills**
- Flame Cone: follows the player, lasts longer and is cast more often.
- Magnet Totem (combination): the totem pulses pull the XP gems inside their radius.
- Ash Totem: less damage at high levels and in the combination.
- Ashen Heart: now gives +20 max health in points (it used to be 20% of the base health).

**Other**
- A level-up card shows the partner skill's icon when a combination is possible.
