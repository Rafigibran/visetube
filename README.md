<div align="center">

<img src=".github/assets/icon.png" width="112" height="112" alt="ViseTube icon">

# ViseTube

### Built on SmartTube. Made for your phone.

An unofficial YouTube client for Android phones and tablets, built on
[SmartTube](https://github.com/yuliskov/SmartTube) by [@yuliskov](https://github.com/yuliskov).<br>
Sign in with a code, keep it playing in the background, save videos for offline,
and cast to SmartTube on your TV.

[![Latest release](https://img.shields.io/github/v/release/Rafigibran/visetube?style=flat-square&label=release&color=1E2A78)](https://github.com/Rafigibran/visetube/releases/latest)
[![Android 7.0+](https://img.shields.io/badge/Android-7.0%2B-1E2A78?style=flat-square)](#download)
[![License: MIT](https://img.shields.io/badge/license-MIT-1E2A78?style=flat-square)](LICENSE)
[![Built on SmartTube](https://img.shields.io/badge/built_on-SmartTube-1E2A78?style=flat-square)](https://github.com/yuliskov/SmartTube)

**[Download](#download) · [Features](#features) · [How sign-in works](#how-sign-in-works) · [FAQ](#faq) · [Credits](#built-on-smarttube)**

<br>

<img src=".github/assets/hero.webp" width="100%" alt="Three ViseTube screens: the sign-in code, the watch page with SponsorBlock segments, and the Downloads tab">

</div>

> [!NOTE]
> **ViseTube is SmartTube's work underneath.** The engine that talks to YouTube, the account
> sign-in and the SponsorBlock, DeArrow and Return YouTube Dislike integrations all come from
> [SmartTube](https://github.com/yuliskov/SmartTube). ViseTube adds a touch interface, its own
> player and offline saving. It is an independent project, not endorsed by SmartTube's developer.
> ViseTube takes no donations: if you find it useful, [support SmartTube](https://github.com/yuliskov/SmartTube#donation).

## Features

<table>
<tr>
<td width="50%" valign="top">

#### Your account, in seconds
Sign in once with a code and your subscriptions, history, playlists, Watch later and
recommendations load from your account. It doesn't need microG, GmsCore, root or a patched app.
Signing in is optional; signed out, YouTube still personalises Home from what you watch.

</td>
<td width="50%" valign="top">

#### Keeps playing
Background playback with the screen off, picture-in-picture, and a mini-player you can
drag down while you keep browsing. Lock-screen and headset controls work too.

</td>
</tr>
<tr>
<td valign="top">

#### Save for offline
Pick a quality up to 1080p, or keep only the audio. Saved videos play in the same player
with no connection, and they show up in your gallery.

</td>
<td valign="top">

#### Measured speed
The first screen appears in about 0.24 s, and a related video shows its first frame about half
a second after you tap it ([Pixel 9 medians](#how-fast)). The interface is plain Material Design,
in a dark theme (a light one is on the way).

</td>
</tr>
<tr>
<td valign="top">

#### Less noise
**SponsorBlock** skips sponsor segments, **DeArrow** swaps clickbait titles and thumbnails,
and **Return YouTube Dislike** shows estimated dislike counts. Shorts are hidden in Home and
Subscriptions.

</td>
<td valign="top">

#### Works with SmartTube on your TV
Pair with SmartTube on the TV using its Remote control code. You can also play straight to a
Chromecast from the phone (no live streams or subtitles in that mode), or use the TV's own
YouTube app.

</td>
</tr>
</table>

<details>
<summary><b>Everything else</b></summary>

- Up to 4K where the video and the phone allow (1080p by default), with codec choice
- Subtitles, including auto-translated tracks, and caption style and size
- Playback speed from 0.25x to 2x, plus finer steps
- Playlists: Play all, Shuffle, Save to playlist, New playlist, a queue with "Playing from…"
- Several accounts, with a switcher, or none at all
- Picture-in-picture on Android 8 and later
- Read comments and live chat; chapters and dubbed audio tracks
- Playback that waits out tunnels and dead zones and resumes where it stopped
- English and Spanish

</details>

<p align="center">
<img src=".github/assets/screens/channel.webp" width="23%" alt="Blender Studio channel page">
<img src=".github/assets/screens/mini.webp" width="23%" alt="Mini-player over search results">
<img src=".github/assets/screens/quality.webp" width="23%" alt="Quality picker up to 2160p60">
<img src=".github/assets/screens/picker.webp" width="23%" alt="Save-for-offline quality picker with file sizes">
</p>

## Download

<a href="https://github.com/Rafigibran/visetube/releases/latest"><img src="images/badge_github.png" height="64" alt="Get it on GitHub"></a>

| Your device | File |
|:--|:--|
| Almost every phone from the last ~8 years | `ViseTube_<version>_arm64-v8a.apk` |
| Older 32-bit phones | `ViseTube_<version>_armeabi-v7a.apk` |
| Not sure (any ARM phone) | `ViseTube_<version>_universal.apk` (bigger) |
| Older x86 devices and emulators | `ViseTube_<version>_x86.apk` |

- **Requires Android 7.0 or newer.** ViseTube has its own package name
  (`com.rafgibran.visetube`), so it installs next to SmartTube or the YouTube app.
- **Updates:** with [Obtainium](https://obtainium.imranr.dev), choose *Add app* and paste
  `https://github.com/Rafigibran/visetube`, or install a newer APK over the old one. ViseTube
  also checks for new versions itself and offers them in the app.
- **Verify what you install.** Every APK is signed with the same key. Its certificate SHA-256 is
  `2e:f9:9d:76:ed:fa:d9:88:ad:17:cd:ee:8b:a1:8c:63:4e:23:0f:e1:e3:cb:1f:dc:6c:db:02:49:37:0a:36:c9`.
  Check it with `apksigner verify --print-certs <file>.apk`. Each release also lists a SHA-256 for every file.
  From 1.10.3 the APKs are built by GitHub Actions from the tagged source; check that with
  `gh attestation verify <file>.apk -R Rafigibran/visetube`.
  ViseTube's key is not SmartTube's, so neither app can update the other.
- **Distributed on GitHub**, not on Google Play.

## How sign-in works

1. Open the **You** tab, tap the account row, then **Sign in**. ViseTube shows a short code.
2. Tap **Continue with Google**. Google's own page opens: pick your account and allow access.
   It may mention a TV, because ViseTube signs in the same way a TV does.
3. Come back. Sign-in finishes by itself.

Your password is only ever typed into Google's page, never into ViseTube. The login token is
stored on your phone and never sent to the developer. You can revoke it at any time at
[myaccount.google.com/security](https://myaccount.google.com/security), under
*Your connections to third-party apps & services*.

## How fast

Medians measured on a Pixel 9 with release builds: small samples, one phone, one carrier, and the
mobile-data runs were on different days. The method and the full table are in
[STATUS.md](docs/mobile-port/STATUS.md).

| | Wi-Fi | Mobile data |
|:--|--:|--:|
| Open the app → first screen | 0.24 s | 0.24 s |
| Open the app → Home fully painted | 1.35 s | 1.56 s |
| Tap a related video → first frame | 0.50 s | 0.53 s |
| Tap a related video → picture visible | 0.66 s | 0.73 s |
| Reopen a half-watched video → picture | 0.37 s | – |
| Tap a shared link → first frame | 0.66 s | 0.84 s |

## ViseTube and SmartTube

|  | SmartTube | ViseTube |
|:--|:--|:--|
| Made for | Android TV and TV boxes | Phones and tablets |
| Controls | TV remote (D-pad) | Touch and gestures |
| Interface | Leanback | Material Design |
| Engine | MediaServiceCore + SharedModules | Forks of the same modules |
| Player | ExoPlayer | androidx Media3 |
| Offline saving | No | Yes |
| License | MIT | MIT |

Have an Android TV? Get [SmartTube](https://github.com/yuliskov/SmartTube). It's excellent,
and ViseTube can cast to it.

## FAQ

<details>
<summary><b>Do I need microG, GmsCore, root or ReVanced?</b></summary>

No. ViseTube isn't a patched YouTube app. It signs in with a code the way a TV does, so it
doesn't need Google Play Services or a stand-in for them.

</details>

<details>
<summary><b>How is it different from NewPipe, LibreTube or ReVanced?</b></summary>

They're all good apps, and which one fits depends on what you want. NewPipe and LibreTube
don't sign in to a Google account; they keep subscriptions on your phone or on a Piped server.
ReVanced patches the official app and needs GmsCore unless you're rooted.
ViseTube is built on SmartTube, so it uses your real account without any of that.

</details>

<details>
<summary><b>Is there another SmartTube-based phone app?</b></summary>

Yes. [SmarterTube](https://github.com/CodeSculptor/SmarterTube) is another independent phone
fork of SmartTube, worth comparing. The two are separate projects. One difference today
(September 2026): ViseTube can save videos for offline.

</details>

<details>
<summary><b>Is it safe? How do I know the APK is really ViseTube?</b></summary>

Up to 1.10.2 the APKs were built on the maintainer's computer. From 1.10.3 they're built by
GitHub Actions from the tagged source, and each file has a build attestation you can check with
`gh attestation verify <file>.apk -R Rafigibran/visetube`. The builds aren't reproducible yet. Check the signing
certificate against the fingerprint under [Download](#download), and each file against the
SHA-256 in its release notes. Every release is tagged, so you can read the exact source.
The app has no analytics, no crash reporting and no ad SDKs, and the developer receives nothing.
It talks to YouTube (which sees what you watch, as it would anywhere), to the community services
you can switch off (SponsorBlock, DeArrow, Return YouTube Dislike), and to GitHub. Details are
in [PRIVACY.md](PRIVACY.md).

</details>

<details>
<summary><b>Was this made with AI?</b></summary>

Yes, in large part. ViseTube is one person's project, and most of its own code (the phone
interface, the player and the network work) was written with AI coding assistants (Claude and
Codex); the commit trailers say so. The maintainer directs and reviews that work and uses the app
daily. Each [release record](docs/releases/) lists what was checked on a real phone, what only in
automated tests, and what is still open. The engine underneath is SmartTube's, written by
@yuliskov and its contributors over several years.

</details>

<details>
<summary><b>Why no donations?</b></summary>

ViseTube doesn't take donations. SmartTube did the heavy lifting, so if you want to give
something back, [support SmartTube](https://github.com/yuliskov/SmartTube#donation).

</details>

<details>
<summary><b>A video won't play. What now?</b></summary>

YouTube sometimes refuses a video or an account. ViseTube retries through other routes, but not
every video comes back. If one keeps failing, [open an issue](https://github.com/Rafigibran/visetube/issues/new/choose)
with the video link and your ViseTube version.

</details>

## Built on SmartTube

| Project | By | Used for |
|:--|:--|:--|
| [SmartTube](https://github.com/yuliskov/SmartTube) | [@yuliskov](https://github.com/yuliskov) and contributors | The engine, accounts and integrations: everything under the hood |
| [SponsorBlock](https://sponsor.ajay.app) · [DeArrow](https://dearrow.ajay.app) | Ajay Ramachandran and contributors | Segment and title data (CC BY-NC-SA 4.0) |
| [Return YouTube Dislike](https://returnyoutubedislike.com) | RYD contributors | Dislike counts |
| [androidx Media3](https://developer.android.com/media/media3) | Google (Apache-2.0) | Playback |

Full notices are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
SmartTube's original README is kept at [docs/UPSTREAM_README_SmartTube.md](docs/UPSTREAM_README_SmartTube.md).

## Building and contributing

Issues and pull requests are welcome. Build instructions are in [docs/BUILDING.md](docs/BUILDING.md).
The [changelog](CHANGELOG.md) covers every release, with a
[Spanish edition](CHANGELOG.es.md) for the testers.

## License

[MIT](LICENSE), the same as SmartTube. © yuliskov (SmartTube) and ViseTube contributors.

## Star history

<a href="https://www.star-history.com/#Rafigibran/visetube&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Rafigibran/visetube&type=Date&theme=dark">
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Rafigibran/visetube&type=Date">
    <img alt="ViseTube's GitHub stars over time" src="https://api.star-history.com/svg?repos=Rafigibran/visetube&type=Date" width="100%">
  </picture>
</a>

---

*ViseTube is an independent, unofficial project. It is not affiliated with, funded, authorized or
endorsed by Google LLC, YouTube, or SmartTube's developer, and it hosts no content. Save only what
the law and the platform's terms allow you to. YouTube, Android and Google are trademarks of Google LLC.*
