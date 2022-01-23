# gMKVExtractGUI Flatpak

📦 Flatpak Package of gMKVExtractGUI for Linux

gMKVExtractGUI is a small GUI utility to use mkvinfo and mkvextract cli tools from MKVToolnix pack, in order to extract tracks, chapters and CUE sheets from mkv files.  
It runs on Linux using Mono. The "source" (build v2.5.2 from [SourceForge](https://sourceforge.net/projects/gmkvextractgui/files/)) is included here as a .tar.xz file because flatpak can't use .7z files.

Find out more here: https://forum.doom9.org/showthread.php?t=170249

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/net.sourceforge.gMKVExtractGUI.flatpakref
```

You can also install it from the bundle in Releases on GitHub, but you won't get updates that way.

## Building

### Install SDK, Platform and mono6 Extension

```bash
flatpak install flathub org.kde.Sdk//5.15
flatpak install flathub org.kde.Platform//5.15
flatpak install flathub org.freedesktop.Sdk.Extension.mono6//20.08
```

### Build and install for user

```bash
flatpak-builder --user --install --force-clean build-dir net.sourceforge.gMKVExtractGUI.yml
```

### Build to repo

```bash
flatpak-builder --repo=repo --force-clean build-dir net.sourceforge.gMKVExtractGUI.yml
```

### Make single-file bundle from repo

```bash
flatpak build-bundle repo gMKVExtractGUI.flatpak net.sourceforge.gMKVExtractGUI stable --runtime-repo="https://flathub.org/repo/flathub.flatpakrepo"
```
