# Valheim Vanilla+

Client modpack releases for our Valheim server and the unofficial **Valheim Companion** Windows updater.

## Downloads

- [**Companion Player Installer — v0.16.2**](https://github.com/arodr576/valheim-vanillaplus/releases/tag/companion-v0.16.2)
- [**Latest Valheim Vanilla+ modpack**](https://github.com/arodr576/valheim-vanillaplus/releases/latest)

The app installer and modpack now have separate release pages. Older Companion ZIPs are historical downloads.

## Players

1. Open the Companion installer page above and download **ValheimCompanion-v0.16.2-x64.msi**.
2. Close any running Companion app, run setup, and choose your shortcuts. New installations can choose a writable installation folder; MSI upgrades keep the existing folder and settings.
3. Open **Valheim Companion** and confirm the detected folder containing `valheim.exe`.
4. Click **Check / Verify**, review the release, close Valheim, then click **Install / Repair**.
5. Use **Play Valheim** with Steam running.

The player installer includes no admin launcher, admin shortcut, admin screen, or release-building code. The installer is unsigned, so Windows may show an unrecognized-app warning. A SHA256 checksum is available on its download page.

The update feed is already configured:

```text
https://github.com/arodr576/valheim-vanillaplus/releases/latest/download/release.json
```

Updates verify SHA256 checksums and create a rollback backup. Managed mod settings are replaced by the release settings. Extra unmanaged plugins are preserved and listed for review. Avoid having Vortex manage the same files. World saves are not managed by the updater.

The latest modpack release includes its ZIP and release.json for manual downloads. The manifest pins the version-specific package URL.

## Server administration

Server administration uses a separate Admin build, distributed separately from the public player installer. Use its **Admin / Build release** screen with prepared client staging and a known-good BepInEx 5 installation. Confirm shared gameplay mods match the server through the existing DLL-report workflow. Companion does not connect to or update the dedicated server.

Publish modpack ZIPs and release.json together. Keep the repository **Latest** label on the current modpack release so the update feed continues working. Companion-only releases use their own tags and must not replace that latest modpack release.

## Validation

Companion v0.16.2 passed 59 existing engine integration checks, Player/Admin capability and settings-save checks, and MSI build/payload validation. Full installation and upgrade testing of this revision remains outstanding. See each release page for its validation details.

This is an unofficial community tool. Valheim, its logo, and included third-party mods belong to their respective rights holders. Attribution and mod-package documentation accompany the relevant downloads.
