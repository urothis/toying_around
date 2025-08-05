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
cargo tauri build
