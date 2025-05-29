# 🖥️ xrandr — X11 CLI Tool for Display Configuration

**xrandr** (X Resize, Rotate and Reflect) is a standard command-line utility for managing displays in X11. It allows you to set screen resolution, orientation, position, and more — all without restarting your session.

---

## ✅ Features

* Full control over display settings via CLI
* Support for multiple monitors
* Set position, rotation, enable/disable outputs
* Lightweight, no GUI required
* Ideal for window managers like i3, bspwm, Openbox, etc.

---

## 🔧 Installation

### Debian / Ubuntu

```bash
sudo apt install x11-xserver-utils
```

### Arch Linux

```bash
sudo pacman -S xorg-xrandr
```

### Fedora

```bash
sudo dnf install xrandr
```

---

## 🚀 Basic Usage

```bash
xrandr
```

Lists all connected displays, their resolutions, and current status.

---

## ⚙️ Command-Line Options

| Option                    | Description                                   |          |                |
| ------------------------- | --------------------------------------------- | -------- | -------------- |
| `--output <name>`         | Select the display/output to configure        |          |                |
| `--mode <resolution>`     | Set the resolution (e.g. 1920x1080)           |          |                |
| `--primary`               | Mark output as the primary display            |          |                |
| `--left-of`, `--right-of` | Position display to the left/right of another |          |                |
| `--same-as`               | Mirror the display                            |          |                |
| `--off`                   | Disable the display                           |          |                |
| \`--rotate left           | right                                         | normal\` | Rotate display |
| `--auto`                  | Automatically enable with best resolution     |          |                |

---

## 🎯 Examples

### Enable external monitor to the right of laptop screen:

```bash
xrandr --output HDMI-1 --auto --right-of eDP-1
```

### Disable secondary monitor:

```bash
xrandr --output HDMI-1 --off
```

### Change resolution of internal display:

```bash
xrandr --output eDP-1 --mode 1366x768
```

### Rotate screen vertically:

```bash
xrandr --output HDMI-1 --rotate left
```

### Mirror two screens:

```bash
xrandr --output HDMI-1 --same-as eDP-1
```

---

## 📂 Sample Output

```
Screen 0: minimum 8 x 8, current 3840 x 1080, maximum 32767 x 32767
eDP-1 connected primary 1920x1080+0+0
HDMI-1 connected 1920x1080+1920+0
```

---

## 📚 More Info

* Manual:

```bash
man xrandr
```

* Arch Wiki: [https://wiki.archlinux.org/title/Xrandr](https://wiki.archlinux.org/title/Xrandr)

---

## 🧩 Alternatives

* `arandr` — GUI frontend for xrandr
* `lxrandr` — Lightweight graphical interface
* `wallutils` — CLI utility with multi-monitor support
