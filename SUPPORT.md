# Controller Tester — Support

Diagnostic iOS app for testing game controllers — buttons, analog sticks, triggers, d-pad, drift, and reaction time. Built for the fighting game community.

## Contact

For bug reports, controller compatibility issues, or questions, email:

**lowekeyflexin@gmail.com**

When emailing about a controller that isn't working, the more detail the better:

- Controller make and model (e.g. "Razer Wolverine V2 Pro", "8BitDo Ultimate")
- Connection method (Bluetooth or USB)
- Which mode the controller is in (PS5 / PS4 / Switch / XInput / PC, etc.)
- What you see in the app (does it appear in the device list? do any buttons light up?)
- iOS or iPadOS version
- Device model (iPhone 16 Pro Max, iPad Pro M4, etc.)

## Quick troubleshooting

### My controller doesn't show up at all

1. **Pair the controller through iOS Settings first**, not the app. Go to **Settings → Bluetooth**, put the controller in pairing mode, and tap it to pair. Once iOS sees it, the app sees it.
2. If pairing fails: make sure the controller is in the right mode. Many fighting-game controllers have a hardware switch for PS / Switch / Xbox / PC. **Nintendo Switch mode or XInput / PC mode** has the highest compatibility with iOS.
3. After pairing in Settings, open Controller Tester and tap **Rescan** in the device-info panel.

### My controller pairs but no buttons register

- Tap **RAW** (in the buttons panel header) to show every input element your controller reports. Press buttons one at a time and watch which cells light up — this tells you whether iOS sees inputs at all.
- If RAW mode shows nothing either, your controller is connected but iOS isn't routing its inputs to apps. This typically happens with Sony-licensed controllers (like the Victrix Pro BFG) where iOS requires PS5-style authentication that isn't standardized for apps. **Try wired USB instead of Bluetooth**, or switch the controller to Nintendo Switch / PC / XInput mode if it supports one.

### On iPad, my left analog stick and D-pad are swapped

A known iPadOS bug affects some PlayStation controllers — the framework swaps which input it routes as the analog stick vs the digital d-pad. The app has a built-in workaround:

- Tap the **L↔D · OFF** button just above the on-screen D-pad. It changes to **L↔D · ON** in green, and the inputs swap back to their correct positions.
- iPhone users typically don't see this issue.

### My controller keeps disconnecting and reconnecting

A red warning banner appears at the top of the app when this is detected. This usually means the controller is a PS5 emulator board waiting for a Sony console-side authentication response that iOS can't provide — the controller switches modes and cycles connections.

**Workarounds:**

- Connect via wired USB instead of Bluetooth. Most controllers behave differently over USB and often skip authentication entirely.
- Switch the controller's firmware mode to **Nintendo Switch**, **PC**, or **XInput** if your controller has that option. Sony-licensed boards in PS5 / PS4 modes will keep failing on iOS; non-Sony modes work fine.
- Use a **MAYFLASH Magic NS2 adapter set to macOS Mode.** This is the most reliable fix for controllers iOS won't recognize natively. The adapter re-presents the controller in a form iOS accepts, so its inputs surface in the app. Confirmed working with **Qanba** controllers and controllers running through a **Brook adapter**.

### What controllers are supported?

Anything iOS recognizes through Apple's GameController framework as an Extended Gamepad — including:

- PlayStation DualSense, DualSense Edge, DualShock 4
- Nintendo Switch Pro Controller, Joy-Cons
- Xbox Wireless Controllers (Series, Bluetooth-enabled models)
- 8BitDo controllers (most modes)
- Most generic Bluetooth gamepads
- Most arcade sticks and leverless controllers in **Switch mode** or **XInput mode**

Controllers that depend on Sony's PS5 authentication chip (Victrix Pro BFG, Hori Fighting Edge PS5, Brook FGC adapters, etc.) generally don't work on iOS because iOS doesn't speak Sony's auth protocol. Use those over wired USB or switch them to a non-PS5 mode if possible.

For controllers that still won't connect — including **Qanba** boards and pads on a **Brook adapter** — a **MAYFLASH Magic NS2 set to macOS Mode** is the confirmed workaround: it re-presents the controller in a form iOS accepts. See "My controller keeps disconnecting and reconnecting" above.

### My fightstick / leverless board pairs as a keyboard, not a controller

That's fine — the app supports this. When no gamepad is connected but a keyboard is, the buttons panel automatically shows live key presses. Boards like the Varmilo HA10 work this way on iOS; they pair as a keyboard rather than as a gamepad, and the app surfaces every key press as a button cell.

### How is "reaction time" measured?

The reaction test shows results in both milliseconds and **frames** (the fighting-game standard, calculated at 60 fps so it's comparable across devices). On ProMotion displays (iPad Pro, iPhone 13 Pro and later), input sampling runs at up to 120 Hz so the measurement is as low-latency as the hardware allows.

The test is also useful for comparing controllers — if one board adds 3 frames of latency vs another, you'll see it.

## Privacy

Controller Tester does not collect, store, or transmit any user data. All input data is held in memory only while the app is open. See the full [Privacy Policy](./PRIVACY_POLICY).

## Roadmap

This is a small project maintained in spare time. Bug reports and controller-compatibility reports are the most helpful thing you can send. Features are added as time allows.

If you have a leverless board, arcade stick, or unusual controller that doesn't appear on the tested list, email a short note and the troubleshooting info above — adding support for a new controller class is usually a small change once we know what iOS reports for that device.

— Aaron Lowe
