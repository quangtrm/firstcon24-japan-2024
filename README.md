# Defensive Solutions - The Golden Gate for Targeted Attack

This repository contains the slides and materials for the **FIRSTCON24** presentation:  
**"Defensive Solutions - The Golden Gate for Targeted Attack"**  
Presented by **Hoang Vu Duc, Tu Nguyen Thanh, Quang Tran Minh**  
**Viettel Threat Intelligence | Viettel Cyber Security**

---

## 📌 Overview
This presentation explores:
- **Real-world attack scenarios** leveraging EDR, AV, and NSM to distribute malware.
- **Malware analysis techniques**, including DLL Sideloading, Process Injection, and PE Headless attacks.
- **Threat Intelligence-driven defense strategies** for detecting and mitigating targeted attacks.
- **Key recommendations** for improving endpoint security, threat hunting, and detection.

---

## 📂 Contents
- `slides/` - PDF slides used during the presentation.
- `research/` - Additional research materials on malware techniques.
- `tools/` - References to open-source detection and investigation tools.

---

## 🚀 Key Takeaways
- **Threat actors leverage security solutions** to deploy and conceal malware.
- **DLL Sideloading & Process Injection** remain highly effective techniques in modern APT campaigns.
- **Threat Hunting & ZeroTrust approaches** are critical to early detection and mitigation.
- **Security teams must continuously validate EDR & AV configurations** to avoid blind spots.

---

## 🛠 Detection & Defense Strategies
### 🔍 **Identifying DLL Sideloading**
- Check for **unsigned DLL files** in application directories.
- Look for DLLs that mimic **System32/Syswow64** filenames.
- Analyze MFT timestamps to detect **anomalous loading patterns**.

### 🔥 **Detecting Process Injection**
- Monitor for suspicious Windows API calls (`VirtualAllocEx`, `WriteProcessMemory`, etc.).
- Identify memory areas with **Private, RWX/RX protection** that may contain shellcode.
- Use tools like **HollowsHunter** for process memory analysis.

### 🛡 **Strengthening Defense**
- Implement **absolute paths** instead of relative DLL loading.
- Use **SetDllDirectory("")** to remove unsafe search paths.
- Regularly audit **EDR and security software deployments**.

---

## 📢 Presentation Team
- **Hoang Vu Duc** - Threat Analyst  
- **Tu Nguyen Thanh** - Threat Intelligence Manager  
- **Quang Tran Minh** - Cyber Security Service Director  

📧 Contact: [Viettel Cyber Security](https://viettelcybersecurity.com)

---

## 📝 References
- **MITRE ATT&CK**: [https://attack.mitre.org](https://attack.mitre.org)
- **HollowsHunter**: [https://github.com/hasherezade/hollows_hunter](https://github.com/hasherezade/hollows_hunter)
- **NPS Proxy Server**: [https://github.com/ehang-io/nps](https://github.com/ehang-io/nps)

---

## ⚠️ Disclaimer
This repository is for educational and research purposes only. The authors and Viettel Cyber Security are not responsible for any misuse of the information.

---

🎯 **Stay ahead of targeted attacks with Threat Intelligence!**
