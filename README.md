# CloakSphere: A Framework for IDS Evasion and Pen Testing

This project, titled **CloakSphere**, is a practical implementation of network security testing using **Snort IDS**. It includes writing custom rules, simulating network-based attacks, and testing common evasion techniques used to bypass detection.

Developed under the M.Sc. Cyber Security program, the project demonstrates both attack simulation and defense strategy within a controlled lab setup using OWASP Juice Shop as the vulnerable target.

---

## 🎯 Objectives

- Write and implement custom Snort rules.
- Simulate real-world attacks (e.g., SSH brute force, SQL injection).
- Explore IDS evasion techniques like Base64 encoding and SQL obfuscation.
- Evaluate Snort’s effectiveness and improve detection accuracy.

---

## 🔍 Key Features

- 🚨 **SSH Authentication & Brute-Force Attack Detection**
- 💬 **Improper Input Validation Detection (Juice Shop Feedback Form)**
- 🧩 **SQL Injection Detection with Regex Matching**
- 📁 **Unauthorized File Upload Detection (non-PDF/ZIP)**
- 🎭 **Reflected XSS Parameter Tampering**
- 🎯 **Evasion Techniques**
  - Base64-encoded payloads
  - SQL inline comments (`' OR/**/1=1--`)

---

## 🧰 Tools Used

| Tool        | Purpose                                | Link |
|-------------|----------------------------------------|------|
| **Snort**   | IDS engine for writing custom rules     | [snort.org](https://www.snort.org) |
| **OWASP Juice Shop** | Vulnerable web app for testing    | [Juice Shop](https://owasp.org/www-project-juice-shop/) |
| **Hydra**   | Brute-force simulation tool             | [GitHub](https://github.com/vanhauser-thc/thc-hydra) |
| **TCPDump** | Traffic capture and inspection          | [man page](https://man7.org/linux/man-pages/man8/tcpdump.8.html) |
| **Burp Suite** | Request interception and manipulation | [PortSwigger](https://portswigger.net/burp) |

---

## 🧪 Attack Simulations

| Attack Type               | Detection Method                             |
|---------------------------|----------------------------------------------|
| SSH Login Detection       | TCP alert with Snort rule SID 100002         |
| SSH Brute Force           | Detection filter on login frequency          |
| Input Validation Bypass   | Regex match on modified rating parameters    |
| SQL Injection             | Classic payload (`' OR 1=1--`) and obfuscation |
| Unauthorized File Upload  | PCRE match on disallowed MIME types          |
| Reflected XSS             | Parameter tampering via URL or input field   |

---

## 📊 Evasion Techniques

- **Base64 Encoding** – Encodes input to avoid plain-text rule detection.
- **SQL Comment Obfuscation** – Breaks injection pattern using `/**/` comments to avoid signature match.

---

## 🧠 Recommendations & Future Work

- Use **PCRE** for flexible pattern matching.
- Integrate **machine learning** for anomaly-based detection.
- Visualize logs using **ELK Stack** for easier incident analysis.

---

## 📌 References

- [Snort Documentation](https://docs.snort.org/)
- [Hydra on GitHub](https://github.com/vanhauser-thc/thc-hydra)
- [TCPDump Manual](https://man7.org/linux/man-pages/man8/tcpdump.8.html)
- [Regex101 Tool](https://regex101.com/)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)

---

## 📄 License

This project is released under the MIT License.
