# SimpleDeckyTDP

[![](https://img.shields.io/github/downloads/fewtarius/SimpleDeckyTDP/total.svg)](https://github.com/fewtarius/SimpleDeckyTDP/releases)

This is a variant of SimpleDeckyTDP for my personal use, it is only tested on my systems.  Use at your own risk.

# Install

### Prerequisites

Decky Loader must already be installed. If using ryzenadj for TDP control, secure boot must be disabled.

### Quick Install / Update

Run the following in terminal, then reboot. Note that this works both for installing or updating the plugin

```
curl -L https://github.com/fewtarius/SimpleDeckyTDP/raw/main/install.sh | sh
```

### Manual Install

Download the latest release from the [releases page](https://github.com/fewtarius/SimpleDeckyTDP/releases)

Unzip the `tar.gz` file, and move the `SimpleDeckyTDP` folder to your `$HOME/homebrew/plugins` directory

then run:

```
sudo systemctl restart plugin_loader.service
```

then reboot your machine.

## Manual build

Dependencies:

- Node.js v16.14+ and pnpm installed
- fully functional ryzenadj

```bash
git clone https://github.com/fewtarius/SimpleDeckyTDP.git

cd SimpleDeckyTDP

# if pnpm not already installed
npm install -g pnpm

pnpm install
pnpm update @decky/ui --latest
pnpm run build
```

Afterwards, you can place the entire `SimpleDeckyTDP` folder in the `~/homebrew/plugins` directly, then restart your plugin service

```bash
sudo systemctl restart plugin_loader.service

sudo systemctl reboot
```

### Uninstall Instructions

In Desktop mode, run the following in terminal:

```bash
sudo rm -rf $HOME/homebrew/plugins/SimpleDeckyTDP
sudo systemctl restart plugin_loader.service
```

# Attribution

Thanks to the following for making this plugin possible:

- [SimpleDeckyTDP](https://github.com/aarron-lee/SimpleDeckyTDP)
- [hhd-adjustor](https://github.com/hhd-dev/adjustor/)
- [hhd-hwinfo](https://github.com/hhd-dev/hwinfo)
- [decky loader](https://github.com/SteamDeckHomebrew/decky-loader/)
- [ryzenadj](https://github.com/FlyGoat/RyzenAdj)
