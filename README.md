# Island Music Patch

An unofficial source patch for the Windows version of Coucou. It adds a YouTube Music pill with inline song and playlist search, background playback, and a separate volume level that stays put when you switch pills. It also adds a session-scoped Auto Allow toggle for new agent permission requests.

## Apply the patch

Use the Windows build prerequisites from the [upstream Windows README](https://github.com/Louis-CFM/coucou/blob/main/windows/README.md). Run these commands from the checkout with Git, Node.js, Rust and the Windows C++ build tools available.

```powershell
git clone https://github.com/Louis-CFM/coucou.git
cd coucou
git checkout 0d7fe58884d99f275f3238e8dbe29ddee69fa9e8
git apply C:/path/to/island-music.patch
cd windows
npm ci
npm run tauri build
```

Enable **YouTube Music** under **Settings → Active pills**. Search results appear inside the island, and the music-note button opens the full player on demand. On an agent approval card, **Auto Allow** applies to future permission requests from that session. The header lets you turn it off.

## Credits

**[Louis Raillé (Louis-CFM)](https://github.com/Louis-CFM) created Coucou.** Thank you, Louis, for making Coucou and sharing its source. Thanks also to everyone who contributes to the [original project](https://github.com/Louis-CFM/coucou).

This repository distributes a source patch under the [MIT License](LICENSE). The original name, character, icons, sounds and artwork are covered by [upstream's separate asset license](https://github.com/Louis-CFM/coucou/blob/main/LICENSE-ASSETS.md). For official builds, see the [original Coucou releases](https://github.com/Louis-CFM/coucou/releases).
