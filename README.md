# 🐧 Debian12‑Exegol VM

A **VirtualBox-ready appliance** featuring Debian 12 (64-bit) with **Exegol free** pre-installed.

---

## 📦 What’s Inside

- **Operating System**: Debian 12 “Bookworm” (64-bit)
- **Exegol free** installed via pipx/Docker
- **User account**:
  - **Username**: `jul` (sudo privileges)
  - **Password**: `jul`
- **Root user**: disabled by default (no password set)
- **SSH**: enabled and ready to use

---

## 🛠️ System Requirements

| Component    | Minimum        | Recommended |
|-------------|----------------|-------------|
| VirtualBox  | ≥ 6.1          | —           |
| RAM         | 4 GB           | 8 GB        |
| CPU         | 2 vCPUs        | —           |
| Video       | 128 MB + 3D acceleration enabled | — |
| Disk space  | ≥ 50 GB free   | —           |
| Network     | NAT (port forwarding optional) | — |

Below are the VirtualBox settings used for the Debian 12 virtual machine :

### 📄 General Settings
![General Setting](https://github.com/user-attachments/assets/a6092f66-13b4-45da-94eb-4d72119fa28b)

### 🧠 System (RAM, Boot Order, Chipset, etc.)
![System Settings](https://github.com/user-attachments/assets/a3b34b8f-b243-4cf1-a4de-75ad593314e0)

### 🖥️ Display (Video Settings)
![Display Settings](https://github.com/user-attachments/assets/06cd7f48-d7df-4211-aba1-093bd5b23a69)

### 💾 Storage
![Storage Settings](https://github.com/user-attachments/assets/cb6ee98a-3f1d-49c8-bb51-700e2f8d82e9)

### 🌐 Network
![Network Settings](https://github.com/user-attachments/assets/4b0a8411-50c6-43c4-aa5c-41402c255b55)

---

## 📥 Installation

#### 1. Clone the repository :
   ```bash
   git clone https://github.com/Jul1111/Debian12-Exegol-VM
   ```
#### 2. Download all parts of the Debian12.7z archive from the Releases section.
- 🔗 [GitHub Releases (split archive)](https://github.com/Jul1111/Debian12-Exegol-VM/releases)
- 🔗 [Direct Mega Link (full `.ova` file)](https://mega.nz/file/QUBi2DgY#cDtwvbKSQudLYNnZSEe9AoS2BxdBDxUL1aqu7yTRrqg)
#### 3. Make sure all files are in the same folder, then extract using 7-Zip or via terminal :

🖥️ On Windows (with 7-Zip installed):
     ```
    7z x Debian12.7z.001
    ```

🐧 On Linux/macOS (with p7zip-full installed) :
      ```
    7z x Debian12.7z.001
    ```
    
#### 4. You will get the .ova virtual machine file. You can import it into your hypervisor (e.g., VirtualBox or VMware).

## 🚀 Quickstart: Launching Exegol

From the Debian 12 VM command line (Docker, pipx, and Exegol are already installed):

### 1. Update Exegol & images  
```bash
exegol update    # Updates the Exegol wrapper and all installed images :contentReference[oaicite:1]{index=1}
```
### 2. Start & enter a container
```bash
exegol start <container_name> <image_name> [options]
```
Example: 
```bash
exegol start default
```
![Example](https://github.com/user-attachments/assets/0317f251-4392-4f72-8ea7-f4419331d860)

- If <container_name> is omitted, it defaults to the <image_name>

- Process:
  - If the image isn’t installed, Exegol prompts for installation
  - Creates the container with the provided settings
  - Starts it and drops you into an interactive shell

 Common options:
```bash
-w, --workspace <path>: bind host folder to /workspace
```

```bash
-cwd: mount current directory as workspace
```

```bash
--vpn <file.ovpn>: launch VPN at startup
```

```bash
-V, --volume <host>:<container>: add volume mount
```

```bash
-d, --device <dev>: add host device (e.g., /dev/ttyACM0)
```

```bash
--disable-X11: disable GUI sharing
```

```bash
--desktop: enable full GUI desktop via HTTP/VNC 
```

```bash
-l, --log: enable shell logging (asciinema by default) 
```

```bash
-e, --env KEY=VALUE: set environment variable
```

```bash
-s, --shell <shell>: choose shell (default: zsh)
```

```bash
--privileged/--cap: add Linux capabilities or privileged mode when needed (e.g., VPN, devices)
```
---

### For full option list :

Run 
```bash
exegol start -h
```
---

### ✅ Verify file integrity (optional but recommended)

After extracting `Debian12.7z`, you will get a `.ova` file.

To verify that the file was not corrupted or altered, run:

#### On Linux/macOS :
```bash
sha256sum Debian12.ova
```
#### Windows PowerShell:
```bash
Get-FileHash -Algorithm SHA256 .\Debian12.ova
```
#### Expected SHA-256 hash:

```bash
890F4F754B0EE504AC61EE9CB886CD77B3A11F6DC2F17791F50A8EA9C1A79B39
```
#### If the result matches, the file is intact.

---
⚠️ **Security Note**: This VM is provided as-is. Ensure you review its contents before using it in sensitive environments.

