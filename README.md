Guardian Tales is a game designed to make you to log in at least once in the morning and once at night.
These macros do what you should be doing on your account for your first login and last logins of the day.
However, they do not do what you should be doing on your account every week, such as buying certain items that reset weekly from the Shop.
They also do not do anything that heavily desires manual input, such as Arena, Master Arena, Death Match, or Co-op Expedition.

# Instructions
1. Open Guardian Tales in MuMuPlayer (also known as MuMu, an Android emulator).
2. Click on "..." (Main menu) in the title bar.
3. Click on "Keyboard & Mouse/Gamepad".
4. Click on "Manage".
5. Click on "Import".
6. Click on "Local import".
7. Select the "com.kakaogames.gdts-Guardian Tales.json" file.
8. Optional: Click "More" then "Rename" to rename the key bind scheme.
9. Optional: Repeat steps 5-8 for the "com.kakaogames.gdts-Guardian Tales 2 Events.json" file.
10. Click on one of the newly added key bind schemes.
11. Click "Apply".

In step 7, you can select "com.kakaogames.gdts-Guardian Tales with Colosseum.json" instead if you want the compilation macros to do Colosseum for you.

In step 9, you can select "com.kakaogames.gdts-Guardian Tales 2 Events with Colosseum.json" instead if you want the compilation macros to do Colosseum for you.

The reason for step 9 is because having both versions will make it easier to edit the macros when 2 concurrent events with Event Points start and end.

# Usage
- For your login in the morning, press PageUp (pg up) on your keyboard after the first Attendance Check shows up on top of Heavenhold.
- For your login at night, Press PageDown (pg dn) on your keyboard after you see Heavenhold.

These keys can be remapped if you do not have them on your keyboard.

# Important Notes
- Some macros may require you to make changes for the compilation macro to function as intended.
  - If the compilation macro does not function as intended, it may waste resources on your account.
- If you move a macro out of order, it must be bundled with the `sleep X` (where X is a number) call that followed it.
- It is assumed that you do not move the macros out of their default order in the compilation macros.
  - Although most macros are theoretically modular, the compilation macros have not been tested with the macros in a different order.
- It is assumed that you have already unlocked everything.
  - The macros are not designed to handle unlocking animations, tutorials, story scenes, or the inability to Sweep.
  - It is recommended to reach the highest stage you can clear before Sweeping.
- It is assumed that you have not already done anything that the compilation macro will do before you run it.
- It is assumed that you do not have exceedingly long loading times.

# Macros
## Dailies: PageUp (pg up)
- A compilation of macros.
- Can be ran after the first Attendance Check shows up on top of Heavenhold.
  - The home screen must be Heavenhold (not My Room) before running.
### __Attendance: N1 (Numpad 1)__
- By default, clicks 6 times, going through 3 attendance checks.
  - For each additional attendance check, increase the number of loops in this macro by 2.
    - Increase the sleep time after `key_release N1` in `Dailies: PageUp (pg up)` by 3000.
  - For each package popup, at the end of this macro, call `key_press T`, then `key_release T`, and then `sleep 1500`.
    - Increase the sleep time after `key_release N1` in `Dailies: PageUp (pg up)` by 1500.
- __Modularity__
  - Not modular, should be the first macro ran in `Dailies: PageUp (pg up)`.
  - Can be removed from `Dailies: PageUp (pg up)`, but you will need to manually go through every attendance check and package popup.
    - To remove, erase `key_press N1`, `key_release N1`, and the following `sleep 9000` from `Dailies: PageUp (pg up)`.
- __Safety__
  - Unsafe, the compilation macro may not function as intended if this macro does not successfully go through every attendance check and package popup.
    - If this macro calls `key_press T`, but there is no package popup, it will click on the Hero button, making the compilation macro not function as intended.
### __Friend: N2 (Numpad 2)__
- Sends gifts to and receives gifts from friends.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Safe, assuming no prior macro fails.
### __Guild Attendance: N3 (Numpad 3)__
- Claims the attendance reward from your Guild.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, has not been tested on an account without a Guild.
### __Awakening Dungeon: N4 (Numpad 4)__
- Sweeps the Awakening Dungeon 3 times.
  - "Set to Remaining Free Entries" should already be enabled.
- __Modularity__
  - Modular if and only if it is placed before `Boosted Dungeon: N5 (Numpad 5)`, which must be placed before `Tetis: N6 (Numpad 6)`.
    - If the conditions above are satisfied, the bundle can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Safe, assuming no prior macro fails.
### __Boosted Dungeon: N5 (Numpad 5)__
- By default, Sweeps the Gold Dungeon 10 times.
  - "Set to Remaining Free Entries" should already be enabled.
  - You should have 100 Stamina.
- __Modularity__
  - Modular if and only if it is placed after `Awakening Dungeon: N4 (Numpad 4)` and before `Tetis: N6 (Numpad 6)`.
    - If the conditions above are satisfied, the bundle can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, see `Controls` section.
### __Tetis: N6 (Numpad 6)__
- Sweeps Tetis 3 times.
  - "Set to Remaining Free Entries" should already be enabled.
- __Modularity__
  - Modular if and only if it is placed after `Boosted Dungeon: N5 (Numpad 5)`, which must be placed after `Awakening Dungeon: N4 (Numpad 4)`.
    - If the conditions above are satisfied, the bundle can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Safe, assuming no prior macro fails.
### __Inn and Little Princess: N7 (Numpad 7)__
- Claims rewards from the Inn and the little princess' precious present.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Placing this macro too early may make it not claim the little princess' precious present, as the animation must progress enough for her precious present to be claimable.
- __Safety__
  - Unsafe, you must not pan or zoom in Heavenhold after loading in.
### __Vending Machine: N8 (Numpad 8)__
- Only works if you don't pan or zoom in Heavenhold after loading in.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, you must not pan or zoom in Heavenhold after loading in.
  - This macro has not been tested with insufficient Soul Points.
### __Shop: N9 (Numpad 9)__
- Buys the 2,000 free Gold and Level 15 Strengthening Hammer.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, see `Controls` section.
  - Clicks on the second item in the Resource shop, which may not be the 2,000 free Gold.
    - This is the case if you have not bought out the Coffee Grinders.
### __Mission Book: N0 (Numpad 0)__
- Claims mission rewards from the Daily tab.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro, although discouraged.
  - Recommended to be placed after `N1-9` to claim the reward for 1000 Activity Points.
### __Stamina/Coffee: * (Numpad Asterisk)__
- Spends 200 Gems to buy 100 Stamina.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro, although discouraged because it is susceptible to not function as intended.
  - Recommended to be placed last in `Dailies: PageUp (pg up)`.
    - Additionally, buying 100 Reserve Stamina now will help `__Dungeon: - (Numrow Minus or Hyphen or Dash)__` in `Nightlies: PageDown (pg dn)` run a Dungeon 15 times.
- __Safety__
  - Unsafe, will not function as intended if you have over 3000 Stamina or fewer than 200 Gems.
## Nightlies: PageDown (pg dn)
- A compilation of macros.
- Can be ran after you see Heavenhold.
  - Should be ran after the nightly Stamina mail gets sent, but can be used earlier.
- Plays `Friend: N2 (Numpad 2)`, `Inn and Little Princess: N7 (Numpad 7)`, and `Vending Machine: N8 (Numpad 8)` first.
### __Dungeon: - (Numrow Minus or Hyphen or Dash)__
- By default, Sweeps the Red Shard Dungeon 15 times.
  - You should have 150 Stamina.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, see `Controls` section.
### __Event - Roadmap: 6 (Numrow 6)__
- Claims Event Missions.
  - Does not exchange Event Points for rewards.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Replaces the event macro called in `Nightlies: PageDown (pg dn)`, or is called after it if there are 2 concurrent events with Event Points.
    - Call `sleep 16500` afterward.
- __Safety__
  - Unsafe, see `Controls` section.
### __Event - Heavenhold Marble: 7 (Numrow 7)__
- Claims Event Missions.
  - Does not use Event Points to roll dice.
  - Does not claim Lap Rewards or Monopoly Rewards.
- Identical to `Event - Bingo Machine: 8 (Numrow 8)`.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Replaces the event macro called in `Nightlies: PageDown (pg dn)`, or is called after it if there are 2 concurrent events with Event Points.
    - Call `sleep 16500` afterward.
- __Safety__
  - Unsafe, see `Controls` section.
  - Not tested yet.
### __Event - Bingo Machine: 8 (Numrow 8)__
- Claims Event Missions.
  - Does not use Event Points to draw numbers.
- Identical to `Event - Heavenhold Marble: 7 (Numrow 7)`.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Replaces the event macro called in `Nightlies: PageDown (pg dn)`, or is called after it if there are 2 concurrent events with Event Points.
    - Call `sleep 16500` afterward.
  - Not tested yet.
- __Safety__
  - Unsafe, see `Controls` section.
### __Event - Giant Capsule Machine: 9 (Numrow 9)__
- Claims Event Missions.
  - Does not use Event Points to collect capsules.
  - Does not exchange Empty Capsules for rewards.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Replaces the event macro called in `Nightlies: PageDown (pg dn)`, or is called after it if there are 2 concurrent events with Event Points.
    - Call `sleep 16500` afterward.
- __Safety__
  - Unsafe, see `Controls` section.
  - Not tested yet.
### __Event - Rift: 0 (Numrow 0)__
- Sweeps the Event Rift 5 times, exchanges Event Coins for both Event Rift Tickets, Sweeps the Event Rift 2 times, claims Event Missions, then claims Event Rewards.
  - "Set to Remaining Free Entries" should already be enabled.
  - Does not exchange Event Coins for other rewards.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Replaces the event macro called in `Nightlies: PageDown (pg dn)`, or is called after it if there are 2 concurrent events with Event Points.
    - Call `sleep 66000` afterward.
- __Safety__
  - Unsafe, see `Controls` section.
### __Mystery Evolution: + (Numpad Plus)__
- Performs Mystery Evolution 2 times.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
- __Safety__
  - Unsafe, your Mystery Evolution settings should already be set to only select 1 and 2 star equipment, and to exclude incompleted Knowledge or Collections.
### __Pass: / (Slash)__
- Claims Pass Missions then Pass Rewards for both the Guardian and Festival Passes.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro, although discouraged.
  - Recommended to be placed towards the end of `Nightlies: PageDown (pg dn)` so that you do not complete another mission after already claiming Pass Missions.
- __Safety__
  - Safe, assuming no prior macro fails.
### __Mailbox: = (Equals)__
- Claims mail from both the General and Manage categories.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro, although discouraged because it is susceptible to not function as intended.
  - Recommended to be placed last in `Dailies: PageUp (pg up)`.
- __Safety__
  - Unsafe, will not function as intended if clicking Receive All will make you exceed 3000 Stamina.
## Ads: Insert (ins)
- By default, not included in the `Dailies: PageUp (pg up)` compilation macro.
- By default, not included in the `Nightlies: PageDown (pg dn)` compilation macro.
- Can be ran after you see Heavenhold.
- Watches the ad for the additional Awakening Dungeon entry, but does not do the additional run for you, so you must do it manually.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro, although HIGHLY discouraged because it is susceptible to not function as intended.
  - Recommended to be placed last in either `Dailies: PageUp (pg up)` or `Nightlies: PageDown (pg dn)`.
    - Call `sleep 617000` afterward.
- __Safety__
  - Unsafe, every ad you get must be escapable with the back button, and must not send you to another app.
## Colosseum: Delete (del)
- By default, not included in the `Dailies: PageUp (pg up)` compilation macro.
- By default, not included in the `Nightlies: PageDown (pg dn)` compilation macro.
- Can be ran after you see Heavenhold.
- Attacks the third slot in Colosseum 5 times using the currently set team.
- On 1x speed, an attack may last up to 2 minutes, but this macro only waits for 1 minute 15 seconds before clicking Confirm.
  - If the macro clicks Confirm too early, it will not use 5 Colosseum Entry tickets.
  - Most attacks will not take that long even on 1x speed.
- __Modularity__
  - Modular, can be removed or placed anywhere before or after another modular macro.
  - Recommended to be placed between `Mission Book: N0 (Numpad 0)` and `Stamina/Coffee: * (Numpad Asterisk)` in `Dailies: PageUp (pg up)`.
    - Call `sleep 387000` afterward.
  - Recommended to be placed between `Pass: / (Slash)` and `Mailbox: = (Equals)` in `Nightlies: PageDown (pg dn)`.
    - Call `sleep 387000` afterward.
## Excavation Camp: End (end)
- By default, not included in the `Dailies: PageUp (pg up)` compilation macro.
- By default, not included in the `Nightlies: PageDown (pg dn)` compilation macro.
- Holds down ` ` (space) for 0.5 seconds.
  - Does not do anything else.
- __Modularity__
  - Only to be used manually.
- __Safety__
  - Safe.

# Controls
### __WASD__
- Movement.
### __I__
- Rapidly spams normal attack.
### __J__
- Rapidly spams Weapon Skill.
### __K__
- Rapidly spams 2nd skill.
### __1234__
- Chain Skills.
### __Q__
- Leader skill.
### __E__
- Co-op.
### __R__
- Co-op.
### __Shift__
- Map.
### __Tab__
- Cycle through DPS/HP/Heal in Colosseum.
### __[ (Left Bracket)__
- Place it on "Evolution Dungeon" or "Resource / Awakening Dungeon".
- Affects `Boosted Dungeon: N5 (Numpad 5)`.
### __] (Right Bracket)__
- Place it on "-10 Sweep" for the one you want.
- Affects `Boosted Dungeon: N5 (Numpad 5)`.
### __\ (Backslash)__
- Needs to be moved to the Equipment shop when the Event Shop becomes active or inactive.
- Affects `Shop: N9 (Numpad 9)`.
### __; (Semicolon)__
- Place it on "Myth Dungeon" or "Resource / Awakening Dungeon".
- Affects `Dungeon: - (Numrow Minus or Hyphen or Dash)`.
### __' (Apostrophe)__
- Place it on "-10 Sweep" for the one you want.
- Affects `Dungeon: - (Numrow Minus or Hyphen or Dash)`.
### __, (Comma)__
- By default, clicks on the first event in the Ongoing Events list.
  - Place it on the event if it is not first in the Ongoing Events list.
- If placed on the first event, place it on the bottom edge so that it does not click "Batch Exchange" (Roadmap) or "Check Event Missions!" (Heavenhold Marble, Bingo Machine).
### __. (Period or Dot)__
- By default, clicks on the second event in the Ongoing Events list.
  - Place it on the event if it is not second in the Ongoing Events list.
- Meant to be used when there are 2 concurrent events with Event Points.
  - Replace `,` (comma) with `.` (period or dot) in the event macro.
    - Revert this change after the double event period ends.
### __T__
- Clicks the area where the box next to "Do not display again today." on the package popup is.
  - The `Dailies: PageUp (pg up)` section explains how to use it.
### __` (Grave Accent)__
- Clicks the area where the in-game back button is.
  - Note that not every menu has this button, such as the Event Missions menu or in a stage.
  - The macros use it to go back.
  - The user is not expected to use it.
