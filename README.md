# Tauri + Leptos

```bash
cargo install cargo-leptos leptosfmt trunk tauri-cli
rustup target add wasm32-unknown-unknown
```

### Arch
```bash
sudo pacman -S --needed webkit2gtk-4.1 base-devel curl wget file openssl appmenu-gtk-module libappindicator-gtk3 librsvg xdotool
```

# How do

## Development

```bash
# Desktop
cargo tauri dev
# Android
cargo tauri ios dev
# iOS
cargo tauri ios dev
```

## Build
```bash

# windows
# Do this on windows and don't make it complicated
tauri build

# android
# Play store
cargo tauri android build --aab
# external
cargo tauri android build --apk

# universal-apple/ios
rustup target add aarch64-apple-darwin
rustup target add x86_64-apple-darwin
cargo tauri build --no-bundle
cargo tauri bundle --bundles app --target universal-apple-darwin --config src-tauri/tauri.appstore.conf.json

# bundle for App Store distribution
cargo tauri build --no-bundle
cargo tauri bundle --bundles app --config src-tauri/tauri.appstore.conf.json

# bundle for distribution outside the macOS App Store
cargo tauri build --no-bundle
cargo tauri build --bundles app,dmg
