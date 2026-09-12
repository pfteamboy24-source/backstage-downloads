# Backstage Production

Backstage is a local-network production app for church service lineups, equipment assignments, team displays, and Companion controls. Front of house prepares each person's setup, publishes only what is ready, and sends clear information to backstage, stream, and production displays.

## Current release

**[Backstage Preview 13 — Final Preview](https://github.com/pfteamboy24-source/backstage-downloads/releases/tag/v0.1.1-preview.13)**

Preview 13 is the release candidate for the beta phase. Backstage is preview software undergoing real-world testing. Back up your data before updating, test it with non-critical equipment first, and keep your existing production workflow available until Backstage has been verified in your environment.

## Choose your download

| Host | Download | Use it for |
| --- | --- | --- |
| Windows 10/11 x64 | `Backstage-Setup-0.1.1-preview.13-Windows-x64.exe` | A Windows PC or virtual machine. Includes the runtime, desktop shortcut, and app control window. |
| Raspberry Pi 4/5 arm64 | `backstage-production_0.1.1-preview13_arm64.deb` | 64-bit Raspberry Pi OS with a desktop or headless operation. Includes the runtime and automatic system service. |
| Windows guide | `Windows.html` | Step-by-step installation and update instructions. |
| Raspberry Pi guide | `Pi.html` | Desktop and headless installation, first-PIN commands, updates, and troubleshooting. |

Open the release, expand **Assets**, and choose the installer for the host that will run Backstage. Do not download GitHub's automatically generated **Source code** archives; this repository contains download documentation rather than the private application source.

No GitHub account, collaborator invitation, access token, or separate Node.js installation is needed.

## What Backstage does

- Builds service lineups manually or from Planning Center Services. Planning Center remains optional.
- Keeps people and locally defined teams, imports each church's own Planning Center team names, and tracks confirmed, declined, or unconfirmed scheduling status.
- Stores microphones, IEM packs, DI boxes, instruments, stage-box ports, notes, and reusable setups.
- Keeps edits as drafts until front of house publishes them. Declined people are removed from live displays automatically.
- Preserves past services as read-only history so previous assignments remain available.
- Provides a full backstage lineup, a ProPresenter StageDisplay overlay, and up to 12 named team displays with custom layouts.
- Can launch a chosen screen automatically on a monitor connected to a Windows, macOS, Linux, or Raspberry Pi host.
- Uses separate Admin and Team PINs. Team access handles service work while host settings, credentials, backups, updates, and token management remain administrative.
- Exports and restores backups while keeping host authentication and credentials separate.
- Checks the public release feed, verifies installer checksums, and lets an administrator choose when to update.
- Provides a scoped HTTP API for Bitfocus Companion actions and status feedback without sharing the Admin PIN.
- Includes searchable Help & how-to instructions inside the app.

## Install or update

Before updating, open **Display & connections → Back up or restore your setup** and export a backup.

On Windows, close the Backstage control window and run the new `.exe`. On a Pi, download the `.deb` and run:

```sh
sudo apt install ~/Downloads/backstage-production_0.1.1-preview13_arm64.deb
```

The Pi service restarts during installation, so update outside a live service. Saved data, PINs, Planning Center credentials, display layouts, and Companion tokens stay in the host data folder.

For a first-time headless Pi installation, follow `Pi.html`. It includes the exact commands for setting the first Admin PIN as the Backstage service account.

## Current testing limits

- Windows installers are not code-signed yet, so Windows may show an unknown-publisher warning.
- Raspberry Pi and Companion coexistence should be tested on the exact Pi model and production load before service use.
- There is no packaged macOS installer. A Mac can use the portable runtime during development and can display any Backstage screen in a browser.
- Companion uses its Generic HTTP connection in this preview; a dedicated Companion module may follow during beta.
- Browser and ProPresenter web views must be tested on the church's actual display hardware and network.

## Data and privacy

New installations start empty. Public packages contain no church database, people, photos, equipment, PINs, Planning Center credentials, or Companion tokens. Windows data stays in `%LOCALAPPDATA%\Backstage\data`; Pi data stays in `/var/lib/backstage-production`. Installer updates preserve those folders.

See the [complete release history](https://github.com/pfteamboy24-source/backstage-downloads/blob/main/CHANGELOG.md). Report a packaging or installation problem through the [downloads repository issues](https://github.com/pfteamboy24-source/backstage-downloads/issues).
