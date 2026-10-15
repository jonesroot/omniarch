# Chat Suite — Arch Linux App Suite

Installer + uninstaller TUI (whiptail) buat Arch Linux: WhatsApp PWA,
ZapZap, Telegram, Discord, Vesktop, Signal, Slack, Zoom, Ferdium,
Instagram/YouTube/X PWA, LibreOffice, OnlyOffice, Office365 PWA,
BleachBit, VLC, MPV, Celluloid, Spotify, GIMP, OBS, Steam, Lutris,
Heroic, PrismLauncher, Snapper, Timeshift, pacman-contrib.

> File `.bin` di sini hasil compile (shc) — kode sumber tidak
> dipublikasikan. Lihat `CARA-PAKAI.txt` buat instruksi.

## Isi rilis

| File | Keterangan |
| --- | --- |
| `install-chat-suite.bin` | Installer utama |
| `uninstall-chat-suite.bin` | Uninstaller (keep/purge data) |
| `VERSION` | Versi rilis saat ini (dipakai self-update) |
| `SHA256SUMS` | Checksum binary (wajib cocok saat self-update) |
| `CARA-PAKAI.txt` | Instruksi buat pengguna |

## Cara pakai

```bash
chmod +x *.bin
./install-chat-suite.bin
```

## Bikin rilis baru (author)

```bash
# 1. Naikkan VERSION di install-chat-suite.sh
# 2. Compile ulang:
shc -r -f install-chat-suite.sh -o install-chat-suite.bin   # (dari copy bershebang /bin/bash)
shc -r -f uninstall-chat-suite.sh -o uninstall-chat-suite.bin
# 3. Refresh metadata:
echo "<VERSI>" > VERSION
sha256sum ./*.bin > SHA256SUMS
# 4. Commit + push — user lama otomatis ditawarin update
```

Atau cukup jalankan `./build.sh` (lihat repo lokal author).
