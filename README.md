<div align="center">

# 🎬 playAbility pro

**The smart player, fast editor, and your audio-visual companion**

[![Version](https://img.shields.io/badge/version-3.1.1-00aaff.svg?style=flat-square)](https://github.com/hamza-abo-slema/PlayAbility-pro-setup/releases)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6.svg?style=flat-square)
![UI Languages](https://img.shields.io/badge/UI%20Languages-7-00aaff.svg?style=flat-square)
![Accessibility](https://img.shields.io/badge/Accessibility-Screen%20Reader%20Ready-28a745.svg?style=flat-square)

playAbility pro is more than a traditional media player — it's a smart, blazing-fast media player, downloader, and converter that puts a mini-studio in your hands without slowing down your computer or distracting you, while giving you full control over every detail of your media.

</div>

---

## ✨ Key Features

- **⚡ Blazing-Fast Playback for All Formats** — Audio and video files play instantly at the highest possible quality, with no extra codecs or packages to install (powered by MPV).
- **📂 Supercharged Sidebar (File Management)** — Instantly pulls and organizes folders with thousands of files into a blazing-fast, searchable, filterable sidebar with one-click custom playlists.
- **✂️ Instant Lossless Editing** — Cut any clip and export it in the blink of an eye, with 100% original quality and zero re-encoding. Includes a bulk cut bin, frame-by-frame navigation, and fine-grained A/B point control.
- **▶️ YouTube at Your Fingertips** — Search, play (audio or video), download at any quality, subscribe to channels, and manage subscriptions locally — all without opening a heavy browser.
- **📻 Built-in Radio with Smart Scheduling** — Thousands of Arabic, international, and sports stations, live MP3 recording, favorites, and scheduled recordings via Windows Task Scheduler.
- **🎙️ AI Subtitles** — Transcribe and translate any audio or video into subtitle text from inside the app (Whisper + Google Gemini + Groq), with a built-in subtitle editor.
- **🔇 Smart Silence Skip** — Skip silent sections during playback and export a cleaned copy without silence.
- **♿ 100% Screen Reader Compatibility** — Built from the ground up for blind users: every action is instantly announced (NVDA-friendly), fully keyboard-driven, with no unlabeled controls.
- **🎚️ Professional Audio Effects** — Advanced equalizer (EQ) and Reverb Halls applied in real-time for a cinematic listening experience.
- **🔄 Universal Format Converter** — Convert between audio and video formats, edit tags, and manage tracks.
- **🔖 Bookmarks & Chapters** — Bookmark positions, split clips into chapters, and export them as separate files.
- **📜 Subtitle Tools** — Search and download subtitles online, read embedded subtitles aloud, cycle subtitle languages, and manage subtitle files.
- **🪟 Distraction-Free Single Window** — The app opens once; opening any media from Windows sends it to the running player, keeping your desktop clean.

## ♿ Accessibility (Blind Users)

playAbility pro was designed from scratch to be fully compatible with screen readers (especially NVDA):

- Every movement, edit, and step is instantly and interactively announced.
- The interface removes focus from visual elements that don't concern you — the keyboard is your ultimate maestro.
- Pressing `Enter` on any media file in Windows opens the software, announces the file name, and starts playback immediately, with the containing folder loaded as a playlist.
- Sector-specific shortcuts for searching, playlists, editing, radio, and AI subtitles are all announced in real time.

## 📦 Installation

### System Requirements

- **Windows 7 SP1 64-bit or later** (x64 / ARM64-compatible)
- ~200 MB of free disk space (media playback requires no additional codecs)

### Install

1. Download the latest setup file (`playAbility pro setup V3.x.x.exe`) from the [Releases](https://github.com/hamza-abo-slema/PlayAbility-pro-setup/releases) page.
2. Run the setup wizard (Arabic, English, and French installers available).
3. The app registers itself for **"Open With"** on audio and video formats and adds a folder context-menu entry (`Open with playAbility pro`).

> The installer bundles the MPV engine and runtime libraries — no manual dependencies required.

## 🚀 Quick Start

1. Press **Enter** on any audio or video file in Windows — playAbility pro opens and starts playing it instantly.
2. Press **Ctrl+L** to open the supercharged sidebar and search/filter your folder.
3. Press **Ctrl+Y** for YouTube, **Ctrl+R** for Radio, and **S** for AI Subtitles.

### Key Shortcuts

| Function | Shortcut |
| --- | --- |
| Play / Pause | `Space` |
| Volume Up / Down | `↑` / `↓` |
| Boost volume (up to 400%) | `Shift + ↑` |
| Speed Up / Slow Down | `Ctrl + →` / `Ctrl + ←` |
| Next / Previous file | `Page Down` / `Page Up` |
| Seek by percentage (10%–90%) | `1` – `9` (and `0` for start) |
| Open / Close sidebar | `Ctrl + L` |
| Open / Close YouTube | `Ctrl + Y` |
| Open / Close Radio | `Ctrl + R` |
| AI Subtitles | `S` |
| Set cut start / end point (A / B) | `[` / `]` |
| Export selection as a file | `Alt + S` |
| Add selection to cut bin | `Alt + B` |
| Audio Effects (EQ & Reverb) | `Shift + F` |
| Search subtitles online | `Ctrl + Alt + S` |
| Toggle subtitle reading | `Shift + R` |
| Toggle silence skip | `/` |
| Download YouTube video / audio | `Ctrl + D` |
| Settings | `Ctrl + P` |

All shortcuts are fully customizable from the Settings window.

## 📖 Documentation

User guides are bundled with the app and available in 7 languages:

- [English](User_guide/User_guide_en.html)
- العربية (Arabic) — [`User_guide_ar.html`](User_guide/User_guide_ar.html)
- Français (French) — [`User_guide_fr.html`](User_guide/User_guide_fr.html)
- Deutsch (German) — [`User_guide_de.html`](User_guide/User_guide_de.html)
- Español (Spanish) — [`User_guide_es.html`](User_guide/User_guide_es.html)
- Italiano (Italian) — [`User_guide_it.html`](User_guide/User_guide_it.html)
- Türkçe (Turkish) — [`User_guide_tr.html`](User_guide/User_guide_tr.html)

The guides cover overview, a dedicated blind-users guide, a sighted users guide, and a comprehensive shortcuts reference.

## 🔧 Building from Source

### Prerequisites

- Python 3.10+
- Windows 10/11 64-bit

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Build both executables (PlayAbility Pro + AI Subtitles)
python build_all.py

# Output: dist\PlayAbility Pro\
```

For a release installer, open `]setup Script.iss` with [Inno Setup](https://jrsoftware.org/isinfo.php) and compile it.

### Branch Layout

- `playAbility_main.py` is the entry point; the AI subsystem is a separate bundled app (`AI Subtitles`) that works standalone.

## 🗂️ Project Structure

| File | Purpose |
| --- | --- |
| `playAbility_main.py` | Entry point: MPV loading, single-instance mutex, radio recording worker |
| `UI.py` | Main window, menus, sidebar, settings, shortcut handling (wxPython) |
| `AI_subtitles.py` | AI transcription & translation engine (Whisper + Gemini + Groq) |
| `mighty_youtube.py` | YouTube search, playback, downloads, subscriptions (yt-dlp) |
| `radio_feature.py` | Radio UI, stations, favorites, recording, scheduling |
| `background_recorder.py` | Standalone recorder worker for scheduled radio recordings |
| `radio_os_tasks.py` | Windows Task Scheduler integration for recordings |
| `audio_effects.py` | Real-time equalizer and reverb effects |
| `subtitles.py` | Online subtitle search, download, and reading |
| `subtitle_editor.py` | SRT subtitle editor |
| `skip_silence.py` / `export_silence.py` | Silence detection, skipping, and export |
| `converter.py` | Universal format converter |
| `tag_editor.py` | Media tag (metadata) editor |
| `updater.py` | Updater with progress reporting and auto-update |
| `config.py` | Configuration, defaults, and translation system |
| `Langs/` | UI translations (ar, en, fr, de, es, it, tr) |
| `User_guide/` | Multilingual user guides |
| `]setup Script.iss` | Inno Setup installer script |

## 🧰 Technology Stack

- **Python 3** — core language
- **wxPython** — GUI framework
- **MPV (libmpv)** — media playback engine
- **yt-dlp** — YouTube search & downloads
- **faster-whisper** — offline speech-to-text transcription
- **Google Gemini & Groq** — AI translation & transcription
- **PyInstaller** — executable packaging
- **Inno Setup** — Windows installer

## 🌍 Supported Languages

The UI and user guides are available in: Arabic, English, French, German, Spanish, Italian, and Turkish.

## 📄 License

This software is provided free of charge under the terms of the **End User License Agreement (EULA)** included with the installer ([English](license_en.txt), [Arabic](license_ar.txt), [French](license_fr.txt)).

The software is intended solely for lawful use. You may use it for personal or professional playback, conversion, and translation; redistribution, modification, decompiling, or reverse engineering without prior written permission from the developer is prohibited. It is provided "AS IS" without warranty of any kind.

## 🤝 Contact & Support

- 👤 **Developer Telegram:** [t.me/Hamza_abo_slema](https://t.me/Hamza_abo_slema)
- 💬 **Community Telegram:** [t.me/Zawya_thaneya](https://t.me/Zawya_thaneya)
- 🐛 **Issues & Feedback:** [GitHub Issues](https://github.com/hamza-abo-slema/PlayAbility-pro-setup/issues)

## 🙏 Acknowledgements

Special thanks to the open-source projects that make playAbility pro possible: [MPV](https://mpv.io/), [yt-dlp](https://github.com/yt-dlp/yt-dlp), [faster-whisper](https://github.com/SYSTRAN/faster-whisper), [Google Generative AI](https://ai.google.dev/), [Groq](https://groq.com/), [wxPython](https://www.wxpython.org/), and [PyInstaller](https://pyinstaller.org/).

---

<div align="center">
  <sub>Developed with ❤️ by <strong>Hamza Abo Slema</strong> · Copyright © 2026 PAPH</sub>
</div>