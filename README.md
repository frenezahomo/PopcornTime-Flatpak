# PopcornTime-flatpak
PopcornTime Flatpak package (unoffical)

## TODO:
- [ ] Contact upstream to use it as an official distribution system
- [ ] Get a dynamic mirror link instead of "mirror03.popcorntime.sh"
- [ ] Looking for a way to allow external players (might not be possible with flatpak)


## How to build:
1 - Install [Flatpak](https://flatpak.org/setup/) & flatpak-builder

2 - Add Flathub remote

```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

3 - Install freedesktop's runtime

```bash
flatpak install flathub org.freedesktop.Platform//18.08
flatpak install flathub org.freedesktop.Sdk//18.08
```

4 - Install Electron's BaseApp

```
flatpak install flathub org.electronjs.Electron2.BaseApp//stable
```

5 - Clone the repository

```
git clone --recurse-submodules https://gitlab.com/Preisschild/popcorntime-flatpak
cd ./popcorntime-flatpak
``` 

6 - Build & Install the Flatpak package
```
flatpak-builder --install popcorntime sh.popcorntime.PopcornTime.yml
```
