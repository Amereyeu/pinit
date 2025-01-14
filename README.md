# Pin It!
Pin shortcuts for portable apps like raw executable files, AppImage files, etc. to the app launcher on your desktop.

![Files view in the light mode](data/screenshots/gnome/screenshot-files-view-light.png)

![Edit view in the light mode](data/screenshots/gnome/screenshot-edit-view-light.png)

Other features include:

- Edit or delete created app entries without opening the file manager
- Automatically add execution permission to the file you select

## Installation
### From Flathub (Recommended)
You can download the app from Flathub, which should make this app available for all Linux distribution:

[<img src="https://flathub.org/assets/badges/flathub-badge-en.svg" width="160" alt="Download on Flathub">](https://flathub.org/apps/com.github.ryonakano.pinit)

### From Source Code (Flatpak)
If you would like to test latest source code, clone the repository and then run the following command:

```
flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install -y --user flathub org.flatpak.Builder
flatpak run org.flatpak.Builder builddir-flatpak --user --install --force-clean --install-deps-from=flathub com.github.ryonakano.pinit.yml
```

### From Source Code (Native)
You'll need the following dependencies to build:

* libadwaita-1-dev (>= 1.4.0)
* libgee-0.8-dev
* libglib2.0-dev (>= 2.74)
* libgtk-4-dev (>= 4.10)
* meson (>= 0.57.0)
* valac

Run `meson setup` to configure the build environment and run `meson compile` to build:

```bash
meson setup builddir --prefix=/usr
meson compile -C builddir
```

To install, use `meson install`, then execute with `com.github.ryonakano.pinit`:

```bash
meson install -C builddir
com.github.ryonakano.pinit
```

## Contributing

Please refer to [the contribution guideline](CONTRIBUTING.md) if you would like to:

- submit bug reports / feature requests
- propose coding changes
- translate the project

## Get Support

Need help in use of the app? Refer to [the discussions page](https://github.com/ryonakano/pinit/discussions) to search for existing discussions or [start a new discussion](https://github.com/ryonakano/pinit/discussions/new/choose) if none is relevant.

## History
The original idea of the app is inspired from [Desktopius by Alex K](https://github.com/alexkdeveloper/dfc).
