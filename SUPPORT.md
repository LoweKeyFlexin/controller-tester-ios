# Controller Tester — Support

Diagnostic iOS app for testing game controllers — buttons, sticks, triggers, d-pad, drift, and reaction time. Built for the FGC.

If a controller won't work, you're in the right place. Start here.

## Does my controller work?

iOS sees a controller through Apple's GameController framework. If iOS recognizes it as an Extended Gamepad, the app does too.

**Works natively:**

- PlayStation DualSense, DualSense Edge, DualShock 4
- Nintendo Switch Pro Controller and Joy-Cons
- Xbox Wireless Controllers (Series / Bluetooth models)
- 8BitDo pads in most modes
- Most generic Bluetooth gamepads
- Most sticks and leverless boards set to **Switch** or **XInput** mode

**Doesn't work natively:** anything that leans on Sony's PS5 authentication chip. iOS only speaks that protocol for first-party DualSense and DualShock 4, so these don't show up on their own:

- Victrix Pro BFG and Pro KO (all PS5 / PS4 / PC modes)
- Qanba Obsidian and Sapphire
- Brook FGC converters and DualSense-impersonator boards

Don't give up on those — see the rescues below.

**On iPad:** PlayStation pads work, but iPadOS swaps the left stick and d-pad. There's a one-tap fix. Details below.

## Top fixes

### It doesn't show up at all

1. Pair through **iOS Settings → Bluetooth first**, not the app. Once iOS sees it, the app sees it.
2. Set the controller's hardware mode switch to **Nintendo Switch** or **XInput / PC** — those have the best iOS compatibility. PS5 / PS4 modes are the usual culprit.
3. Open the app and tap **Rescan** in the device-info panel.

### It pairs but no buttons register

Tap **RAW** in the buttons-panel header. That shows every input element your controller reports. Press buttons one at a time and watch the cells.

- Cells light up but the glyphs are wrong → that's a mapping quirk; send me a note (bottom of page) and it's usually a few lines to fix.
- Nothing lights up even in RAW → iOS isn't routing the controller's inputs to apps. Try **wired USB** instead of Bluetooth, or switch the board to **Switch / PC / XInput** mode. This is common with Sony-licensed pads.

### iPad: left stick and d-pad are swapped

Known iPadOS bug on some PlayStation controllers — the framework crosses up which input is the stick and which is the d-pad. Built-in fix: tap **L↔D · OFF** just above the on-screen d-pad. It flips to **L↔D · ON** in green and the inputs land where they should. iPhone users rarely see this.

### It connects, then disconnects, over and over

A red banner at the top flags this. It almost always means a PS5 emulator board is waiting on a Sony console-side auth handshake that iOS can't give it, so it keeps cycling modes.

Three things to try, in order:

- **Wired USB instead of Bluetooth.** Many controllers skip the auth dance entirely over USB.
- **Switch the firmware to Switch / PC / XInput.** Non-Sony modes work; Sony modes will keep failing.
- **MAYFLASH Magic NS2 in macOS Mode.** This is the reliable rescue for controllers iOS won't take natively — the adapter re-presents the controller in a form iOS accepts. Confirmed working with **Qanba** boards and pads on a **Brook adapter**.

> On a Lightning iPhone, a wired controller needs Apple's **Lightning to USB 3 Camera Adapter (A1619)** with **external power** plugged into it — the port alone doesn't supply enough.

### My fightstick pairs as a keyboard

That's fine. When a keyboard is connected and no gamepad is, the buttons panel shows live key presses automatically. The **Varmilo HA10** works this way — put it in keyboard mode for iOS (its gamepad mode reads as a mouse and surfaces nothing).

### How is reaction time measured?

Results show in milliseconds and in **frames at 60 fps** — the FGC standard, so the number is comparable across devices. On ProMotion screens (iPad Pro, iPhone 13 Pro and later) input sampling runs up to 120 Hz. Handy for A/B-ing two boards: if one adds 3 frames of latency, you'll see it.

## Privacy

Controller Tester collects nothing. No analytics, no telemetry, no remote calls. Input data lives in memory only while the app is open. Full [Privacy Policy](./PRIVACY_POLICY).

## Contact

Bug reports and compatibility reports are the most useful thing you can send:

**lowekeyflexin@gmail.com**

When a controller won't work, more detail is better:

- Make and model (e.g. "Razer Wolverine V2 Pro", "8BitDo Ultimate")
- Bluetooth or USB
- Which mode it's in (PS5 / PS4 / Switch / XInput / PC)
- What the app shows — does it appear in the device list? do any buttons light up? what does RAW mode show?
- iOS / iPadOS version and device model

This is a small project maintained in spare time. If you've got a leverless board, stick, or oddball controller that isn't on the list, send the info above — adding a new controller class is usually a small change once I know what iOS reports for it.

— Aaron Lowe
