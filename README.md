
# 🎓 **Graduation Project - Automated Web Vulnerability Scanner**

This project is a **custom-built vulnerability scanner** designed to automate the process of discovering and testing web application security flaws. The scanner integrates multiple tools to perform **subdomain enumeration**, **parameter discovery**, **domain validation**, and **vulnerability scanning** in a simple, streamlined workflow. The main script `main.py` acts as the core controller that links and runs all other tools in the correct sequence. You can run all tools together or select individual modules as needed.

---

## 🚀 **Included Tools and Modules**

1. 🔍 **Subdomain Enumeration**  
   - **Script:** `SubScoutX.py`  
   - **Purpose:** Automatically finds valid subdomains for a given domain.  
   - **Output:** `output/subdomains.txt`

2. 🔗 **Parameter Finder**  
   - **Script:** `DomainPulse.py`  
   - **Purpose:** Extracts and lists URL parameters from target domains.  
   - **Output:** `output/parameters.txt`

3. ✅ **Domain Status Code Validator**  
   - **Script:** `DomainPulse.py`  
   - **Purpose:** Checks HTTP response codes for each enumerated subdomain to validate active targets.  
   - **Output:** `output/status_codes.txt`

4. 🛡️ **Vulnerability Scanner**  
   - **Script:** `scanner.py`  
   - **Purpose:** Scans valid targets and parameters for known vulnerabilities such as **XSS**, **SQL Injection**, **SSRF**, **LFI**, etc.  
   - **Payloads:** Uses payload files stored in the `payloads/` directory.  
   - **Output:** `output/vulnerabilities.txt`

---

## 🗂️ **Directory Structure**

```
.
├── main.py
├── SubScoutX.py
├── DomainPulse.py
├── ParamForge.py
├── scanner.py
├── payloads/
│   ├── xss.txt
│   ├── sqli.txt
│   ├── ssrf.txt
│   └── lfi.txt
├── output/
│   ├── subdomains.txt
│   ├── parameters.txt
│   ├── status_codes.txt
│   └── vulnerabilities.txt
└── README.md
```

---

## ⚙️ **How to Run**

1. Install required Python modules:
```bash
pip install -r requirements.txt
```

2. Run the main script:
```bash
python3 main.py
```

3. Follow the on-screen instructions to select which modules to run.

---

## 📝 **Example Usage**

▶️ **Run the Full Scanner (All Modules):**
```bash
python3 main.py
```

**Sample Output:**
```
[*] Starting Subdomain Enumeration...
[+] Found 10 subdomains. Saved to output/subdomains.txt

[*] Starting Parameter Finder...
[+] Found 5 parameters. Saved to output/parameters.txt

[*] Starting Status Code Validator...
[+] 8 active domains identified. Saved to output/status_codes.txt

[*] Starting Vulnerability Scanner...
[+] 3 potential vulnerabilities found! Saved to output/vulnerabilities.txt
```

▶️ **Run Only the Vulnerability Scanner Manually:**
```bash
python3 scanner.py -u https://example.com
```

**Sample Output:**
```
[*] Scanning https://example.com...
[+] Possible XSS vulnerability detected on https://example.com/search?q=<payload>
[+] Possible SQL Injection detected on https://example.com/login?id=' OR '1'='1
```

---

## 📌 **Notes**

- All logs and results are saved automatically in the `output/` folder.
- Ensure the `payloads/` directory contains the necessary payload lists before running the scanner.

---

## 👨‍💻 **Authors**

- Abdullah Mahmoud AboShosha  
- Mahmoud Adham Mohammed  
- Waleed Salah Eldin Sultan  
- Ahmed Elsayed Tawfeq  
- Abdullah Atta Shawat  
- Ahmed Osama Samir  
- Salma Fouad Younes

---

## 🎓 **Supervision**

**Dr. Mai Ramadan**  
_Associate Professor and Head of IT Department_

---

## 🏫 **Faculty of Computer and Information Science**  
### Information Technology Department  
### Graduation Project 2025
