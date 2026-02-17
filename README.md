# ✨ Project Essential GNOME Theme

A premium, monochromatic desktop suite for GNOME, inspired by the high-contrast and structural design language of **Nothing OS**. This theme is the visual core of the **Project Essential** ecosystem, designed to provide a distraction-free, "essential" computing experience.

---

## 📷 Screenshots

![Image](PROJECT-ESSENTIAL-GNOME-THEME.jpg)


---

## 🚀 Features

* ⚙️ **Essential Shell** — Full support for GNOME 45+ Shell, featuring custom dot-matrix activity indicators and frosted glass panels.
* 🎨 **GTK 4 / Libadwaita** — Modern monochromatic styling for system apps and settings.
* 🧱 **Eww Dashboards** — Floating "Essential" widgets for time, weather, and system telemetry.
* 📉 **Conky Minimalism** — A lightweight, persistent desktop clock and system monitor.
* 🖼 **Official Wallpapers** — Curated backgrounds optimized for the Project Essential palette.

---

## 🧰 Dependencies

To ensure all elements (blur, widgets, and fonts) render correctly, install the following:

### 📦 Debian 13 (Trixie) / Ubuntu

```bash
# System Tools
sudo apt update && sudo apt install -y gnome-tweaks gnome-shell-extension-manager conky-all git alacritty

# Eww (Widgets) Dependencies
sudo apt install -y libgtk-3-dev libglib2.0-dev libpango1.0-dev libgdk-pixbuf2.0-dev libjson-glib-dev rustc cargo

```

---

## 🛠 Installation

### 1. Clone the Official Repo

```bash
git clone https://github.com/dixon-team-tech/project-essential-gnome-theme/
cd project-essential-gnome-theme

```

### 2. Deploy Configs & Themes

Use the following commands to move the assets to their correct locations:

```bash
# Setup Themes and Icons
mkdir -p ~/.themes ~/.icons
cp -r themes/* ~/.themes/
cp -r icons/* ~/.icons/

# Setup App Configs
cp -r config/alacritty ~/.config/
cp -r config/eww ~/.config/
cp -r config/conky ~/.config/

```

### 3. Application Settings

Open **GNOME Tweaks** and apply:

* **Legacy Applications:** `Project-Essential-GTK`
* **Shell Theme:** `Project-Essential-Shell` *(Requires 'User Themes' extension)*
* **Icons:** `Project-Essential-Icons`
* **Typography:** Set all fonts to **Inter** or **NDot 57**.

---

## 🌦 Widget Activation

Project Essential uses **Eww** for its signature widgets.

```bash
# Start the widget daemon
eww daemon

# Launch the primary dashboard
eww open essential-status

```

---

## 📢 Credits
Inspired by the **NothingOS** design language  
* **Developed by:** Dixon Team Tech - Creators of the Project ESSENTIAL Distro
* **Design Inspiration:** Nothing OS and HyenaDesign
* **Core Technologies:** GNOME, Eww, Conky

---

## 🔗 Official Repository

[https://github.com/dixon-team-tech/project-essential-gnome-theme/]()

## 📢 📢 📢 📢 License

This project is released under the [GPL3 License](LICENSE), unless otherwise noted.


---

