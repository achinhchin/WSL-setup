# **My Windows Subsystem for Linux setup**
This is my WSL setup, and it's for run linux terminal while running Windows.
“Out of 130 tests in total, Windows 11 WSL2 Ubuntu 20.04 LTS managed to run at 94% the speed of bare metal Ubuntu 20.04 LTS on the same system.

### **Preview Image**
![screenshot](https://github.com/chinhchin/wsl-setup/blob/master/readme-assets/screenshot.png?raw=true)

### **Go to**
- [Verison record](./version-record.json).
- See how to get cool and productive [Windows Terminal](https://github.com/chinhchin/Windows-Terminal-setup.git).

### **Credits**
- Inspiration, list of modules and solution from [craftzdog/dotfiles-public](https://github.com/craftzdog/dotfiles-public.git).

### **OS support**
- Windows 10, 11

### **Contents**
#### 1. [Prepare to install WSL](./readme.md#1-prepare-to-install-wsl)
1. [Install Windows Subsystem for Linux Preview](./readme.md#12-install-windows-subsystem-for-linux-preview-for-windows-11-build-22000-or-windows-11-insider-preview-builds-21362-only)
2. [Install vGPU driver](./readme.md#13-install-vgpu-driver) 3. [Run powershell as Administrator](./readme.md#11-run-powershell-as-administrator)
4. [Install WSL and Linux](./readme.md#2-install-wsl-and-linux)

#### 2. [Install WSL and Linux](./readme.md#2-install-wsl-and-linux)
1. [Download Linux](./readme.md#21-download-linux-you-can-use-other-distro-of-linux-see-more-at-microsoft-store)
2. [Install Linux on WSL](./readme.md#22-install-linux-on-wsl)

### 3. [Running Linux on WSL](./readme.md#3-running-linux-on-wsl)

---

## **1. Prepare to install Linux**
### **1.1 Install Windows Subsystem for Linux Preview** For (Windows 11 (build 22000.\*) or Windows 11 Insider Preview (builds 21362+) only
Download and install [here](https://www.microsoft.com/store/productId/9P9TQF7MRM4R).

### **1.2 Install vGPU driver**
It is recommended to run WSLg on a system with virtual GPU (vGPU) enabled for WSL so that you can benefit from hardware accelerated OpenGL rendering. You can find preview drivers supporting WSL from each of our partners below.
- [AMD GPU driver for WSL](https://community.amd.com/community/radeon-pro-graphics/blog/2020/06/17/announcing-amd-support-for-gpu-accelerated-machine-learning-training-on-windows-10)
- [Intel GPU driver for WSL](https://downloadcenter.intel.com/download/30579/Intel-Graphics-Windows-DCH-Drivers)
- [NVIDIA GPU driver for WSL](https://developer.nvidia.com/cuda/wsl)

### **1.3 Run powershell as Administrator**
1. Press "*Windows*" button on keyboard.
2. Type "*Powershell*".
3. At the right pane of search window press Run as Administrator.

### **1.4 Prepare to install Linux**
1. enable WSL.
```
dism /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

2. enable VirtualMachinePlatform.
```
dism /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

3. Download and install [WSL2 Linux kernel update package for x64 machines
 Note](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi).

4. Set WSL to version 2.
```
wsl --set-default-version 2
```

5. Update and upgrade apt (for Linux/Debian only)
```
wsl
sudo apt update && sudo apt upgrade
```

6. Restart your computer.

## **2 Download and install Linux**
### **2.1 Download Linux** (You can use other distro of linux, see more at Microsoft Store)
1. Install [Ubuntu](https://www.microsoft.com/store/productId/9PDXGNCFSCZV).

### **2.2 Install Linux on WSL**
1. **Open with ubuntu app**: Press "*Windows*" button, type "*Ubuntu*", then press "*Enter*", and wait for installing.

## **3. Running Linux on WSL**
There are 2 ways to run Linux on WSL, 
1. Run with Ubuntu app.
2. Run at powershell by type "*wsl*".
