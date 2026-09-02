# Privacy Policy — TurboWatch

**Last updated:** 30 August 2026

## The short version

TurboWatch collects nothing, transmits nothing, and contacts no server. Everything it
stores stays on your own computer.

That is the whole policy. The rest of this page is the detail behind it — what the extension
touches while it runs, and why none of it is kept.

## What TurboWatch stores

TurboWatch saves your settings using Chrome's `chrome.storage.local` API, on your device only:

- whether TurboWatch is switched on or off
- your global playback speed, and your forward/rewind seek steps
- per-site and per-domain speed and seek rules you create
- the list of sites where you have turned the extension off
- your theme, language and on-screen badge preferences

Every one of those is a setting you chose. TurboWatch never adds a site to that list on its
own: a site appears only because you pinned a rule to it, typed it in, or blocked it. The list
is not a history of where you have been — it has no page titles, no addresses beyond the site
name, no visit times, and no record of any site you did not deliberately configure.

This data is written and read only by TurboWatch, only on your machine. It is never uploaded,
backed up to a server, or synchronised to your other devices. Deleting the extension deletes it.

**Export and import.** Because nothing is synced, TurboWatch can save your settings to a JSON
file so you can keep a copy or move them to another computer. That file is written by your
browser to wherever you choose, and it contains your rules — including the list of sites you have
turned the extension off on. Nothing sends it anywhere; where it goes afterwards is entirely up
to you. Treat it as you would any other personal file.

## What runs on the pages you visit

To change the speed of a video on any site, TurboWatch has to be present on that site. There it
looks for `<video>` players, sets the speed and position of the ones it finds, and draws a small
badge when the speed changes. Nothing it does there is recorded, and nothing leaves your device.

**The site's name.** TurboWatch reads the hostname of your active tab (for example
`www.example.com`) purely to match it against the rules you have created. This happens in memory,
on your device, and the result is not stored beyond the rules you explicitly set up yourself.
The full address, its path, its query string and anything in it are never read, never sent and
never stored.

**Keyboard input.** TurboWatch listens for key presses on the pages it runs on, because a
keyboard shortcut is how you change speed or skip. Each press is compared against your own
shortcuts and then discarded in the same instant. It is never recorded, never counted, never
written to storage and never transmitted. Keys that are not one of your shortcuts are ignored
and passed straight on to the page. When your cursor is in a text box, TurboWatch checks only
the *kind* of element you are typing into — so that it can stand aside and let you type — and
never the words in it.

## Links you choose to open

The popup footer has two links that only ever open when you click them — TurboWatch never loads,
pings, or embeds anything from either address on its own, and no settings or page data are sent
along when they open:

- **Configure** opens your browser's own extension-shortcuts page, to rebind the keyboard
  shortcuts — `chrome://extensions/shortcuts` on Chrome, and the equivalent address on other
  Chromium browsers. If the browser refuses to open it, the popup shows you the address
  instead of navigating anywhere.
- **Support developer** opens `buymeacoffee.com/joelphilip5` in a new tab. Buy Me a Coffee is a
  third-party site with its own privacy practices, which this policy does not cover. This link is
  optional: turn off **Support developer** in the Site rules tab to remove it from the footer.

## What TurboWatch does not do

- **No network requests made by the extension itself.** Not for analytics, not for fonts, not
  for update checks, not for anything automatic. Its typefaces are bundled inside the extension
  package specifically so that opening the popup cannot reveal to anyone that you opened it. The
  only requests that ever happen are the two links above, and only if you click one yourself.
- **No tracking or analytics.** No telemetry, no usage statistics, no crash reporting, no
  advertising or fingerprinting identifiers.
- **No browsing history collection.** TurboWatch never records, stores, or transmits the pages
  you visit.
- **No keystroke logging.** Key presses are matched against your shortcuts and discarded. None
  is ever stored or sent.
- **No page content collection.** No text, images, audio, video, links, form fields, passwords,
  cookies or site storage are read or copied.
- **No account, no sign-in, no identifiers.** It never asks who you are.
- **No data sharing or selling.** There is no third party to share with; no data leaves your
  device.
- **No advertising, and no use of your data to profile you** — for creditworthiness, lending, or
  anything else. There is no data to use.
- **No remote code.** All code is contained in the published package. Nothing is downloaded or
  evaluated at runtime.

## Keeping and deleting your data

Your settings stay on your device until you remove them. There is no copy anywhere else, so
there is nothing to request, recall or delete from us.

- Remove a single rule or blocked site from the popup, and it is gone.
- Uninstalling TurboWatch removes everything it stored, including every rule and the blocklist.
  Chrome deletes the extension's local storage with the extension.
- A settings file you exported yourself is an ordinary file on your computer; delete it as you
  would any other.

## Permissions, and why each one exists

| Permission | Why it is needed |
|---|---|
| `storage` | To save your speed rules and preferences on your device. |
| `host_permissions: http://*/*`, `https://*/*` | Videos appear on any site, so the speed controller must be able to run on any site you choose to use it on. It reads a page's hostname only to decide which of *your* rules applies. |
| `scripting` | To activate the extension in tabs that were already open when you installed or updated it, so shortcuts work without reloading them. |
| `webNavigation` | To ask each frame in the current tab whether it contains a video, so the popup can show accurate status. It is not used to observe or record navigation. |
| `commands` | To register the keyboard shortcuts. |

The host permission is broad by necessity, not by ambition. It is what allows the
extension to work on any video site. It is not used to read page content, collect data, or
observe your browsing.

Where a narrower grant existed, it was taken. The `tabs` permission is deliberately **not**
requested, and TurboWatch asks for no others than the five above.

## Children's privacy

TurboWatch collects no data from anyone, of any age.

## Your rights

Data-protection laws such as the GDPR and the CCPA give you rights to see, correct, export or
delete the personal data a service holds about you. TurboWatch holds none, and no personal data
is collected, processed, sold or shared, so there is no request to make and no one to make it to.
Your settings are already in your hands: they are on your own device, visible in the popup,
exportable to a file, and deleted when you delete them.

## Changes to this policy

If this policy ever changes, the updated version will be published here and the date at the top
will be updated. Because the extension collects no data, any change is likely to be a
clarification rather than a change in practice.

## Contact & Support

If you have questions, feedback, or need support regarding this privacy policy or the extension, please use the **Support** tab on the TurboWatch Chrome Web Store listing.
