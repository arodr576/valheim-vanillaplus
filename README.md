# Valheim Vanilla+

Client modpack releases for our Valheim server, with the unofficial **Valheim Companion** Windows updater.

## Players

1. Open the [latest release](https://github.com/arodr576/valheim-vanillaplus/releases/latest).
2. Download **ValheimCompanion-v0.5.zip**, extract it, and run **ValheimCompanion.exe**.
3. Choose the folder containing your `valheim.exe`.
4. Click **Check / Verify**, review the release, close Valheim, then click **Install / Repair**.

The app already has the update feed configured. Keep using this address for future releases:

```text
https://github.com/arodr576/valheim-vanillaplus/releases/latest/download/release.json
```

Updates verify SHA256 checksums and create a rollback backup. Managed mod settings are replaced by the release's settings. Extra unmanaged plugins are preserved and listed for review. Avoid having Vortex manage the same files. World saves are not managed by the updater.

The release also includes the modpack ZIP for manual installation. Its version-specific download is pinned by the manifest, so a changing latest release cannot silently substitute another ZIP during installation.

## Admin

Use the app's **Admin / Build release** screen with the prepared client staging folder and a known-good BepInEx 5 installation. Confirm the shared gameplay mods match the server using the existing DLL-report workflow. The app does not connect to or update the dedicated server.

The app ZIP contains source, build instructions, and `Publish-GitHub.ps1` for future releases. Upload the ZIP and `release.json` together, then publish the release as latest. Keep this repository's latest release dedicated to the modpack feed; an app-only release without `release.json` would break the stable feed address.

The first app-backed release passed 33 synthetic integration checks and a file-level install/verify/rollback test using the real 1.0.1 pack. Public downloads were verified against the original files. A live desktop HTTPS and gameplay test on a spare client remains the next validation step.

This is an unofficial community tool. Valheim, its logo, and included third-party mods belong to their respective rights holders. Attribution and mod-package documentation are included with the downloads.
