# Remote97

**One app to control your entire home theater — no hub hardware required.**

Remote97 is a pure-software universal remote for your home cinema. Traditional setups require an expensive control hub (Control4, ELAN, Savant) plus professional programming. Remote97 replaces that with the phone or PC you already own, talking to your gear directly over the local Wi-Fi network. Zero extra hardware, zero monthly fees.

Official site: **https://remote97.com**

---

## Why Remote97

- **No hub, no hardware** — runs as an app on devices you already have; connects straight to your equipment over LAN.
- **Auto discovery** — finds supported devices on the network (SSDP / mDNS / vendor probes), no manual IP typing needed.
- **One unified remote** — volume, input source, power & standby, sound modes, EQ, and on-screen text input, all in one place.
- **Multi-room audio** — group and control Sonos, Bluesound (BluOS), WiiM, and Arylic speakers together.
- **Custom layouts & themes** — organize devices your way; multiple UI themes including glassmorphism and ink-wash.
- **Windows with global hotkeys** — control the whole stack from the keyboard while seated.
- **Privacy-first** — no cloud, no account, no telemetry. Everything stays on your local network.
- **Free.**

## Supported devices

| Category | Brands / Protocol |
|----------|-------------------|
| AV receivers | **Denon / Marantz** (Telnet + HTTP), **Yamaha** MusicCast (YXC) |
| TVs | **Sony** Bravia (REST + IRCC), **Samsung** (WebSocket / JSON-RPC), **Xiaomi / Redmi** (HTTP), **LG webOS** (SSAP), **Apple TV** (MRP), **Roku** (ECP) |
| Streamers / media hubs | **Zidoo**, **Vidoo / 威动** |
| Wireless audio | **Sonos**, **Bluesound BluOS**, **WiiM**, **Arylic** (LinkPlay) |
| Projectors | **PJLink** (TCP 4352) |

> Device coverage grows over time. New families are added through a documented device-research + simulator standard so each addition ships with a test harness.

## Platforms

| Platform | Distribution |
|----------|--------------|
| Android | Google Play + direct APK |
| iOS / iPadOS | Apple App Store |
| Windows | Microsoft Store + portable ZIP (no install) |
| Web | responsive site at https://remote97.com |

## Download

All download options (Google Play, App Store, Microsoft Store, APK, Windows ZIP) are listed on the site: **https://remote97.com**

Direct releases are also published on the [GitHub Releases](https://github.com/Benjamin-LY777/remote97/releases) page.

## Project layout

```
remote97/
├─ cinehub_app/            # Flutter app (Android / iOS / Windows)
├─ website/                # Static marketing site (https://remote97.com)
├─ store_listing/          # App-store screenshots & copy
├─ simulators/             # Device simulators for development & testing
└─ tools/                  # Build & dev helper scripts
```

## Development

The app is built with [Flutter](https://flutter.dev).

```bash
# Pull dependencies
cd cinehub_app
flutter pub get

# Run on a connected device / desktop
flutter run

# Build release artifacts
flutter build apk --release            # Android
flutter build windows --release        # Windows
# iOS builds are produced via CI (Codemagic)
```

Device simulators (no real hardware needed for development) live under `simulators/` and follow `SIMULATOR_STANDARD.md`.

## License

MIT — see the repository for details.
