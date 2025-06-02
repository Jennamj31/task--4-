# 📡 Task 5: Capture and Analyze Network Traffic Using Wireshark

## 🎯 Objective
To perform real-time network traffic analysis using Wireshark, identify key protocols, and gain hands-on experience with packet capture, inspection, and filtering.
---

## 🛠️ Tools Used
- **Wireshark** – Network protocol analyzer
- **Command Prompt / Terminal** – To generate network traffic (e.g., `ping`, web browsing)
- **Windows OS** – Host environment

---

## 🧪 What Was Done

1. Installed and launched Wireshark.
2. Captured network traffic on the active interface for 1 minute.
3. Visited web pages and used basic network tools to generate traffic.
4. Applied filters (`http`, `tls`, `quic`) to analyze protocol-specific packets.
5. Exported the packet capture to `.pcap` format.
6. Screenshots of filtered packet views were saved.
7. A detailed report was written based on packet contents and behaviors.

---


## 🛠 Tools & Environment
- **Tool:** Wireshark (latest version)
- **Platform:** Windows 11
- **Network Interface:** Wi-Fi (Active Interface)
- **Traffic Sources:** Browser activity, system services, background apps

---

## 🔄 Steps Performed

1. **Installed Wireshark**
2. Started packet capture on the active network interface
3. Browsed websites and pinged servers to generate traffic
4. Captured for ~1 minute
5. Applied protocol filters:
   - `http`
   - `tls`
   - `quic`
   - `tcp`
6. Identified and analyzed at least 3 distinct protocols
7. Exported packet capture as `.pcap` (stored separately due to size constraints)
8. Summarized findings with annotated screenshots

---

## 🔍 Protocol Analysis

### 1. **HTTP (Unencrypted)**
- **Observation:** HTTP GET request to IP `132.196.154.22`
- **Response:** Standard `200 OK`
- **Insight:** URLs contained telemetry and software info, likely from background services like **BingWallpaper**
- **Security Note:** Unencrypted traffic can leak data unless protected

### 2. **TLS (Encrypted)**
- **TLS Versions Detected:** TLS 1.2 and TLS 1.3
- **Fields Observed:** Client Hello, Server Hello, SNI, Certificates
- **Application Data:** Encrypted after handshake
- **Example Domain:** `static.edge.microsoft.com`

### 3. **QUIC (Encrypted over UDP)**
- **Frames Detected:** Initial, PING, CRYPTO, PADDING
- **Usage:** Google and Microsoft services using QUIC over UDP
- **Insight:** Faster alternative to TCP+TLS; always encrypted

### 4. **OCSP**
- **Purpose:** Online Certificate Status Protocol for certificate validation
- **Observation:** System verifying digital certificate validity

  ---
## ✅ Conclusion
This task provided essential experience in monitoring and analyzing network packets using Wireshark. Through filtering and inspection, we identified active protocols and better understood how communication happens at the packet level, including application-level data, DNS lookups, and certificate validation steps.

