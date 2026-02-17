# ✨ NothingOS GNOME – A Minimalist, Monochromatic Desktop Environment**
This repository contains a curated NothingOS-inspired desktop environment for GNOME. Designed for those who value the "Essential," it brings the clean, monochrome aesthetic of Nothing’s design language to Linux—focusing on polished typography, glassmorphism, and structural simplicity.

📷 Screenshots
[Place your updated screenshots here showing the GNOME Shell and Eww widgets in action]

🚀 Theme Components
⚙️ Essential Shell — A custom GNOME Shell theme that styles the top panel, notifications, and search.

🎨 GTK Theme — Dark/Light monochromatic styles for application windows.

🧱 Eww Widgets — Custom interactive widgets (Time, System Stats, Music) built with Elkowar's Wacky Widgets.

📈 Conky Lite — A distraction-free system monitor for the minimalist desktop.

🖼 Wallpapers — A collection of high-resolution, Nothing-inspired wallpapers.

🧰 Dependencies
Before installing, ensure your system has the following tools.

📦 Install on Debian / Ubuntu / Pop!_OS
Bash
# Core Tools
sudo apt update && sudo apt install -y gnome-tweaks gnome-shell-extensions conky-all git alacritty

# Eww Build Dependencies (Build from source for best performance)
sudo apt install -y libgtk-3-dev libglib2.0-dev libpango1.0-dev libgdk-pixbuf2.0-dev libjson-glib-dev rustc cargo
📦 Install on Arch / Manjaro
Bash
sudo pacman -S gnome-tweaks gnome-shell-extensions conky alacritty eww
🛠 Installation
1. Clone the Repository
Bash
git clone https://github.com/HyenaDesign/nothingos-gnome-manjaro
cd nothingos-gnome-manjaro
2. Deploy Assets
Configs are modular. You can choose to copy the entire suite or just specific parts:

Bash
# Copy Application & Shell Themes
mkdir -p ~/.themes && cp -r .themes/* ~/.themes/

# Copy Icons
mkdir -p ~/.icons && cp -r .icons/* ~/.icons/

# Copy Widget & Terminal Configs
cp -r .config/alacritty ~/.config/
cp -r .config/eww ~/.config/
cp -r .config/conky ~/.config/
3. Apply via GNOME Tweaks
Open GNOME Tweaks.

Navigate to Appearance.

Set Legacy Applications to NothingOS-GTK.

Set Shell to NothingOS-Shell (Requires "User Themes" extension enabled).

Set Icons to NothingOS-Icons.

🌦 Widget Configuration (Eww)
To use the interactive dashboard, ensure the eww daemon is running.

Bash
# Start the daemon
eww daemon

# Open the NothingOS Dashboard
eww open nothing-dashboard
To set your weather location, edit your API key in ~/.config/eww/scripts/get-weather.sh.

🙋 FAQ
Q: Does this work on Wayland? A: The Shell and GTK themes work perfectly. Some Eww widgets may require specific configuration for Wayland layers; check the eww.yuck file for details.

Q: How do I change the font to the Dot-Matrix style? A: Install the NDot 57 font and select it as the "Interface Font" in GNOME Tweaks.

❤️ Credits
Design Philosophy: Inspired by Nothing.

Icons: Based on the Papirus Development Team.

Widgets: Built using Eww and Conky.
