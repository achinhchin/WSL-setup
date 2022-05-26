# **My Windows Subsystem for Linux setup**
This is my WSL setup, and it's for run linux terminal while running Windows.
“Out of 130 tests in total, Windows 11 WSL2 Ubuntu 20.04 LTS managed to run at 94% the speed of bare metal Ubuntu 20.04 LTS on the same system.

![screenshot](https://github.com/chinhchin/wsl-setup/blob/master/readme-assets/screenshot.png?raw=true)

### **Go to**
- **[Verison record](./version-record.json)**
- see how to get cool and productive [Windows Terminal](https://github.com/chinhchin/Windows-Terminal-setup.git)

### **OS requirement**
- Windows 10, 11

### **Contents**
#### 1. [Install and setup](./readmd.md#1-install-and-setup)
1. [Turn on WSL feature](./readmd.md#11-turn-on-wsl-feature)
2. [Install 2 softwares from Microsoft Store](./readmd.md#12-install-wsl)
#### 2. [Running Ubuntu](./readmd.md#2-running-ubuntu)

---

## **1. Prepare for install WSL**

### **1.1 Run powershell as Administrator**
1. Press "*Windows*" button on keyboard.
2. Type "*Powershell*".
3. At the right pane of search window press Run as Administrator.

### **1.2 Prepare to install WSL**
1. enable WSL
```
dism /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

2. enable VirtualMachinePlatform
```
dism /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

3. Download and install [WSL2 Linux kernel update package for x64 machines
 Note](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

4. Set WSL-2 as default
```
wsl --set-default-version 2
```

5. Restart your computer

## **2 Install WSL and Linux**

### **2.1 Install WSL** 
1. Install [Ubuntu](https://www.microsoft.com/store/productId/9PDXGNCFSCZV).

### **2.2 Install Linux on WSL**
1. **Open with ubuntu app**: Press "*Windows*" button, type "*Ubuntu*", then press "*Enter*".

