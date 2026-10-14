Intro Video: https://drive.google.com/file/d/1aqQXdiRrjVXD3gWpY5SzSJVVJy0pcB8p/view?usp=sharing

So you want to put some zoomy zoomies in your life? Install me.

# Zoom-Zoom

**Zoom-Zoom is a DWM clone.** It is a lightweight, keyboard-driven X11 window manager based on the suckless DWM approach.

## Installation

### Arch Linux

Install the build dependencies:

```bash
sudo pacman -S --needed git base-devel libx11 libxft libxinerama
```

Clone and build Zoom-Zoom:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### Debian / Ubuntu

Install the build dependencies:

```bash
sudo apt update
sudo apt install git build-essential libx11-dev libxft-dev libxinerama-dev
```

Clone and build:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### Fedora

Install the build dependencies:

```bash
sudo dnf install git make gcc libX11-devel libXft-devel libXinerama-devel
```

Clone and build:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### openSUSE

Install the build dependencies:

```bash
sudo zypper install git make gcc libX11-devel libXft-devel libXinerama-devel
```

Clone and build:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### Void Linux

Install the build dependencies:

```bash
sudo xbps-install -S git make gcc libX11-devel libXft-devel libXinerama-devel
```

Clone and build:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### Alpine Linux

Install the build dependencies:

```bash
sudo apk add git make gcc musl-dev libx11-dev libxft-dev libxinerama-dev
```

Clone and build:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
sudo make install
```

### Nix / NixOS

Enter a temporary development environment with the required build tools and X11 libraries:

```bash
nix shell nixpkgs#gcc nixpkgs#gnumake nixpkgs#pkg-config nixpkgs#xorg.libX11 nixpkgs#xorg.libXft nixpkgs#xorg.libXinerama
```

Clone and build Zoom-Zoom:

```bash
git clone https://github.com/CalebH245/zoom-zoom.git
cd zoom-zoom
make
```

To install the compiled window manager using the Makefile's default prefix:

```bash
sudo make install
```

On NixOS, a declarative Nix package or system configuration is recommended for a persistent system-managed installation.

## Running Zoom-Zoom

Zoom-Zoom is an X11 window manager. An X server must be installed and configured before it can be used.

To start Zoom-Zoom with `startx`, add the following line to `~/.xinitrc`:

```bash
exec dwm
```

Log in through a TTY and run:

```bash
startx
```

Alternatively, configure Zoom-Zoom as an X11 session in your display manager.

## Dependencies

- Git
- A C compiler
- Make
- X11 development libraries
- Xft
- Xinerama

The optional default keyboard shortcuts may also require `st` (terminal) and `dmenu` (application launcher).

## Configuration

Configuration is managed through `config.h` and the project's build configuration. After changing the configuration, rebuild and reinstall:

```bash
make clean
make
sudo make install
```

## Updating

To update your local clone:

```bash
cd zoom-zoom
git pull
make clean
make
sudo make install
```

## Uninstalling

From the cloned repository, run:

```bash
sudo make uninstall
```

## Source

[GitHub Repository](https://github.com/CalebH245/zoom-zoom)
