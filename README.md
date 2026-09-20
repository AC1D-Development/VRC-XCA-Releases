# VRC-XCA

Release downloads for **VRC-XCA**, a fork of [VRCX](https://github.com/vrcx-team/VRCX) — an assistant/companion application for VRChat.

This repository contains **builds only**. The source code is kept in a private repository, so there is no code, issue tracker, or commit history here. Every release below is produced by an automated build from that private source.

## Download

Grab the latest build from the [**Releases page**](../../releases/latest).

| Platform | File |
|---|---|
| **Windows** (recommended) | `VRCX_<version>_Setup.exe` |
| Windows (portable, no installer) | `VRCX_<version>.zip` |
| Linux (x64) | `VRCX_<version>_x64.AppImage` |
| Linux (ARM64) | `VRCX_<version>_arm64.AppImage` |
| macOS (Intel) | `VRCX_<version>_x64.dmg` |
| macOS (Apple Silicon) | `VRCX_<version>_arm64.dmg` |

On Windows, run the installer and you're done. On Linux, mark the AppImage executable first:

```sh
chmod +x VRCX_*.AppImage
./VRCX_*.AppImage
```

## Updating

You usually don't need this page. VRC-XCA checks here for new releases once an hour while running and will offer the update to you in-app.

You can change this behaviour under **Settings → General → Update**:

- **Auto Download** (default) — downloads the update in the background, installs it next time you restart.
- **Notify** — tells you an update exists and waits for you to start it.
- **Off** — never checks.

Updates downloaded in-app are verified against the SHA-256 published with the release before they are installed. A download that doesn't match is discarded.

## Verifying a manual download

If you downloaded the installer from this page by hand, you can check it against the SHA-256 GitHub publishes for the asset:

```powershell
Get-FileHash .\VRCX_<version>_Setup.exe -Algorithm SHA256
```

```sh
gh release view <version> --repo AC1D-Development/VRC-XCA-releases --json assets --jq '.assets[] | "\(.digest)  \(.name)"'
```

## Support

<!-- FILL: where should users report bugs or ask questions? A Discord invite, an email,
     or a public issues-only repo. Do not point them at the upstream VRCX Discord —
     upstream can't support a fork's builds. -->

## License and attribution

VRC-XCA is a fork of [VRCX](https://github.com/vrcx-team/VRCX) and is distributed under the MIT License.

> Copyright (c) 2019-2026 pypy, individual contributors, AC1D-Development, and CraziestPizza

See [LICENSE](./LICENSE) for the full text. <!-- FILL: copy the LICENSE file from the source repo into this repo -->

## Disclaimer

VRCX is not endorsed by VRChat and does not reflect the views or opinions of VRChat or anyone officially involved in producing or managing VRChat properties. VRChat and all associated properties are trademarks or registered trademarks of VRChat Inc. VRChat © VRChat Inc.
