---
title: Fresh Install Magento
createDate: 2024-12-10
updateDate: 2024-12-10
excerpt: 
tags: 
draft: false
published: false
---
> [!warning] This note for me only
## Create boot Installer USB
- Download a full macOS installer from Apple
- Format USB to "MacOS Extended" (USB must be >= 32GB)
- Use terminal to create the bootable installer

```shell
# Sequoia
sudo /Applications/Install\ macOS\ Sequoia.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

# Sonoma
sudo /Applications/Install\ macOS\ Sonoma.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

# Ventura
sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

## Keyboard & Trackpad Settings
Go