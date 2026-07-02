---
title: "MSG & EML Email Viewer — Privacy Policy"
date: 2026-07-02
url: "/msg-eml-viewer/privacy/"
showtoc: true
tocopen: true
ShowReadingTime: false
ShowWordCount: false
ShowShareButtons: false
ShowBreadCrumbs: false
hidemeta: true
---

_Last updated: 2 July 2026_

> **TL;DR** — Everything happens locally in your browser. The extension does
> **not** collect, transmit, sell, or share any data. No analytics, no tracking,
> no servers operated by the developer.

## What the extension does

**MSG & EML Email Viewer** intercepts `.msg` and `.eml` email file downloads
from sites you configure and opens them in a built-in viewer instead of saving
them to disk. To do this, it:

- Reads the download URL and, when needed, re-fetches the file using your
  existing browser session so it can be parsed.
- Parses the email (subject, sender, recipients, date, body, attachments)
  **entirely on your device**.
- Stores your preferences (URL patterns, on/off toggle, theme, and per-email
  "load remote images" choice) using the browser's local storage.

## Data we collect

**None.**

| | |
| --- | --- |
| Data collection | ❌ None |
| Data sent to the developer | ❌ Never |
| Third-party sharing or sale | ❌ Never |
| Advertising / tracking | ❌ None |
| Analytics | ❌ None |

Email contents, attachments, and settings never leave your browser.

## Permissions

| Permission | Why it is needed |
| --- | --- |
| `downloads` | Detect and cancel `.msg`/`.eml` downloads so they open in the viewer instead of being saved. |
| `storage` | Save your preferences locally on your device. |
| `contextMenus` | Add a right-click **"Open with MSG & EML Viewer"** item on links. |
| `host_permissions` (`<all_urls>`) | Fetch the original file from any origin — including authenticated corporate intranets — using your session, so it can be parsed locally. No page content is read or sent anywhere. |

## Remote content

Remote images inside emails are **blocked by default** to prevent tracking
pixels. You may opt in per email to load them; your browser then requests those
images directly from their host, exactly as any web page would.

## Data retention & deletion

The only stored data is your local preferences. Removing the extension deletes
all stored settings immediately.

## Contact

Questions about this policy? Reach out via [eth0.pp.ua](https://eth0.pp.ua/) or
on [GitHub](https://github.com/Evgeniyme).

## Changes

This policy may be updated over time; the _"Last updated"_ date above always
reflects the current version.
