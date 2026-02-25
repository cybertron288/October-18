<p align="center">
  <img src="Design/banner.svg" alt="October-18" width="900"/>
</p>

<p align="center">
  A macOS screen saver featuring 90+ animations from Apple's Brooklyn event — rebuilt for Apple Silicon and modern macOS.
</p>

<p align="center">
  <a href="https://github.com/cybertron288/October-18/releases"><img src="https://img.shields.io/github/downloads/cybertron288/October-18/total.svg?style=flat-square" alt="Downloads"/></a>
  <a href="https://github.com/cybertron288/October-18/actions/workflows/build.yml"><img src="https://img.shields.io/github/actions/workflow/status/cybertron288/October-18/build.yml?style=flat-square" alt="Build"/></a>
  <img src="https://img.shields.io/badge/macOS-13%2B-black?style=flat-square" alt="macOS 13+"/>
  <img src="https://img.shields.io/badge/Swift-5-orange?style=flat-square" alt="Swift 5"/>
  <a href="https://github.com/cybertron288/October-18/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square" alt="MIT License"/></a>
</p>

---

### Highlights

- **Apple Silicon Native** — Universal binary, no Rosetta required
- **90+ Animations** — Stunning visuals from Apple's October 2018 event
- **Fully Offline** — No internet connection needed

---

## Installation

Close **System Settings** before installing.

### Homebrew (recommended)

```sh
brew install --cask cybertron288/tap/october-18 --no-quarantine
```

### Manual

1. Download the latest `October18.saver.zip` from [Releases](https://github.com/cybertron288/October-18/releases/latest)
2. Unzip and double-click **October18.saver**

### Set as active screen saver via Terminal

```sh
defaults -currentHost write com.apple.screensaver moduleDict -dict moduleName October18 path "$HOME/Library/Screen Savers/October18.saver"
```

## Compatibility

| Requirement | Minimum |
|---|---|
| macOS | 13 Ventura |
| Architecture | Apple Silicon (native) + Intel |

## Troubleshooting

macOS may block the screen saver because it is from an unidentified developer.

**System Settings**

Open **Privacy & Security**, scroll down to the blocked message, and click **Open Anyway**.

**Terminal**

```sh
sudo xattr -d com.apple.quarantine ~/Library/Screen\ Savers/October18.saver
```

## Building from Source

```sh
xcodebuild -project October18.xcodeproj \
  -scheme October18 \
  -configuration Release \
  ARCHS="arm64 x86_64" \
  build
```

## Acknowledgments

Originally created by [Pedro Carrasco](https://github.com/pedrommcarrasco/Brooklyn). Animations and logo are Apple's property.

## License

MIT — see [LICENSE](https://github.com/cybertron288/October-18/blob/main/LICENSE) for details.
