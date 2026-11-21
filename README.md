# VELTRIX Dock

**A self-hosted control plane and Android/Termux agent.**

VELTRIX Dock lets you manage services and connected devices from a web-based Control Plane.

## Documentation

- **Documentation:** https://docs.veltrix.com
- **Downloads and releases:** https://github.com/NexLab-ceo/veltrix-dock/releases
- **Source code:** https://github.com/NexLab-ceo/Yevqo

## Installation

Download the .deb package matching your use case from the [latest release](https://github.com/NexLab-ceo/veltrix-dock/releases/latest). Releases are published automatically by the Yevqo build workflow and include both packages plus a SHA-256 checksum file. Installed packages check for updates automatically every six hours.

In Termux, install the required dependencies and then install the selected package:

    pkg update
    pkg install mariadb php git termux-services
    pkg install ./yevqo-all_<version>_aarch64.deb

For an Agent-only device:

    pkg update
    pkg install php git termux-services
    pkg install ./yevqo_<version>_aarch64.deb

Replace <version> with the version in the downloaded filename. Install **one** package per device: yevqo-all for the Control Plane host (which also includes the Agent), or yevqo for a remote Agent. If both files are present, do not use the wildcard pkg install ./yevqo*.deb, as it may select both packages.

## Packages

| Package | Contents | Intended use |
|---|---|---|
| yevqo-all | Control Plane, Agent, web assets, migrations and setup scripts | Developer / master phone |
| yevqo | Agent and its setup script | Remote device |

## License

VELTRIX Dock is freeware, not open source. Personal, educational and non-commercial use is free. Commercial use requires a separate license. See [LICENSE](LICENSE) and [LICENSE.ru.md](LICENSE.ru.md).

---

© 2026 NexLab. All rights reserved.
