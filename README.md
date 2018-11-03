# PopcornTime-flatpak
PopcornTime Flatpak package (unoffical)

## TODO:
- [ ] Contact upstream to use it as an official distribution system
- [ ] Looking for a way to allow external players (might not be possible with flatpak)


## How to build:
1 - Install [Flatpak](https://flatpak.org/setup/) & flatpak-builder

2 - Add Flathub remote

```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```


3 - Clone the repository

```
git clone https://gitlab.com/Preisschild/popcorntime-flatpak
cd ./popcorntime-flatpak
``` 

4 - Build & Install the Flatpak package
```
flatpak-builder --install --install-deps-from=flathub popcorntime sh.popcorntime.PopcornTime.yml
```
