# Archinstall

## 1. ISO Installation

Download ISO from [archlinux.org/download/]() -> Scroll down to Swiss Mirrors

## 2. Start Installation

### 2.1 Set Keyboard Layout

Set keyboard layout to Swiss German with this:

```
loadkeys de_CH-latin1
```

### 2.2 Set WLAN Connection

1. Start Wireless Daemon (iwctl)

        iwctl

2. Show available devices

        device list

3. Scan available networks

        station <device> scan

4. Show available networks

        station <device> get-networks

5. Connect to a network

        station <device> connect <SSID>

6. Check connection

        station <device> show


7. Exit the IWCTl with `exit`

### 2.3 Archinstall

Start the installation process with `archinstall`

#### 2.3.1 Locales

**Set locales:**

- **Keyboard Layout**: `de_CH-latin1`
- **Locale Language**: `en_US.UTF-8`
- **Locale Encoding**: `UTF-8`

#### 2.3.2 Mirrors

- **Mirror Region**: `Switzerland`

#### 2.3.3 Disk Configuration

- **Use best-effort default partition layout**

  - Select Disk
  - Filesystem: `BTRFS` (with `subvolumes with a default structure` and `compression`)

#### 2.3.4 Bootloader

- **Bootloader**: `grub`

#### 2.3.5 Hostname

Set Hostname

#### 2.3.6 Authentication

- Create User Account and add it to the super user group

#### 2.3.7 Profile

- **Profile Type**: `Desktop`
- **Desktop**: `Hyprland` (polkit)

#### 2.3.8 Applications

- **Audio**: `pipewire`
- **Bluetooth**: `Enabled`

#### 2.3.9 Network Configuration

- Copy ISO network configuration to installation

#### 2.3.10 Timezone

- **Timezone**: `Europe/Zurich`

#### 2.3.11 Install

Install the configuration.

#### 2.3.12 Exit and Shutdown

Exit the Archinstall and Shutdown:

```
shutdown -h now
```

### 2.4 Post Archinstall (Hyprland)

#### 2.4.1 Change Keyboard Layout

- Edit the file `~/.config/hypr/hyprland.conf`
- Scroll down to the `INPUT` Section:
  - kb_layout = ch

> See the file `/usr/share/X11/xkb/rules/base.lst` for available Keyboard Layouts.

#### 2.4.2 Install Firefox

```
sudo pacman -S firefox
```

### 2.5 My Linux for Work (ML4W-Dotfiles)

#### 2.5.1 Install Flatpak

```
sudo pacman -S flatpak
```

### 2.5.2 Dotfiles installer

- Open https://mylinuxforwork.github.io/dotfiles
- Execute the Install-Command on the flathub-install page
- Execute the Run-Command on the flathub-install page
- Copy the link of the Rolling-Release (or Stable) into the Dotfiles installer
- Execute the Install-Script-Command
  - AUR-Helper: `yay`
- Backup existing Configuration
- Change Settings (Keyboard Layout, Default Terminal etc.)






