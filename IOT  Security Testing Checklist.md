# 🌐 IoT Security Testing Checklist
*A comprehensive assessment guide for IoT devices, protocols, and ecosystems*

---

## 🔧 **1. Hardware Assessment**
- [ ] Inspect physical ports (UART, JTAG, SPI, USB)
- [ ] Test debug interfaces (serial console access)
- [ ] Dump flash memory (chip-off/ISP techniques)
- [ ] Analyze PCB for hardcoded credentials
- [ ] Test voltage glitching/fault injection
- [ ] Verify tamper protection mechanisms

---

## 💾 **2. Firmware Analysis**
- [ ] Extract firmware (OTA/physically)
- [ ] Reverse engineer binaries (Ghidra/IDA)
- [ ] Search hardcoded secrets (API keys, passwords)
- [ ] Test for buffer overflows in services
- [ ] Verify secure boot implementation
- [ ] Check for deprecated libraries (OpenSSL 1.0.2)
- [ ] Analyze update mechanism integrity

---

## 📶 **3. Wireless Protocols**
### **WiFi**
- [ ] Test WPA2/3 implementation (KRACK attacks)
- [ ] Check default SSID/password combos
- [ ] Test captive portal security

### **Bluetooth/BLE**
- [ ] Test auth bypass (BlueBorne)
- [ ] Check insecure pairing modes
- [ ] Sniff sensitive data transmissions

### **Zigbee/Z-Wave**
- [ ] Test encryption key weaknesses
- [ ] Check for replay attacks
- [ ] Verify mesh network isolation

### **RFID/NFC**
- [ ] Test card cloning attacks
- [ ] Check relay attack feasibility

---

## 🌐 **4. Network Services**
- [ ] Scan open ports (nmap)
- [ ] Test for Telnet/FTP default creds
- [ ] Analyze custom TCP/UDP protocols
- [ ] Test DNS rebinding attacks
- [ ] Verify firewall rules

---

## ☁️ **5. Cloud/Web Interfaces**
- [ ] Test API endpoints (REST/MQTT)
- [ ] Check for IDOR in device management
- [ ] Test SSRF in cloud functions
- [ ] Verify WebSocket security
- [ ] Audit AWS/GCP/Azure configurations

---

## 📱 **6. Mobile Applications**
- [ ] Reverse engineer APK/IPA
- [ ] Test insecure local storage
- [ ] Analyze app-to-device auth
- [ ] Bypass certificate pinning
- [ ] Check for sensitive data leaks

---

## 🔄 **7. Update Mechanism**
- [ ] Test OTA update signing
- [ ] Attempt firmware downgrade
- [ ] Check update server authentication
- [ ] Verify encrypted update channels
- [ ] Test rollback protection

---

## 🛠️ **Recommended Tools**
```bash
# Hardware
- Bus Pirate, JTAGulator, ChipWhisperer

# Firmware
- Binwalk, Ghidra, Firmwalker

# Wireless
- HackRF, Ubertooth, Bettercap

# Mobile
- MobSF, Frida, Objection

# Cloud
- Burp Suite, MQTTfx, Postman
```
 ---
### ⚠️ **Disclaimer**  

The lab solutions, exploits, and write-ups in this repository are **for educational and authorized security research purposes only**. 
