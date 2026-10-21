## FiberHome Password Calculator (CVE-2025-63353)
A Password calculator utility designed for security auditing and proof-of-concept demonstration of the deterministic password generation flaw found in FiberHome routers.
## ☠️ Known Affected Devices
`HG6145F1`, `HG6245P`, `HG6249A`, `HG6543C`, `HG6245D`, `HG6243C`, `HG6244C`, `HG6240A`
Devices with Software: `RP2666` , `RP4423`
## 📋 Overview
This password generator exploits CVE-2025-63353, a critical vulnerability where the factory-default WPA/WPA2 pre-shared key is mathematically derived from the broadcasted SSID. By observing the network name (SSID), an attacker can calculate the default password without any user interaction.
The Vulnerability Logic:
The router uses a deterministic formula: HEX_A (from SSID) + HEX_B (from Password) = 0xFFFFFF.
## 🌍 Impact Globally
FiberHome equipment is widely deployed by major Internet Service Providers (ISPs) across emerging markets. This password calculator is specifically effective against devices with the following default naming conventions:

* Vulnerable SSID Format: fh_XXXXXX (e.g., fh_)
* Vulnerable Password Format: wlanxxxxxx

## 🏳️ Affected Regions and ISPs
* **Algeria:** `Algérie Télécom (Idoom Fibre)`
* **Armenia:** `GNC-Alfa`
* **Brazil:** `Brisanet`
* **India:** `BSNL` and `Airtel`
* **Indonesia:** `Telkom`
* **Kenya:** `Safaricom`
* **Pakistan:** `Storm Fiber`
* **Philippines:** `PLDT`
* **Romania:** `RDS Net`
* **Thailand:** `3BB (Triple T Broadband)`

## 🚀 Usage
* [Password Calculator here](https://code-fanatic.github.io/fiberhome-password-calculator/)

## 🛠️ Mitigation for Users
If your router is affected, your network is insecure until you take action:

   1. Change your Wi-Fi Password: Do not use the factory-default settings.
   2. Disable WPS: This reduces the attack surface for similar credential-based exploits.
   3. Use a Third-Party Router: Connect your own router to the FiberHome ONT and disable the FiberHome Wi-Fi entirely.

## ⚠️  Legal Disclaimer
This information is provided for authorized security testing, network administration, and educational purposes.
