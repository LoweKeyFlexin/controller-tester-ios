# Privacy Policy

**Controller Tester**
Developer: Aaron Lowe
Last updated: September 19, 2026

This Privacy Policy describes how Controller Tester handles user information and your privacy rights when you use the app on iOS or iPadOS.

## Summary

Controller Tester is offline by default. With one exception, described below, it does not collect, store, share, or transmit any personal information, and nothing it reads from your controllers leaves your device.

The exception is **Share CT**, an optional global reaction-time leaderboard. It is **off unless you turn it on** and shows you what it sends before the first byte leaves your phone. You can also report a player for review or block that player's entries on your device. You can erase your server-held scores, player record, and reports associated with you. The only request the app may make after you turn Share CT off is a retry of an erasure you already requested.

## What the app does

Controller Tester uses Apple's GameController framework to read live input data from any game controller you connect to your iOS device, whether wired or via Bluetooth. It displays this data on your screen in real time so you can verify that buttons, sticks, triggers, and the directional pad are reporting correctly. All input data is held in memory only for as long as the app is open, and is discarded when you close the app.

## What we collect

With Share CT off, the app sends nothing. Through the app, we do not collect, log, transmit, or store any of the following, whether the leaderboard is on or off:

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
- **A random player id made for this installation by the Share CT server**, and a random id for each score so that a retry is never counted twice
- **Your display name**, which you choose, and which may be blank
- **The app version, the platform** (iOS, Mac, Windows, or Android) **and the device model**
- **If you choose Report**, the reported player's public player reference and the reason you select: spam, harassment, or inappropriate

That is the complete list sent by the app. Your display name, scores, controller name, a short player-id suffix, and an opaque public player reference are available through the board. The public reference is used to block or report a player; it is separate from the private credential that authorizes your requests. The player id is random and is not derived from your device, Apple ID, or advertising identifier. The app does not ask for your email address or create an email account.

**Reports and blocks.** Report is available only after you turn Share CT on. The server accepts a report into a private review queue before the app says it was sent. A report records the reporter, reported player, selected reason, submission time, and review state. It is not public, and sending it does not automatically remove anyone. The developer reviews reports and decides whether to dismiss them or act on the reported player's public entries. The server sends a private email alert to the review owner with a report ID and a link to the authenticated review screen; the player details and reason are read from the review record, not included in the alert. The recipient address is private and configured on the server. A failed email delivery leaves the accepted report in the queue for retry. You can also report offensive board content directly at [lowekeyflexin@gmail.com](mailto:lowekeyflexin@gmail.com).

Block saves a player's public reference and display name on your device to hide that player's entries from your view of the board. You can undo a block in the app. Blocking does not send a request to the server and does not change ranks or what others see.

**Where it goes.** The leaderboard is a small server run on the developer's behalf by a volunteer, on their own hardware and home internet connection. It is not a commercial hosting provider and it is not covered by a service agreement. It is a beta, it may be unavailable at times, and the app says so wherever the board appears.

**Deleting what you have sent.** The app has a control in its leaderboard settings that erases your scores and player record from the live server. The server also removes reports, review records, and unsent email alerts associated with you, whether you submitted a report or someone reported you. The app discards runs still waiting to be sent and retries the erasure until the server confirms it if the server is initially unreachable. A private alert email already delivered to the review owner may remain in that mailbox after server erasure; it contains only a report ID and review link, without a name, player reference, or reason. Contact us at the address below to ask about a delivered alert.

**Backups.** The server is backed up nightly and backups are kept for fourteen days. A deletion takes effect on the live leaderboard and private review queue when confirmed; a copy may persist in a backup until those backups age out.

## Third parties

The app contains no third-party SDKs, analytics tools, advertising networks, or tracking services, and it never has.

If you turn Share CT on, these parties are involved in delivering it:

- **The volunteer who operates the leaderboard server**, described above.
- **Cloudflare**, whose network carries requests to that server. As part of that, Cloudflare passes the server the IP address your request came from. The server uses it only to rate-limit abuse, holds it in memory, and **never writes it to its database or stores it alongside your scores.**
- **Private email delivery**, used only to alert the review owner after the server accepts a report. The alert contains a report ID and authenticated review link, not the reporter's email address or player details.

These services are involved only when Share CT has been enabled or the app is finishing a previously requested erasure.

## Network use

**Before you enable Share CT, the app makes no network requests at all.** It does not connect to any servers, ours or anyone else's. You can verify this by enabling Airplane Mode and using the app normally: every feature except the leaderboard works unchanged. Turning Share CT off stops board requests and score submissions; a previously requested erasure can still retry until confirmed.

With Share CT on, the app contacts only the leaderboard server described above, and only to register a player, send a finished trial, read the board, rename you, submit a report you choose, or erase your data at your request. The server, not the app, sends private review alerts.

## Bluetooth

The app requests Bluetooth permission only so that iOS can expose connected wireless game controllers to it through Apple's GameController framework. The app does not scan for, connect to, or communicate with any other Bluetooth devices. Bluetooth pairing of controllers is handled by iOS itself, not by this app.

## Children

The app is suitable for all ages and contains no advertising. With Share CT off, no data is collected from anyone, children included.

Share CT is off unless it is deliberately turned on. If it is turned on, a chosen display name and reaction scores become publicly visible on the leaderboard. Choose a display name that does not identify you. A parent or guardian can turn the feature off and erase everything it has sent using the control described above.

## Your rights under GDPR, CCPA, and similar laws

**With Share CT off**, Controller Tester collects no personal data at all, so there is nothing to access, correct, delete, port, or restrict.

**With Share CT on**, the data listed above is held, and your rights apply to it:

- **Access** — your scores and name appear on the board, but accepted reports and review records are private. Contact us at the address below for questions about those records.
- **Correction** — you can change your display name in the app at any time.
- **Deletion** — the erase control removes your scores, player record, and associated reports from the live server, subject to the backup and delivered-email limits described above.
- **Portability** — public leaderboard data is served as plain JSON from the same public address as the board. Contact us for questions about private report records.
- **Objection and withdrawal of consent** — turn Share CT off. Board requests and score submissions stop immediately; a previously requested erasure may still retry until confirmed.

We do not sell personal information, share it for cross-context behavioural advertising, or use it for any automated decision-making or profiling. The legal basis for processing is your consent, given by turning the feature on after being shown the list of what it sends, and you may withdraw it at any time by turning it off.

If you have questions about how these regulations apply, you can contact us at the email below.

## Changes to this policy

If this policy changes, the updated version will be posted at the same URL. Substantive changes will be reflected in the "Last updated" date at the top.

## Contact

Questions about this policy, reports, or objectionable leaderboard content can be sent to: [lowekeyflexin@gmail.com](mailto:lowekeyflexin@gmail.com). If you email us, your address and message reach our support mailbox and are used to respond to your request.
