# Privacy Policy

**Controller Tester**
Developer: Aaron Lowe
Last updated: September 11, 2026

This Privacy Policy describes how Controller Tester handles user information and your privacy rights when you use the app on iOS or iPadOS.

## Summary

Controller Tester is offline by default. With one exception, described below, it does not collect, store, share, or transmit any personal information, and nothing it reads from your controllers leaves your device.

The exception is **Share CT**, an optional global reaction-time leaderboard. It is **off unless you turn it on**, it shows you the exact list of what it sends before the first byte leaves your phone, and you can erase everything it has sent at any time. While it is off, the app makes no network requests at all.

## What the app does

Controller Tester uses Apple's GameController framework to read live input data from any game controller you connect to your iOS device, whether wired or via Bluetooth. It displays this data on your screen in real time so you can verify that buttons, sticks, triggers, and the directional pad are reporting correctly. All input data is held in memory only for as long as the app is open, and is discarded when you close the app.

## What we collect

With Share CT off, nothing. We do not collect, log, transmit, or store any of the following, whether the leaderboard is on or off:

- Your email, phone number, or password
- Your location
- Advertising identifiers (IDFA, IDFV, advertising ID)
- Crash reports, diagnostics, or usage analytics
- Controller serial numbers or hardware identifiers
- Your contacts, photos, or anything else on your device
- The input data the app reads from your controllers

There is no account to create and no sign-in anywhere in the app.

## Share CT, the optional leaderboard

Share CT publishes reaction-test scores to a leaderboard that anyone can view on the web. It is **opt-in**. Before it sends anything, the app shows you a sheet listing every item below; if that list ever changes, the sheet is shown again and you are asked again.

When it is on, and only then, these are sent:

- **Every Reaction trial you finish while it is on**: your best time, your average, accuracy, score, the three individual attempt times, any misfires, and whether you used touch, a controller, or a keyboard
- **Which controller you used, by name** — or "Touch"
- **A random player id made for this phone**, and a random id for each score so that a retry is never counted twice
- **Your display name**, which you choose, and which may be blank
- **The app version, the platform** (iOS, Mac, Windows, or Android) **and the device model**

That is the complete list. The display name and the scores are **public**: anyone who visits the leaderboard can see them. The player id is random and is not derived from your device, your Apple ID, or anything that identifies you personally. No email address is involved, because there are no accounts.

**Where it goes.** The leaderboard is a small server run on the developer's behalf by a volunteer, on their own hardware and home internet connection. It is not a commercial hosting provider and it is not covered by a service agreement. It is a beta, it may be unavailable at times, and the app says so wherever the board appears.

**Deleting what you have sent.** The app has a control in its leaderboard settings that erases your scores and your player record from the server. It also discards any runs still waiting to be sent from your phone. The app keeps retrying that erase until the server confirms it, so it completes even if the server is unreachable when you ask.

**Backups.** The server is backed up nightly and backups are kept for fourteen days. A deletion takes effect immediately on the live leaderboard; a copy may persist in a backup until those backups age out.

## Third parties

The app contains no third-party SDKs, analytics tools, advertising networks, or tracking services, and it never has.

If you turn Share CT on, two parties are necessarily involved in delivering it:

- **The volunteer who operates the leaderboard server**, described above.
- **Cloudflare**, whose network carries requests to that server. As part of that, Cloudflare passes the server the IP address your request came from. The server uses it only to rate-limit abuse, holds it in memory, and **never writes it to its database or stores it alongside your scores.**

Neither is involved in any way while Share CT is off.

## Network use

**With Share CT off, the app makes no network requests at all.** It does not connect to any servers, ours or anyone else's. You can verify this by enabling Airplane Mode and using the app normally: every feature except the leaderboard works unchanged.

With Share CT on, the app contacts only the leaderboard server described above, and only to register a player, send a finished trial, read the board, rename you, or erase your data at your request.

## Bluetooth

The app requests Bluetooth permission only so that iOS can expose connected wireless game controllers to it through Apple's GameController framework. The app does not scan for, connect to, or communicate with any other Bluetooth devices. Bluetooth pairing of controllers is handled by iOS itself, not by this app.

## Children

The app is suitable for all ages and contains no advertising. With Share CT off, no data is collected from anyone, children included.

Share CT is off unless it is deliberately turned on. If it is turned on, a chosen display name and reaction scores become publicly visible on the leaderboard. Choose a display name that does not identify you. A parent or guardian can turn the feature off and erase everything it has sent using the control described above.

## Your rights under GDPR, CCPA, and similar laws

**With Share CT off**, Controller Tester collects no personal data at all, so there is nothing to access, correct, delete, port, or restrict.

**With Share CT on**, the data listed above is held, and your rights apply to it:

- **Access** — everything held about you is what the app sent and what the leaderboard shows. There is nothing additional held out of sight.
- **Correction** — you can change your display name in the app at any time.
- **Deletion** — the erase control removes your scores and your player record from the server, subject to the backup window described above.
- **Portability** — the leaderboard's data is served as plain JSON from the same public address as the board.
- **Objection and withdrawal of consent** — turn Share CT off. It stops sending immediately, and nothing is sent while it is off.

We do not sell personal information, share it for cross-context behavioural advertising, or use it for any automated decision-making or profiling. The legal basis for processing is your consent, given by turning the feature on after being shown the list of what it sends, and you may withdraw it at any time by turning it off.

If you have questions about how these regulations apply, you can contact us at the email below.

## Changes to this policy

If this policy changes, the updated version will be posted at the same URL. Substantive changes will be reflected in the "Last updated" date at the top.

## Contact

Questions about this policy can be sent to: lowekeyflexin@gmail.com
