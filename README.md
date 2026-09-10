# Backstage Production — downloads

Backstage helps a production team assign microphones, IEM packs, and instrument connections, then display each musician’s setup backstage.

## Download and install

**[Open downloads and installation guides](https://github.com/pfteamboy24-source/backstage-downloads/releases)**

Current release: **[Backstage Preview 12](https://github.com/pfteamboy24-source/backstage-downloads/releases/tag/v0.1.1-preview.12)**

No GitHub account, collaborator invitation, or access token is needed.

- **Windows 10/11, Intel/AMD 64-bit:** download the `Backstage-Setup-…-Windows-x64.exe` installer. Double-click to install and start the app. No terminal or Node.js installation is needed. Download `Windows.html` for the step-by-step guide.
- **Raspberry Pi 4/5, 64-bit Raspberry Pi OS with Desktop:** download `backstage-production_…_arm64.deb` and `Pi.html`. Open the guide in your browser for installation steps. Backstage starts automatically after boot. A terminal fallback is included if the desktop has no graphical package installer.

Choose the installer under **Assets**, rather than GitHub’s automatically generated “Source code” archives (those contain only this download repository’s documentation).

Windows preview installers are unsigned. Pi hardware operation and coexistence with Companion need testing on your own equipment before a production service. Mac and 32-bit Pi packages are not included.

## Updates

Open **Display & connections → App updates → Check for updates**. The host also checks at startup and every six hours when it has internet access. It verifies the download’s SHA-256 checksum. You choose when to run the installer; it does not automatically interrupt a service.

If an older installation asks for a GitHub token, download and install the latest package here once. That switches future checks to public downloads. Close the Windows Backstage control window before updating; Pi installation restarts its service. Saved data is retained. Export a backup before updating.

For a first-time headless Pi installation, connect over SSH and run the included PIN setup tool as the Backstage service account. The downloadable `Pi.html` guide contains the exact three commands and explains why initial PIN creation is limited to the host.

## Your data

New installations start empty. Packages include runtime code, but no church equipment list, musician records, photos, Planning Center credentials, or PIN. Your saved setup stays on your app host. Connect your own Planning Center account if needed. Never upload your database, credentials, or private backup to this public repository.

This repository distributes installers and guides. Development source and history are maintained separately.
