# Debian 12 Exegol VM 🐧💻

Welcome to the **Debian 12 Exegol VM** repository! This project offers a lightweight virtual machine based on Debian 12, equipped with Exegol, a modular Docker-based pentesting framework. It serves as an excellent tool for Capture The Flag (CTF) challenges, bug bounty programs, OSINT tasks, and various offensive security activities.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-blue.svg)](https://github.com/ChidiCeeway/Debian12-Exegol-VM/releases)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Topics](#topics)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **Lightweight**: Designed to run efficiently without consuming excessive resources.
- **Modular**: Exegol allows you to add or remove tools as needed.
- **Docker-based**: Simplifies the installation and management of pentesting tools.
- **User-friendly**: Easy to set up and use, even for beginners.
- **Versatile**: Suitable for CTFs, bug bounty, OSINT, and other offensive security tasks.

## Installation

To get started, you need to download the VM image. Visit the [Releases section](https://github.com/ChidiCeeway/Debian12-Exegol-VM/releases) to find the latest version. Download the file and follow these steps:

1. **Install VirtualBox**: If you haven’t installed VirtualBox yet, download it from the [official website](https://www.virtualbox.org/) and install it on your system.

2. **Import the VM**:
   - Open VirtualBox.
   - Click on "Import Appliance."
   - Select the downloaded VM image file.
   - Follow the prompts to complete the import.

3. **Start the VM**: Once imported, you can start the VM by selecting it in VirtualBox and clicking "Start."

4. **Initial Setup**: Log in using the default credentials provided in the documentation.

## Usage

Once the VM is up and running, you can start using Exegol for your pentesting needs. Here are some basic commands to get you started:

- **Start Exegol**: Open a terminal in the VM and run:
  ```bash
  exegol
  ```

- **List Available Tools**: To see all the tools available in Exegol, use:
  ```bash
  exegol list
  ```

- **Run a Tool**: To run a specific tool, type:
  ```bash
  exegol run <tool_name>
  ```

### Example Usage

1. **CTF Challenges**: Use Exegol’s tools to solve various CTF challenges. For example, if you need to perform a web vulnerability scan, run:
   ```bash
   exegol run nikto
   ```

2. **Bug Bounty Programs**: When hunting for bugs, you can use tools like Burp Suite or OWASP ZAP included in Exegol. Simply run:
   ```bash
   exegol run burpsuite
   ```

3. **OSINT Tasks**: Gather information on targets using OSINT tools available in Exegol. For instance:
   ```bash
   exegol run theharvester
   ```

## Topics

This repository covers various topics related to cybersecurity and pentesting:

- **Bug Bounty**: Engage in programs to find vulnerabilities in software.
- **CTF**: Participate in challenges to test your skills.
- **Cybersecurity**: Understand and apply security measures to protect systems.
- **Debian**: Utilize the Debian operating system for stability and performance.
- **Docker**: Manage applications in containers for ease of use.
- **Exegol**: Explore the features of this modular pentesting framework.
- **Offensive Security**: Learn and apply techniques to identify and exploit vulnerabilities.
- **OSINT**: Gather publicly available information for security assessments.
- **Penetration Testing**: Simulate attacks to evaluate the security of systems.
- **Pentesting**: Conduct security assessments to find and fix vulnerabilities.
- **Virtual Machine**: Run isolated environments for testing and development.
- **VirtualBox**: Use this software to create and manage virtual machines.

## Contributing

We welcome contributions from everyone. If you want to contribute, please follow these steps:

1. **Fork the repository**: Click the "Fork" button on the top right of the page.
2. **Clone your fork**: Use the command:
   ```bash
   git clone https://github.com/yourusername/Debian12-Exegol-VM.git
   ```
3. **Create a new branch**: Use:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make your changes**: Edit the files as needed.
5. **Commit your changes**: Use:
   ```bash
   git commit -m "Add your commit message"
   ```
6. **Push to your fork**: Use:
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Create a pull request**: Go to the original repository and click on "New Pull Request."

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or support, please contact:

- **Chidi Ceeway**: [GitHub Profile](https://github.com/ChidiCeeway)

---

Thank you for checking out the **Debian 12 Exegol VM** repository! We hope you find it useful for your pentesting and cybersecurity endeavors. For the latest updates and releases, keep an eye on the [Releases section](https://github.com/ChidiCeeway/Debian12-Exegol-VM/releases).