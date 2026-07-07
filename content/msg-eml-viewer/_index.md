---
title: "MSG & EML Email Viewer"
date: 2026-07-02
url: "/msg-eml-viewer/"
showtoc: true
tocopen: true
ShowReadingTime: false
ShowWordCount: false
ShowShareButtons: false
ShowBreadCrumbs: false
hidemeta: true
---

A browser extension that intercepts `.msg` and `.eml` email file downloads and
opens them in a clean, built-in viewer — instead of dumping files you can't open
into your Downloads folder. Everything is parsed **locally in your browser**; no
data ever leaves your device.

Works on **Chrome** (and Chromium-based browsers like Edge), across macOS,
Windows, and Linux.

![The viewer showing a parsed email](/msg-eml-viewer/cursor.png)

## Install

- **Chrome / Edge:** [Get it on the Chrome Web Store](https://chromewebstore.google.com/detail/msg-eml-email-viewer/egkhffpepjgikgehkpaoblhjdkdmnbdo)

After installing, you'll see the **MSG & EML Viewer** icon in your browser
toolbar.

## How it works

1. You (or a site like Jira / ServiceDesk) start a download of a `.msg` or
   `.eml` file.
2. If the download comes from a site you've allowed, the extension **cancels the
   download** and opens the file in its viewer tab instead.
3. The email is parsed on your machine and rendered with subject, sender,
   recipients, date, body, and attachments.

## Configure it

Click the **toolbar icon** to open the settings page.

![Settings page](/msg-eml-viewer/settings.png)

There are two toggles and one list:

### 1. Intercept downloads

The master switch. When **on**, matching `.msg`/`.eml` downloads open in the
viewer. Turn it **off** to temporarily pause the extension without removing your
site patterns.

### 2. Intercept from all sites

- **Off (default & recommended):** only intercepts downloads from the sites in
  your pattern list below.
- **On:** intercepts `.msg`/`.eml` downloads from **any** website.

### 3. Site URL patterns

This is the list of sites that trigger automatic interception. Type a domain and
press **Add** (or Enter). By default the list includes `*.atlassian.net` and
`jira.*`.

Patterns are matched against the **hostname** only, and you can use `*` as a
wildcard:

| Pattern | Matches |
| --- | --- |
| `*.atlassian.net` | `yourcompany.atlassian.net`, `jira.atlassian.net` |
| `jira.*` | `jira.example.com`, `jira.internal.local` |
| `servicedesk.company.com` | that exact host **and** its subdomains |
| `*` | any host (same effect as "intercept from all sites") |

> **Tip:** a bare domain like `company.com` also matches its subdomains
> (`support.company.com`), so you rarely need a leading `*.`.

Settings are saved instantly and synced across the browsers you're signed into.

## Using the viewer

Once an email is open, you can read the full message — subject, from, to, cc,
date, body, and attachments.

### The toolbar

In the top-right corner of the viewer there are four buttons:

![The viewer toolbar](/msg-eml-viewer/tools.png)

From left to right:

1. **Theme** — cycles between three modes (see below).
2. **Open another file** (folder icon) — open a `.msg`/`.eml` file from your
   computer.
3. **Print / Save as PDF** (printer icon) — opens your browser's print dialog.
4. **Download original file** (down-arrow icon) — save the raw email file to
   disk.

### Switching the theme

The **first icon is the theme button** — but it may not look like one at first,
because in the default **System** mode its icon is a **monitor**, not a sun or a
moon. Each click cycles to the next mode:

- 🖥️ **Monitor = System** — follows your operating system's light/dark setting.
- ☀️ **Sun = Light** — always light.
- 🌙 **Moon = Dark** — always dark.

Your choice is remembered across sessions. Hover the button and the tooltip
shows the current mode, e.g. *"Theme: Dark (click to change)"*.

![The viewer in dark theme](/msg-eml-viewer/cloudflare.png)

### Remote images

Remote images are **blocked by default** to stop tracking pixels. When an email
contains them, a banner appears — click **Load remote images** to show them for
that email if you trust the sender.

![Remote images blocked, with the Load remote images button](/msg-eml-viewer/fedex.png)

## Opening files manually

You don't have to rely on auto-interception:

- **Right-click any link** to a `.msg`/`.eml` file and choose
  **"Open with MSG & EML Viewer"**.
- **Drag and drop** a file onto the viewer, or use the file picker, to open
  emails saved on your computer.

## Privacy

All parsing happens locally. The extension does not collect, transmit, or share
any data. Read the full [Privacy Policy](/msg-eml-viewer/privacy/).

## Support the project

This extension is free and open. If it saves you time, you can support its
development:

☕ [**Buy me a coffee**](https://buymeacoffee.com/thegeka)

Leaving a rating on the [Chrome Web Store](https://chromewebstore.google.com/detail/msg-eml-email-viewer/egkhffpepjgikgehkpaoblhjdkdmnbdo)
helps too.

## Troubleshooting

- **A download still saves to disk instead of opening.** Make sure *Intercept
  downloads* is on, and that the site's hostname matches one of your patterns
  (or enable *Intercept from all sites*).
- **Images don't show in an email.** That's intentional — click the option to
  load remote images for that email.
- **Nothing happens on a link.** Use right-click → *Open with MSG & EML Viewer*,
  or drag the file into the viewer.
