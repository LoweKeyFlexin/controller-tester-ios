# Controller Tester Support

A diagnostic iOS app for game controllers: buttons, sticks, triggers, d-pad, drift, reaction time. Built for the FGC.

Controller won't work? You're in the right place. Start here.

## Does my controller work?

iOS sees a controller through Apple's GameController framework. If iOS recognizes it as an Extended Gamepad, so does the app.

**Works natively:**

- PlayStation DualSense, DualSense Edge, DualShock 4
- Nintendo Switch Pro Controller and Joy-Cons
- Xbox Wireless Controllers (Series / Bluetooth models)
- 8BitDo pads in most modes
- Most generic Bluetooth gamepads
- Sticks and leverless boards set to **Switch** or **XInput** mode
- Keyboards, which covers fightsticks and leverless boards running in **keyboard mode**

**Doesn't work natively:** anything that leans on Sony's PS5 authentication chip. iOS only speaks that protocol for first-party DualSense and DualShock 4, so these won't show up on their own:

- Victrix Pro BFG and Pro KO (all PS5 / PS4 / PC modes)
- Qanba Obsidian and Sapphire
- Brook FGC converters and DualSense-impersonator boards

Don't give up on those. A **MAYFLASH Magic NS2 in macOS Mode** rescues most of them. More on that below.

## Top fixes

### It doesn't show up at all

1. **Switch the controller into a different mode.** Try **XInput / PC**, **PS4**, or **Keyboard** (most sticks and pads have a hardware mode switch). Those play nicest with iOS. PS5 mode is the usual culprit.
2. Pair through **iOS Settings, then Bluetooth**, not the app. Once iOS sees it, the app sees it.
3. Open the app and tap **Rescan** in the device-info panel.
4. Still nothing? Reach for a **MAYFLASH Magic NS2 set to macOS Mode.** It hands the controller to iOS in a form iOS will take, and it's the dependable rescue for pads that won't connect on their own. Confirmed with **Qanba** boards and **Brook-adapter** pads.

### It pairs but no buttons register

Tap **RAW** in the buttons-panel header. That shows every input element your controller reports. Press buttons one at a time and watch the cells.

- Cells light up but the glyphs are wrong? That's a mapping quirk. Send me a note (bottom of page). Usually a few lines to fix.
- If nothing lights up even in RAW, iOS isn't routing the controller's inputs to apps at all. Try **wired USB** instead of Bluetooth, or switch the board to **Switch / PC / XInput** mode. Common with Sony-licensed pads.

### It connects, then disconnects, over and over

A red banner at the top flags this. Nearly always it means a PS5 emulator board is waiting on a Sony console-side auth handshake that iOS can't give it, so it keeps cycling modes.

Three things to try, in order:

- **Wired USB instead of Bluetooth.** Plenty of controllers skip the auth dance entirely over USB.
- **Switch the firmware to Switch / PC / XInput.** Non-Sony modes work. Sony modes keep failing.
- **A MAYFLASH Magic NS2 in macOS Mode** (see above), the most reliable rescue here.

> On a Lightning iPhone, a wired controller needs Apple's **Lightning to USB 3 Camera Adapter (A1619)** with **external power** plugged in. The port alone doesn't supply enough.

### My fightstick pairs as a keyboard

That's fine. When a keyboard is connected and no gamepad is, the buttons panel shows live key presses automatically. The **Varmilo HA10** works this way. Keep it in keyboard mode for iOS; its gamepad mode reads as a mouse and surfaces nothing.

### How is reaction time measured?

Results show in milliseconds and in **frames at 60 fps**, the FGC standard, so the number means the same thing across devices. On ProMotion screens (iPad Pro, iPhone 13 Pro and later) input sampling runs up to 120 Hz. Good for A/B-ing two boards: if one adds 3 frames of latency, you'll see it.

## Using the Combo Editor

Combo Practice plays back a combo as a scrolling note highway and grades your timing against it. The **Combo Editor** is where you build or tune one. Open it from the Combo Practice screen with **Combo Editor**, or from a recording's menu.

**Record a combo.** Tap **REC**, then play the inputs on your controller. Each press drops a note on the timeline at the frame it landed. Tap **REC** again to stop. Prefer to build it by hand? The generated combos in the library are a good starting point to copy and edit.

**Read the timeline.** Time runs top to bottom; the yellow line is the playhead. Each note shows its input glyph (directions as arrows, buttons as your controller's face glyphs). The header reads out how many inputs and frames the combo is.

**Select a note.** Tap a note to select it — or step through notes with the **◀ ▶** buttons on your controller. The **Inspector** below fills in with that note's frame, hold length, and timing window.

**Select several at once.** Drag across empty timeline space to draw a selection box (a marquee) around a group of notes. Everything inside is selected together.

**Deselect.** Tap any empty part of the timeline to clear the selection.

**Move a note.** Drag a selected note up or down to shift it earlier or later; drag a whole selected group to move them together. For frame-exact nudges, use **−1f / +1f** in the Inspector.

**Set the timing window.** A note's window is how many frames **early** or **late** a press still counts as a hit. Loosen it for a lenient link, tighten it for a strict one — or leave **USE GLOBAL** on to follow the app-wide leniency.

**Trim and loop.** After a recording, drag the amber handles to trim off dead space at the ends. Mark a **loop** region to practice or re-record just one link instead of the whole combo.

**Save.** Tap **SAVE** to keep your changes. Saved combos show up in Combo Practice and in the library, ready to grade against.

## How combo grading works

Combo Practice grades you the way the game would, not against a metronome.

**Your timing is measured against your own hands.** Each input's window rides on your previous press. Roll the motion at your pace and time the button to your motion — that gap is what gets graded, with PERFECT / GREAT / GOOD tiers from each input's timing window (most bundled combos use windows measured from the real game).

**Motions are game-strict.** A special's arrows have to actually happen, in order, before the button counts:

- Rolling through a diagonal covers its neighbors — a clean down-forward roll satisfies the down and the forward steps.
- Down then forward with **no diagonal** fails the down-forward step, just like in-game.
- **Holding** a direction counts for the first step — holding crouch into a crouching attack is a real crouch. Holding one diagonal never shortcuts a whole motion; the rest of the arrows need real presses.
- A standing button when the combo starts crouching fails the crouch.

**The miss lands on what you actually missed.** If an arrow never happens, that arrow goes red at the line the moment its window passes. If you press the button but the motion wasn't complete, the move doesn't come out: the first missing arrow takes the miss, the correct direction lights up on the pad diagram, and the results list says which arrow dropped the motion. Arrows never cost score by themselves — the dropped attack carries the points.

**Misses are shown and felt, not squawked.** Hits play the punch sound; a miss deliberately plays no sound — you see the red note at the line, feel the miss haptic, and hear the *silence* where your hit should have landed. That's how most rhythm games do it, and it keeps a rough practice session from turning into a wall of error noises.

**The replay shows your hands.** After a failed run, the replay slows into each miss and draws the inputs you *actually pressed* as ghost markers at their true times, right next to the chart — so you can see a wrong arrow or an early button instead of guessing.

**Practicing a drop** loops just the move you missed. Until your first press, the rep waits for you — hesitating at the count-in doesn't fail anything. Drop it and it restarts in under a second; land it clean three times and the move locks in. If it ever parks on "ready", press anything to re-arm.

A few extras working in your favor: a real dragon-punch motion performed game-true always counts even if the chart spells it differently; simultaneous inputs (like forward + attack) grade as one moment so Bluetooth packet order can't split them; and if your device drops frames during a run, the app annotates the run instead of blaming your hands.

## Privacy

Controller Tester collects nothing. No analytics, no telemetry, no remote calls. Input data lives in memory only while the app is open, then it's gone. Full [Privacy Policy](./PRIVACY_POLICY).

## Contact

Bug reports and compatibility reports are the most useful thing you can send:

**lowekeyflexin@gmail.com**

When a controller won't work, more detail is better:

- Make and model (for example "Razer Wolverine V2 Pro" or "8BitDo Ultimate")
- Bluetooth or USB
- The mode it's in (PS5 / PS4 / Switch / XInput / PC)
- What the app shows: does it appear in the device list, do any buttons light up, what does RAW mode show
- iOS / iPadOS version and device model

This is a small project I keep up in spare time. Got a leverless board, stick, or oddball controller that isn't on the list? Send the info above. Adding a new controller class is usually a small change once I know what iOS reports for it.

Aaron Lowe
