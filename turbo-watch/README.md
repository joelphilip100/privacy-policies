# Privacy Policy — TurboWatch

**Last updated:** 30 August 2026

## The short version

TurboWatch collects nothing, transmits nothing, and contacts no server. Everything it
stores stays on your own computer.

## What TurboWatch stores

TurboWatch saves your settings using Chrome's `chrome.storage.local` API, on your device only:

- whether TurboWatch is switched on or off
- your global playback speed, and your forward/rewind seek steps
- per-site and per-domain speed and seek rules you create
- the list of sites where you have turned the extension off
- your theme, language and on-screen badge preferences

This data is written and read only by TurboWatch, only on your machine. It is never uploaded,
backed up to a server, or synchronised to your other devices. Deleting the extension deletes it.

**Export and import.** Because nothing is synced, TurboWatch can save your settings to a JSON
file so you can keep a copy or move them to another computer. That file is written by your
browser to wherever you choose, and it contains your rules — including the list of sites you have
turned the extension off on. Nothing sends it anywhere; where it goes afterwards is entirely up
to you. Treat it as you would any other personal file.

## Links you choose to open

The popup footer has two links that only ever open when you click them — TurboWatch never loads,
pings, or embeds anything from either address on its own, and no settings or page data are sent
along when they open:

- **Configure** opens Chrome's own `chrome://extensions/shortcuts` page, to rebind the keyboard
  shortcuts.
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
- **No account, no sign-in, no identifiers.** It never asks who you are.
- **No data sharing or selling.** There is no third party to share with; no data leaves your
  device.
- **No remote code.** All code is contained in the published package. Nothing is downloaded or
  evaluated at runtime.

## Permissions, and why each one exists

| Permission | Why it is needed |
|---|---|
| `storage` | To save your speed rules and preferences on your device. |
| `host_permissions: <all_urls>` | Videos appear on any site, so the speed controller must be able to run on any site you choose to use it on. It reads a page's hostname only to decide which of *your* rules applies. |
| `scripting` | To activate the extension in tabs that were already open when you installed or updated it, so shortcuts work without reloading them. |
| `webNavigation` | To ask each frame in the current tab whether it contains a video, so the popup can show accurate status. It is not used to observe or record navigation. |
| `commands` | To register the keyboard shortcuts. |

The `<all_urls>` permission is broad by necessity, not by ambition. It is what allows the
extension to work on any video site. It is not used to read page content, collect data, or
observe your browsing.

## Sites you visit

TurboWatch reads the hostname of your active tab (for example `www.example.com`) purely to
match it against the rules you have created. This happens in memory, on your device, and the
result is not stored beyond the rules you explicitly set up yourself.

## Children's privacy

TurboWatch collects no data from anyone, of any age.

## Changes to this policy

If this policy ever changes, the updated version will be published here and the date at the top
will be updated. Because the extension collects no data, any change is likely to be a
clarification rather than a change in practice.

## Contact & Support

If you have questions, feedback, or need support regarding this privacy policy or the extension, please use the **Support** tab on the TurboWatch Chrome Web Store listing.
