# gMKVExtractGUI Flatpak

📦 Flatpak Package of gMKVExtractGUI for Linux

gMKVExtractGUI is a small GUI utility to use mkvinfo and mkvextract cli tools from MKVToolnix pack, in order to extract tracks, chapters and CUE sheets from mkv files.  

It runs on Linux using Mono.  
The "source" (build from [SourceForge](https://sourceforge.net/projects/gmkvextractgui/files/)) is included here as a .tar.xz file because flatpak-builder can't handle .7z files.

Find out more about gMKVExtractGUI here: <https://forum.doom9.org/showthread.php?t=170249>

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/repo/appstream/net.sourceforge.gMKVExtractGUI.flatpakref
```

You also need to install the mono6 extension for gMKVExtractGUI to work:

```bash
flatpak install flathub org.freedesktop.Sdk.Extension.mono6//22.08
```

## Building

```bash
flatpak install flathub org.freedesktop.Sdk.Extension.mono6//22.08
flatpak-builder --install-deps-from=flathub --force-clean build-dir net.sourceforge.gMKVExtractGUI.yml
```
