## Instructions
1. Open Guardian Tales in MuMu.
- Click on "..." (Main menu) in the title bar.
- Click on "Keyboard & Mouse/Gamepad".
- Click on "Manage".
- Click on "Import".
- Click on "Local import".
- Select the "com.kakaogames.gdts-Guardian Tales.json" file.
- Click on the newly added key bind scheme.
- Optional: Click "More" then "Rename" to rename the key bind scheme.
- Click "Apply".

## Important Notes
- Read everything so changes you want to make to the macros don't break anything.
- Read the `Controls` section (at the bottom) so you don't brick your account.
- The macros below are safe (won't waste your resources) unless stated otherwise.
  - It is assumed that you have not already done anything that the compilation macro will do before you run one.
  - It is assumed that although most macros are modular, you do not move them out of their default order.
  - It is assumed that you do not have excessively long loading times.

# Macros
## Dailies: PageUp (pg up)
- Should be used after the reset.
- Can be pressed from the attendance screen.
- The home screen must be Heavenhold (not My Room).
- If you add instructions to a macro below, do math and increase the amount of time this compilation macro sleeps for after pressing the respective key.
### __Attendance: N1 (Numpad 1)__
- Currently set to go through 3 attendance screens.
  - For each additional attendance screen, increment the number of loops by 2.
  - For each popup, increment the number of loops by 1. Alternatively, program the macro to click "Do not display again today."
  - Alternatively, set the number of loops to a large number so you never have to worry about it.
- __Modularity__
  - Can be removed, but you will need to manually go through every attendance screen and popup.
### __Friend: N2 (Numpad 2)__
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Guild Attendance: N3 (Numpad 3)__
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Awakening Dungeon: N4 (Numpad 4)__
- "Set to Remaining Free Entries" must already be enabled.
- __Modularity__
  - Must be placed before `Boosted Dungeon: N5 (Numpad 5)`, which must be placed before `Tetis: N6 (Numpad 6)`.
  - The bundle can be placed anywhere before or after another modular macro.
### __Boosted Dungeon: N5 (Numpad 5)__
- Unsafe; see "Controls" section.
- "Set to Remaining Free Entries" must already be enabled.
- Runs the Gold Dungeon by default.
- __Modularity__
  - Must be placed after `Awakening Dungeon: N4 (Numpad 4)`, and must be placed before `Tetis: N6 (Numpad 6)`.
  - The bundle can be placed anywhere before or after another modular macro.
### __Tetis: N6 (Numpad 6)__
- "Set to Remaining Free Entries" must already be enabled.
- __Modularity__
  - Must be placed after `Boosted Dungeon: N5 (Numpad 5)`, which must be placed after `Awakening Dungeon: N4 (Numpad 4)`.
  - The bundle can be placed anywhere before or after another modular macro.
### __Inn and Little Princess: N7 (Numpad 7)__
- Only works if you don't pan or zoom in Heavenhold after loading in.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
  - Placing it too early may make it finish running before the little princess' animation progresses enough for her gift to be claimable.
### __Vending Machine: N8 (Numpad 8)__
- Only works if you don't pan or zoom in Heavenhold after loading in.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Shop: N9 (Numpad 9)__
- Unsafe; see "Controls" section.
- Unsafe; will buy Coffee Grinders instead of the 2,000 free Gold if you haven't already bought out the Coffee Grinders.
  - Change "click 650,350" to "click 900,350" if you don't want to buy out the Coffee Grinders. Change every "click 650,350" to "click 900,350" in `Ads: Insert (ins)` if you plan on using it.
- Buys the 2,000 free Gold and Level 15 Strengthening Hammer.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Mission Book: N0 (Numpad 0)__
- __Modularity__
  - Must be placed after N1-9 to claim the reward for 1000 Activity Points.
### __Stamina/Coffee: * (Numpad Asterisk)__
- Spends 200 Gems to buy 100 Stamina.
- __Modularity__
  - Can be placed anywhere before or after another modular macro, but is unrecommended.
  - Recommended to be placed last in `Dailies: PageUp (pg up)` because it will break the macro if you have over 3000 stamina.
  - Not recommended to be placed in `Nightlies: PageDown (pg dn)` because buying 100 Reserve Stamina now will help `__Dungeon: - (Numrow Minus or Hyphen or Dash)__` run a dungeon 15 times.
## Nightlies: PageDown (pg dn)
- Should be used after the nightly coffee gift gets sent, but can be used earlier.
- Can be pressed from Heavenhold.
- If you add instructions to a macro below, do math and increase the amount of time this compilation macro sleeps for after pressing the respective key.
- Plays `Friend: N2 (Numpad 2)`, `Inn and Little Princess: N7 (Numpad 7)`, and `Vending Machine: N8 (Numpad 8)` first.
### __Dungeon: - (Numrow Minus or Hyphen or Dash)__
- Unsafe; see "Controls" section.
- Runs a dungeon 15 times.
- Runs the Red Shard Dungeon by default.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Event - Roadmap: 6 (Numrow 6)__
- Unsafe; see "Controls" section.
- Not tested, but should work.
- Call `sleep 12000` afterward.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Event - Heavenhold Marble: 7 (Numrow 7)__
- Unsafe; see "Controls" section.
- Not tested, but should work.
- Call `sleep 12000` afterward.
- Identical to `Event - Bingo Machine: 8 (Numrow 8)`.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Event - Bingo Machine: 8 (Numrow 8)__
- Unsafe; see "Controls" section.
- Not tested, but should work.
- Call `sleep 12000` afterward.
- Identical to `Event - Heavenhold Marble: 7 (Numrow 7)`.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Event - Giant Capsule Machine: 9 (Numrow 9)__
- Unsafe; see "Controls" section.
- Not tested, but should work.
- Call `sleep 12000` afterward.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Event - Rift: 0 (Numrow 0)__
- Unsafe; see "Controls" section.
- Sweeps 5 runs, exchanges for both Event Rift Tickets, sweeps 2 runs, claims missions, then claims rewards.
- Does not exchange for other items.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
### __Pass: + (Numpad Plus)__
- Claims missions then rewards for both the Guardian and Festival Passes.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
  - Should be placed at the end so that you don't complete another mission after already claiming pass missions and rewards.
### __Mailbox: / (Slash)__
- Claims mail from both categories.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
  - Recommended to be placed last in `Dailies: PageUp (pg up)` because it will break the macro if clicking "Receive All" will make you exceed 3000 Stamina.
### __Mystery Evolution: = (Equals)__
- Unsafe; before running, set your Mystery Evolution settings to only select 1 and 2 star equipment, and to exclude incompleted Knowledge or Collections.
- Performs Mystery Evolution 2 times.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
## Ads: Insert (ins)
- Unsafe; you probably shouldn't use this if you already manually played an ad. Additionally, every ad on your MuMu instance must be escapable with the back button.
- Not included in the `Dailies: PageUp (pg up)` compilation macro by default.
- Not included in the `Nightlies: PageDown (pg dn)` compilation macro by default.
- Can be pressed manually from Heavenhold.
- Although it does the ad for the Awakening Dungeon, it will not do the additional run for you, so you must do it manually.
- __Modularity__
  - Can be placed anywhere before or after another modular macro, but is highly unrecommended.
  - Recommended to be placed at the end of a compilation macro.
  - Call `sleep 617000` after if you put this in a compilation macro.
## Colosseum: Delete (del)
- Not included in the `Dailies: PageUp (pg up)` compilation macro by default.
- Not included in the `Nightlies: PageDown (pg dn)` compilation macro by default.
- Does 5 attacks.
  - On 1x speed, an attack may last up to 2 minutes, but this macro only waits for 1 minute 15 seconds before clicking "Confirm". If the macro clicks "Confirm" too early, it will not use 5 Colosseum Entry tickets.
- Can be pressed manually from Heavenhold.
- __Modularity__
  - Can be placed anywhere before or after another modular macro.
  - Recommended to be placed at the end of both compilation macros.
  - Call `sleep 387000` after if you put this in a compilation macro.
## Excavation Camp: End (end)
- Not included in the `Dailies: PageUp (pg up)` compilation macro by default.
- Not included in the `Nightlies: PageDown (pg dn)` compilation macro by default.
- Holds down ` ` (space) for 0.5 seconds.
  - Does not do anything else.
- __Modularity__
  - Only to be used manually.
## Controls
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
- Place it on "-10   Sweep" for the one you want.
- Affects `Boosted Dungeon: N5 (Numpad 5)`.
### __\ (Backslash)__
- Needs to be moved to the Equipment shop when the Event Shop becomes active or inactive.
- Affects `Shop: N9 (Numpad 9)`.
### __; (Semicolon)__
- Place it on "Myth Dungeon" or "Resource / Awakening Dungeon".
- Affects `Dungeon: - (Numrow Minus or Hyphen or Dash)`.
### __' (Apostrophe)__
- Place it on "-10   Sweep" for the one you want.
- Affects `Dungeon: - (Numrow Minus or Hyphen or Dash)`.
### __, (Comma)__
- Defaulted to click on the first event in the ongoing events list.
  - Place it on the event if it is not first in the ongoing events list.
### __. (Period or Dot)__
- Meant for if there is more than 1 ongoing event in the ongoing events list.
  - Replaces `,` (comma) in the event macro. Remember to change it back after the double event period ends.
### __` (Grave Accent)__
- The macros use it to go back.
  - The user is not expected to use it.
- Clicks the area where the in-game back button is (not to be confused with Android's back button).
  - Note that not every menu has this button, such as the Event Missions menu or in a stage.
