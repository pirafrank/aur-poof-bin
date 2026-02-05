# AUR poof-bin package

<https://aur.archlinux.org/packages/poof-bin>

## Pre

```sh
pacman -Sy
pacman -S namcap
```

## Build

```sh
# edit PKGBUILD file
nvim PKGBUILD
# generate
makepkg --printsrcinfo > .SRCINFO
# test
namcap PKGBUILD
# commit and push
git add . && git commit -S -m "Publish vX.Y.Z" && git push
```
