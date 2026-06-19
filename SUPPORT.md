# Controller Tester Support

Diagnostic iOS app for testing game controllers: buttons, sticks, triggers, d-pad, drift, and reaction time. Built for the FGC.

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
- Keyboards, including fightsticks and leverless boards running in **keyboard mode**

**Doesn't work natively:** anything that leans on Sony's PS5 authentication chip. iOS only speaks that protocol for first-party DualSense and DualShock 4, so these don't show up on their own:

- Victrix Pro BFG and Pro KO (all PS5 / PS4 / PC modes)
- Qanba Obsidian and Sapphire
- Brook FGC converters and DualSense-impersonator boards

Don't give up on those. A **MAYFLASH Magic NS2 in macOS Mode** rescues most of them. More on that below.

## Top fixes

### It doesn't show up at all

1. **Switch the controller into a different mode.** Try **XInput / PC**, **PS4**, or **Keyboard** mode (most sticks and pads have a hardware mode switch). These have the best iOS compatibility; PS5 mode is the usual culprit.
2. Pair through **iOS Settings, then Bluetooth**, not the app. Once iOS sees it, the app sees it.
3. Open the app and tap **Rescan** in the device-info panel.
4. **Still nothing? Use a MAYFLASH Magic NS2 set to macOS Mode.** It re-presents the controller in a form iOS accepts and is the reliable rescue for pads iOS won't take natively. Confirmed with **Qanba** boards and **Brook-adapter** pads.

### It pairs but no buttons register

Tap **RAW** in the buttons-panel header. That shows every input element your controller reports. Press buttons one at a time and watch the cells.

- If cells light up but the glyphs are wrong, that's a mapping quirk. Send me a note (bottom of page); it's usually a few lines to fix.
- If nothing lights up even in RAW, iOS isn't routing the controller's inputs to apps. Try **wired USB** instead of Bluetooth, or switch the board to **Switch / PC / XInput** mode. This is common with Sony-licensed pads.

### It connects, then disconnects, over and over

A red banner at the top flags this. It almost always means a PS5 emulator board is waiting on a Sony console-side auth handshake that iOS can't give it, so it keeps cycling modes.

Three things to try, in order:

- **Wired USB instead of Bluetooth.** Many controllers skip the auth dance entirely over USB.
- **Switch the firmware to Switch / PC / XInput.** Non-Sony modes work; Sony modes will keep failing.
- **A MAYFLASH Magic NS2 in macOS Mode** (see above). The most reliable rescue for pads iOS won't take natively.

> On a Lightning iPhone, a wired controller needs Apple's **Lightning to USB 3 Camera Adapter (A1619)** with **external power** plugged into it, since the port alone doesn't supply enough.

### My fightstick pairs as a keyboard

That's fine. When a keyboard is connected and no gamepad is, the buttons panel shows live key presses automatically. The **Varmilo HA10** works this way. Put it in keyboard mode for iOS (its gamepad mode reads as a mouse and surfaces nothing).

### How is reaction time measured?

Results show in milliseconds and in **frames at 60 fps**, the FGC standard, so the number is comparable across devices. On ProMotion screens (iPad Pro, iPhone 13 Pro and later) input sampling runs up to 120 Hz. Handy for A/B-ing two boards: if one adds 3 frames of latency, you'll see it.

## Privacy

Controller Tester collects nothing. No analytics, no telemetry, no remote calls. Input data lives in memory only while the app is open. Full [Privacy Policy](./PRIVACY_POLICY).

## Contact

Bug reports and compatibility reports are the most useful thing you can send:

**lowekeyflexin@gmail.com**

When a controller won't work, more detail is better:

- Make and model (for example "Razer Wolverine V2 Pro" or "8BitDo Ultimate")
- Bluetooth or USB
- Which mode it's in (PS5 / PS4 / Switch / XInput / PC)
- What the app shows: does it appear in the device list? do any buttons light up? what does RAW mode show?
- iOS / iPadOS version and device model

This is a small project maintained in spare time. If you've got a leverless board, stick, or oddball controller that isn't on the list, send the info above. Adding a new controller class is usually a small change once I know what iOS reports for it.

Aaron Lowe
