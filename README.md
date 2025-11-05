# Wifi Cracker

A Python-based tool for Wi-Fi network scanning and security auditing on Linux. This script provides a user-friendly, menu-driven interface to wrap common commands from the `aircrack-ng` suite and other networking tools.

Developed by Jutt Studio (JS).
Contact: js434@proton.me
## ⚠️ Disclaimer

This tool is intended for educational purposes and for testing network security on systems you own or have explicit permission to test. Unauthorized scanning or attacks on networks are illegal. The developer assumes no liability and is not responsible for any misuse or damage caused by this program. See the `LICENSE` file for more details.

---

## License

This project is licensed under the **Jutt Studio Attribution License (JSAL) 1.0**.

You are free to use, copy, modify, and redistribute this project, provided that the attribution **"Original work by Jutt Studio"** is preserved in all distributed copies, derivative works, documentation, and product interfaces. See the `LICENSE` file for the full text.

## Features

*   **Network Interface Management**:
    *   Check the status and mode (Managed/Monitor) of all wireless interfaces.
    *   Enable and disable monitor mode on a selected interface.
*   **Wi-Fi Scanning**:
    *   Scan for all nearby Wi-Fi networks using `airodump-ng`.
    *   Select a target network from the scan results to perform further actions.
*   **Targeted Actions**:
    *   Run a targeted scan to view clients connected to a specific access point.
    *   Perform a deauthentication attack to disconnect clients from a network.
    *   Combine scanning and deauthentication to capture a WPA/WPA2 handshake.
*   **Handshake Cracking**:
    *   Crack captured `.cap` files against a wordlist.
    *   Supports both CPU-based cracking (`aircrack-ng`) and GPU-based cracking (`hashcat`).
*   **System Integration**:
    *   Ability to start the `NetworkManager` service.
    *   Automatically finds common wordlists in `/usr/share/wordlists/`.

---

## Requirements

This program does not require any external Python libraries, but it depends on several standard Linux command-line tools.

### System Requirements
*   **Operating System**: A Debian-based Linux distribution is recommended (e.g., Kali Linux, Ubuntu).
*   **Privileges**: `root` (sudo) access is required for most operations.
*   **Python**: Python 3.x.

### Software Dependencies
You must have the following tools installed on your system. You can typically install them on a Debian-based system with the command below.

*   `wireless-tools`: Provides `iwconfig` for interface management.
*   `net-tools`: Provides `ifconfig` for interface management.
*   `aircrack-ng`: The core suite for scanning, attacks, and cracking (`airodump-ng`, `aireplay-ng`, `aircrack-ng`).
*   `hashcat` (Optional): For much faster GPU-based handshake cracking.

#### Installation Command
```sh
sudo apt-get update && sudo apt-get install -y wireless-tools net-tools aircrack-ng hashcat
```

---

## How to Run

1.  Clone the repository to your machine:
    ```sh
    git clone https://github.com/Juttstodio/Wifi-Cracker.git
    ```
2.  Navigate into the project directory:
    ```sh
    cd Wifi-Cracker
    ```
3.  Ensure all the software dependencies listed above are installed.
4.  Run the script with `sudo` privileges for full functionality:
    ```sh
    sudo python3 wificracker.py
    ```
5.  Follow the on-screen menu to choose an action.