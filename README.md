# StraitSim for Windows

Pilot ships through the Singapore Strait, with live traffic, chart, radar, passage planning and review.

**[Download the Windows installer](https://github.com/wyxlester/straitsim-downloads/releases/latest/download/StraitSim-Setup-Windows-x64.exe)**

[Release details and checksum](https://github.com/wyxlester/straitsim-downloads/releases/latest)

## Install and play

1. Download `StraitSim-Setup-Windows-x64.exe` (approximately 1.04 GB).
2. Run the installer. It installs StraitSim for your Windows user and creates Start-menu and desktop shortcuts.
3. Double-click **StraitSim** to play. No Unreal Editor, Git, terminal, or separate Python installation is required.

The application uses about 2.12 GB after installation. Allow 10 GB free space for download, setup and saves. Saves and logs are stored under `%LOCALAPPDATA%\StraitSim`; uninstalling preserves them.

This is an unsigned preview build. It has been installed, tested, uninstalled, reinstalled and relaunched on the build PC. A separate clean-PC/laptop test is still pending.

## Provisional minimum laptop requirements

These are conservative planning estimates, **not measured minimum specifications or a guaranteed frame-rate target**. Low-end hardware has not yet been benchmarked.

| Component | Provisional requirement |
| --- | --- |
| OS | Windows 11, 64-bit Intel/AMD (x64) |
| CPU | Modern Intel/AMD quad-core processor, approximately 3 GHz or faster |
| Memory | 16 GB RAM |
| Graphics | Dedicated DirectX 12-compatible GPU with 6 GB VRAM and current drivers |
| Storage | 10 GB free space; SSD recommended |
| Display | At least 1440 x 900; 1920 x 1080 recommended |
| Controls | Keyboard and mouse with a scroll wheel |

Windows on ARM and integrated-only graphics have not been validated. Windows 10 compatibility has not been separately tested. The launcher currently opens a 1440 x 900 window.

**Validated hardware:** Windows 11 25H2, Intel Core Ultra 7 265KF, NVIDIA GeForce RTX 5070 Ti, 64 GB RAM. This is the tested machine, not a claim that this hardware is the minimum.

Epic's [engine hardware documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/hardware-and-software-specifications-for-unreal-engine) describes graphics/API support and editor recommendations; it does not establish this game's minimum performance requirements.

## What was tested

- 18 native checks on both packaged and installed applications: zero failures or skips. Two checks emitted transient test-world cleanup warnings.
- PCG wheel/keyboard steering, linked and split power, neutral, engine feedback, pause protection, speed/course hold and manual takeover.
- Passage review -> New passage -> select another ship -> fresh plan -> sail; Edit passage plan preserves the current ship and route.
- Windows shell launches of the installed Start-menu and desktop shortcuts, normal close/reopen, and uninstall/reinstall with 40 saved review files unchanged.
- Bundled runtime with restricted PATH and invalid external Python settings; no development Python was required. The network was not disconnected during this check.
- 12 PCG power-reduction regressions passed, including the standalone C++ comparison, without skips.

The public release contains the playable installer and checksum. The development repository and source/assets build kit are separate and remain private.
