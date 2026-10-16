# s2f — Storybook to Figma (downloads)

Turn any Storybook into Figma components: every prop combination becomes a variant, themes and brands
become variant options, design tokens become Figma variables.

This repository only hosts the installer and release packages.

## Install (macOS, once)

Open Terminal (⌘ Space → type "Terminal"), paste this and press Return:

```bash
curl -fsSL https://github.com/milosdostanic-cyber/s2f-releases/releases/latest/download/install.sh | bash
```

It takes about a minute and needs nothing else (s2f brings its own Node.js). The helper then starts by
itself every time you log in, and Finder opens the folder with the Figma plugin.

Then, in the Figma **desktop** app (once): **Plugins → Development → Import plugin from manifest…** →
`~/Documents/s2f/Figma plugin/manifest.json`.

## Use

Open an empty Figma file → Plugins → Development → **s2f – Storybook to Figma** → paste a Storybook link →
**Connect** → choose components → **Capture** → **Create**. The first time only, click
**Show pairing code** and type the 6-digit code that pops up on your screen.

## Update

Run the install command again.

## Remove

Download `s2f.zip` from the [latest release](../../releases/latest), unzip it and double-click
`Uninstall helper.command`.

## What the installer does

- Downloads `s2f.zip` from this repository's latest release and an official Node.js build from
  nodejs.org (checksum verified) into `~/.s2f`.
- Installs the helper in `~/.s2f/app` and registers it as a login item (`~/Library/LaunchAgents/com.s2f.helper.plist`).
  It listens on `localhost:7337` only and works only with Figma plugins you pair.
- Copies the Figma plugin to `~/Documents/s2f/Figma plugin`.

Made by Miloš Dostanić.
