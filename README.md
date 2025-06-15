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

*(Add a screenshot of VirtualBox settings here)*

---

## 📥 Installation

1. Clone the repository :
   ```bash
   git clone https://github.com/YOUR_USERNAME/exegol-debian12-vm.git
   
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
Example: exegol start web full

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
### For full option list :

```bash
Run exegol start -h
```

