# Privacy Policy — TurboWatch

**Last updated:** 23 September 2026

## The short version

TurboWatch does not send your browsing activity, settings, or usage data to the developer or
any third party. It has no analytics, advertising, account system, or remote service. It does
process limited information locally so it can control HTML5 videos, and it stores the settings
you choose in Chrome's local extension storage.

## Information processed on your device

TurboWatch locally processes the following information only to provide its visible features:

- **The current tab's URL and hostname.** Chrome supplies the active tab's URL to the extension.
  TurboWatch immediately reduces it to a lowercase hostname (for example,
  `www.example.com`) so it can select a site or domain rule. The URL, path, query string, page
  title, and visit time are not logged or stored. Only a hostname you deliberately add, pin, or
  block becomes a saved setting.
- **HTML5 video elements.** The content script finds `<video>` elements, including videos in
  frames and in Shadow DOM web components (open or closed; closed ones are reached through
  Chrome's `chrome.dom.openOrClosedShadowRoot`, which needs no additional permission), and reads
  or changes limited player state such as whether a video is playing, playback rate, current
  playback position, and duration. It observes page changes
  to find players added later. It does not copy or inspect the video or audio itself.
- **Keyboard events.** TurboWatch checks key presses against its playback shortcuts. It also
  checks whether focus is in an editable control, including one inside a web component, so it
  can leave typing alone. It reads only the control's type and editability, never its value. Keystrokes are not logged, counted, stored, or transmitted.

This processing happens inside your browser. TurboWatch does not transmit this information to
the developer or to any external server.

## Settings stored on your device

TurboWatch uses `chrome.storage.local` to save:

- whether the extension is on or off;
- global playback speed and forward/rewind seek steps;
- per-site and per-domain speed and seek rules you create;
- hostnames you block;
- theme, language, on-screen badge, and support-link preferences; and
- an internal settings-format version used to migrate settings safely after updates.

These settings are not synced by TurboWatch, uploaded, sold, or shared. A saved hostname is
configuration you deliberately created, not an automatically generated browsing history.
Chrome normally removes an extension's local storage when the extension is uninstalled.

## Export and import

You can export your settings to a JSON file and later merge or restore that file. The backup can
contain site/domain rules and blocked hostnames. Your browser saves it to a location you choose;
TurboWatch does not upload it. Anyone who can access the file may be able to see those settings,
so store and share it as you would any other private file. Deleting the exported file is your
responsibility.

## Links and third parties

TurboWatch makes no automatic requests to third-party servers. Its fonts and program code are
bundled with the extension. It fetches language files only from its own installed package.

The popup contains links that act only when you click them:

- **Configure** attempts to open your Chromium browser's extension-shortcuts page.
- **Support developer** opens `https://buymeacoffee.com/joelphilip5`. You can hide this link in
  TurboWatch's settings. Buy Me a Coffee receives the ordinary information your browser sends
  when you visit a website and applies its own privacy policy. TurboWatch does not attach your
  settings or browsing data to the link.

Once you leave TurboWatch, the destination site or browser page is outside this policy.

## What TurboWatch does not do

- No telemetry, analytics, crash reporting, advertising, or fingerprinting.
- No developer-operated server, account, sign-in, or cross-device sync.
- No sale, rental, or sharing of user data.
- No browsing-history log and no storage of page paths, queries, titles, or visit times.
- No collection of page text, images, media, links, form contents, passwords, cookies, or site
  storage.
- No remote code. All executable code is included in the published extension package.

## Permissions

| Permission | Why it is needed |
|---|---|
| `storage` | Saves the settings listed above in local extension storage. |
| Host access to `http://*/*` and `https://*/*` | Lets the video controller work on HTML5 video sites and in embedded frames. It is also what allows Chrome to provide a tab URL, which is reduced to a hostname for rule matching. |
| `scripting` | Activates TurboWatch in eligible tabs that were already open when it was installed or updated. |
| `webNavigation` | Lists frames in the active tab so the popup can ask each frame whether it contains a video. TurboWatch does not subscribe to, store, or transmit navigation events. |
| `commands` | Registers user-configurable playback-speed shortcuts. |

TurboWatch does not request the `tabs` permission. Broad HTTP/HTTPS host access is necessary for
its disclosed purpose of controlling videos on sites chosen by the user; it is not used for
profiling or monitoring browsing.

## Retention and your choices

Settings remain in `chrome.storage.local` until you change/reset them or uninstall TurboWatch.
You can remove individual rules and blocked hosts, reset all settings with **Reset everything**
on the popup's Settings tab, or uninstall the extension. The developer has no server-side copy and therefore cannot retrieve,
correct, export, or delete settings on your behalf. Exported backup files remain until you delete
them yourself.

## Security and incidents

TurboWatch reduces risk by keeping settings and processing on-device, shipping no remote code,
and making no automatic external network requests. No software or storage mechanism can be
guaranteed completely secure. If a vulnerability or incident materially changes the risks or
data practices described here, the developer will investigate, take reasonable remediation
steps, update this policy and the Chrome Web Store disclosures as appropriate, and provide notice
through an available product, store-listing, or project channel when notice is warranted.

Do not include passwords, payment details, backup contents, or other sensitive information in a
public support report.

## Children

TurboWatch is not directed to children and does not knowingly transmit personal information from
users of any age to the developer.

## Future features, paid plans, and policy changes

This policy describes the version available on its last-updated date; it does not grant permission
for future data collection. If a future release introduces accounts, cloud sync, analytics, paid
plans, licensing, or another practice that changes how information is handled, TurboWatch will
update this policy and the Chrome Web Store disclosures before or when that change takes effect
and will provide any notice or consent required by law and store policy.

TurboWatch does not currently sell a paid plan or process payments. If payments are introduced,
the checkout provider—not TurboWatch—should process card details under its own privacy policy;
the applicable seller, price, recurring terms, cancellation, and refund terms will be disclosed
before purchase. This paragraph does not announce or promise a paid offering.

## Chrome Web Store Limited Use

TurboWatch's use of information received from Chrome APIs complies with the Chrome Web Store User
Data Policy, including the Limited Use requirements. Information is used only to provide and
maintain the extension's user-facing video-control features and is not transferred for advertising,
profiling, creditworthiness, or lending purposes.

## Contact and support

For privacy questions or support, use the **Support** tab on TurboWatch's Chrome Web Store listing
or the project's GitHub issue tracker. Avoid posting sensitive information publicly.
