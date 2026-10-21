# Privacy Policy

**Controller Tester**
Developer: Aaron Lowe
Last updated: October 21, 2026

This Privacy Policy describes how Controller Tester handles user information and your privacy rights when you use the app on iOS, iPadOS or macOS (Controller Tester for Mac).

## Summary

Controller Tester is offline by default. With one exception, described below, it does not collect, store, share, or transmit any personal information, and nothing it reads from your controllers leaves your device.

The exception is **Share CT**, optional global Reaction, Endless and Arcade Drills leaderboards. It is **off unless you turn it on** and shows you what it sends before the first byte leaves your phone. The app also offers controls to report a player for review or block that player's entries on your device. A report request leaves your device only when you choose it; the app says it was sent only when the service accepts it. You can request erasure of your server-held data. The only request the app may make after you turn Share CT off is a retry of an erasure you already requested.

## What the app does

Controller Tester uses Apple's GameController framework to read live input data from any game controller you connect to your iPhone, iPad or Mac, whether wired or via Bluetooth. On a Mac it can also read your keyboard, when you choose it as the input to test. It displays this data on your screen in real time so you can verify that buttons, sticks, triggers, and the directional pad are reporting correctly. All input data is held in memory only for as long as the app is open, and is discarded when you close the app.

## What we collect

Before Share CT is enabled, the app sends nothing. After you turn it off, a previously requested erasure may still retry until confirmed. Through the app, we do not collect, log, transmit, or store any of the following, whether the leaderboard is on or off:

- Your email, phone number, or password
- Your location
- Advertising identifiers (IDFA, IDFV, advertising ID)
- Crash reports, diagnostics, or usage analytics
- Controller serial numbers or hardware identifiers
- Your contacts, photos, or anything else on your device
- The input data the app reads from your controllers

There is no account to create and no sign-in anywhere in the app.

## Share CT, the optional leaderboard

Share CT publishes Reaction trial scores and separate per-drill Endless and Arcade rankings and Recent Scores to leaderboards that anyone can view on the web. It is **opt-in**. Before it sends anything, the app shows you a sheet listing every item below; if that list ever changes, the sheet is shown again and you are asked again.

When it is on, and only then, these are sent:

- **Every Reaction trial you finish while it is on**: your best time, your average, accuracy, score, the three individual attempt times, any misfires, and whether you used touch, a controller, or a keyboard
- **Every Endless or Arcade Drills run you finish after accepting the current agreement while it is on**: which drill and mode, points, lost lives, and whether you used touch, a controller, or a keyboard. Arcade also sends successful hits, whole enemies defeated and total opponents, whether you cleared the run, elapsed milliseconds, and perfect opponents. Endless points count successful active reactions; correct non-actions earn no points
- **Which controller you used, by name** — or "Touch"
- **A random player id made for this installation by the Share CT server**, and a random id for each score so that a retry is never counted twice
- **Your display name**, which you choose, and which may be blank
- **Your avatar**: which fighter, outfit, color and gear you picked. It's a short description, never a picture, and other players see it next to your name
- **The app version, the platform** (iOS, Mac, Windows, or Android) **and the device model**
- **If you choose Report on an eligible row**, the reported player's public player reference and the reason you select: spam, harassment, or inappropriate. The app may send this request even if the server cannot accept it; the app then shows failure.

That is the complete list sent by the app. Your display name, avatar, scores, controller name, and a short player-id suffix are available through the board. When the service provides an opaque public player reference, that reference is also available and is used to block or report a player. It is separate from the private credential that authorizes your requests. Recent Drills rows also have an opaque public reference distinguishing each run; it does not expose your private player id or token. The player id is random and is not derived from your device, Apple ID, or advertising identifier. The app does not ask for your email address or create an email account.

**Endless and Arcade Drills.** Each drill has separate Endless and Arcade rankings. Endless counts successful active reactions at 100% speed with three lives. Arcade ranks completed runs above partial runs, clears by time then points, and partial runs by whole enemies defeated then points and time. Arcade points are successful hits plus 5 per perfect opponent, 10 per three defeated enemies, and a clear-only time bonus of up to 300 points. Ranking points are separate from CT currency. All input devices compete on the same board for that drill and mode; device and platform are displayed as information, not separate rankings.

Existing Share CT players must accept the expanded agreement before any Endless or Arcade score submission or global drill-board request. After acceptance, newly finished runs are submitted automatically and appear in that drill and mode's public Recent Scores feed, including runs below your best and zero-point runs. Earlier local history is not uploaded when you accept the agreement or enroll. Older app versions and runs already queued under the earlier best-only agreement keep that scope and are not added to Recent Scores.

The server retains the latest 200 accepted runs per player across all drills and both modes for up to 90 days, whichever limit is reached first, plus a separate all-time best per player per drill and mode and at most 100 recent retry receipts per player in each mode. No per-reaction input traces are retained. The offline queue holds up to 200 finished runs, dropping the oldest if full. Expired runs are excluded from Recent Scores and deleted when the service starts, when new submissions or Recent reads occur, and during hourly cleanup. Progress can keep your last observed global standing on this device, with the time it was checked, so it can show that historical rank while offline.

**Avatar.** The avatar is a short description made only of ids: which fighter, which outfit, a color number or a limited bonus look (such as EX01), and any gear (for example `1:puppet-ronin:1:6:pirate-hat`, about 30 bytes). No picture is ever uploaded; each phone draws the headshot from art the app already includes, and the Share CT website draws the same headshot on its board. The avatar is simply the look you had the last time you used Share CT: the app sends it when you open the leaderboard, and only when it has changed. Nothing is sent while Share CT is off. The server keeps one avatar per player, so it appears on all of your rows, and deleting what you have sent erases it too. It shows what you chose to wear, which can include items bought with the app's CT points or earned in the app.

**Reports and blocks.** Report requires Share CT to be on and a board row with a public player reference. The app says a report was sent only after the server accepts it. Until the server supports reporting, the control may be unavailable or a submission will show failure. If accepted, a report is stored privately with the reporter, reported player, selected reason, submission time, and review state. It is not public, and sending it does not automatically remove anyone. The developer reviews accepted reports and decides whether to dismiss them or act on the reported player's public entries. Accepted reports remain in the private review list; no email alert or message about a report is sent anywhere. You can also report offensive board content directly at [lowekeyflexin@gmail.com](mailto:lowekeyflexin@gmail.com).

Block saves a player's public reference and display name on your device to hide that player's entries from your view of the board. You can undo a block in the app. Blocking does not send a request to the server and does not change ranks or what others see.

**Where it goes.** The leaderboard is a small server run on the developer's behalf by a volunteer, on their own hardware and home internet connection. It is not a commercial hosting provider and it is not covered by a service agreement. It is a beta, it may be unavailable at times, and the app says so wherever the board appears.

**Deleting what you have sent.** The app has a control in its leaderboard settings that erases your scores and player record from the live server. Deletion includes your all-time bests, retained Recent Scores runs, and retry receipts. If the server has accepted reports involving you, deletion also removes their live report and review records. The app discards runs still waiting to be sent and retries the erasure until the server confirms it if the server is initially unreachable.

**Backups.** The server is backed up nightly and backups are kept for fourteen days. A deletion takes effect on the live leaderboard and private review queue when confirmed; a copy may persist in a backup until those backups age out. Expired Recent Scores entries may likewise remain in a backup until it ages out.

## Third parties

The app contains no third-party SDKs, analytics tools, advertising networks, or tracking services, and it never has.

If you turn Share CT on, these parties are involved in delivering it:

- **The volunteer who operates the leaderboard server**, described above.
- **Cloudflare**, whose network carries requests to that server. As part of that, Cloudflare passes the server the IP address your request came from. The server uses it only to rate-limit abuse, holds it in memory, and **never writes it to its database or stores it alongside your scores.**

The volunteer and Cloudflare handle Share CT requests only after it has been enabled or while the app finishes a previously requested erasure.

## Network use

**Before you enable Share CT, the app makes no network requests at all.** It does not connect to any servers, ours or anyone else's. You can verify this by enabling Airplane Mode (or turning off Wi-Fi on a Mac) and using the app normally: every feature except the leaderboard works unchanged. Turning Share CT off stops board requests and score submissions; a previously requested erasure can still retry until confirmed.

With Share CT on, the app contacts only the leaderboard server described above, and only to register a player, send a finished Reaction trial, Endless run or Arcade run, read the board, rename you, submit a report you choose, or erase your data at your request.

## Bluetooth

The app requests Bluetooth permission only so that iOS or macOS can expose connected wireless game controllers to it through Apple's GameController framework. The app does not scan for, connect to, or communicate with any other Bluetooth devices. Bluetooth pairing of controllers is handled by the operating system itself, not by this app.

## Camera and photos

If you choose to photograph a controller, or pick a photo, to build a custom controller layout, the app uses that image only on your device to draw the layout. It is never uploaded, is not part of Share CT, and the app does not access your camera or photo library unless you start one of those actions. On a Mac, if you choose a folder for the app to import recordings from, the app reads only that folder, and only on your device.

## Children

The app contains no advertising. Before Share CT has ever been enabled, no player data is sent to the server. Turning it off later stops new board requests and score submissions but does not erase data already sent; use the erasure control for that.

Share CT is off unless it is deliberately turned on. If it is turned on, a chosen display name and Reaction, Endless or Arcade scores become publicly visible on the leaderboard. Choose a display name that does not identify you. A parent or guardian can turn the feature off and erase everything it has sent using the control described above.

## Your rights under GDPR, CCPA, and similar laws

**If Share CT has never been enabled**, the app has sent no player data to the server. If you used it and then turned it off, previously sent data remains until you request deletion.

**If you have used Share CT**, the data listed above may be held, and your rights apply to it:

- **Access** — your scores and name appear on the board, but accepted reports and review records are private. Contact us at the address below for questions about those records.
- **Correction** — you can change your display name in the app at any time.
- **Deletion** — the erase control removes your scores and player record, plus any accepted reports associated with you, from the live server, subject to the backup limits described above.
- **Portability** — public leaderboard data is served as plain JSON from the same public address as the board. Contact us for questions about private report records.
- **Objection and withdrawal of consent** — turn Share CT off. Board requests and score submissions stop immediately; a previously requested erasure may still retry until confirmed.

We do not sell personal information, share it for cross-context behavioural advertising, or use it for any automated decision-making or profiling. The legal basis for processing is your consent, given by turning the feature on after being shown the list of what it sends, and you may withdraw it at any time by turning it off.

If you have questions about how these regulations apply, you can contact us at the email below.

## Changes to this policy

If this policy changes, the updated version will be posted at the same URL. Substantive changes will be reflected in the "Last updated" date at the top.

## Contact

Questions about this policy, reports, or objectionable leaderboard content can be sent to: [lowekeyflexin@gmail.com](mailto:lowekeyflexin@gmail.com). If you email us, your address and message reach our support mailbox and are used to respond to your request.
