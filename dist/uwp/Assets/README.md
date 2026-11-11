# Brand assets

The GrungeBOX logo, wordmark, tiles, splash screen and launch logo:

- `GrungeBoxLogo.png`, `GrungeBoxWordmark.png`, `LaunchLogo.png`
- `Square150x150Logo.scale-200.png`, `Square44x44Logo.scale-200.png`, `StoreLogo.scale-200.png`
- `Wide310x150Logo.scale-200.png`, `SplashScreen.scale-200.png`

`src/jadyx/storage/network_portal_logo.h` embeds the bytes of `Square150x150Logo.scale-200.png`
for the web portal. Regenerate it after changing that file; `tools/xbox/tests/network-portal-page.cjs`
fails when the two differ.

The `.scale-200` suffix is the file's real size (200% of the base size the manifest names);
`tools/xbox/package-appx.ps1` builds the `resources.pri` that maps one to the other.

`InputPrompts/` is third-party; see its own README.

`Fonts/` holds [Inter](https://rsms.me/inter/) by Rasmus Andersson (Regular, Medium, SemiBold,
Bold), under the SIL Open Font License 1.1; see `Fonts/OFL.txt`.
