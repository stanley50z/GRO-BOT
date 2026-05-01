# GRO-BOT

GRO-BOT is a smart algae bioreactor project hub. This repository hosts the public project website and links the companion firmware and iOS app repositories as submodules.

Live site: https://stanley50z.github.io/GRO-BOT/

## Repository Contents

- `index.html` - static project website
- `images/` - website images and diagrams
- `gro-bot-esp32/` - ESP32 firmware submodule
- `AgTech-App/` - iOS app submodule

## Submodules

This repository tracks the firmware and app repositories as submodules:

- ESP32 firmware: https://github.com/stanley50z/gro-bot-esp32.git
- iOS app: https://github.com/vchallans/AgTech-App.git

Clone everything with:

```sh
git clone --recurse-submodules https://github.com/stanley50z/GRO-BOT.git
```

If you already cloned the repo without submodules:

```sh
git submodule update --init --recursive
```

## Website Deployment

The website is deployed with GitHub Pages from the `main` branch using the workflow in `.github/workflows/pages.yml`.

The ESP32 firmware repository is private, so the Pages workflow checks out this repository without recursively cloning submodules. That keeps the public website deploy independent from private firmware access.
