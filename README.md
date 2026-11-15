# Week 3 Cybersecurity Lab: Password Cracking with John the Ripper & Networkwalks Tools

**Intern:** Abbeylanre (Batch B084)  
**Organization:** Networkwalks Academy  
**Modules Covered:**
* **Module 1:** Password Cracking with John the Ripper (JTR) & Johnny GUI
* **Module 2:** Password Cracking with Networkwalks Web Tools

---

## 📌 Executive Summary
This repository documents the Week 3 Cybersecurity & Ethical Hacking internship labs focused on password auditing and cryptographic hash recovery. Using both local desktop tools (**John the Ripper** / **Johnny**) and browser-based utilities (**Networkwalks Hash Calculator** & **Password Cracker**), an encrypted target document (`My Locked PDF1.pdf`) was analyzed, its `$pdf$` hash extracted, and its plaintext password (`password1`) recovered.

---

## 🔹 Module 1: Password Cracking with John the Ripper & Johnny

### Tools & Environment
* **OS:** Windows PC
* **CLI Engine:** John the Ripper (`john-1.9.0-jumbo-1`)
* **GUI Frontend:** Johnny (`v2.2`)
* **Hash Extraction:** OnlineHashCrack PDF Hash Extractor

### Methodology
1. **Installation & Setup:** Downloaded John the Ripper and Johnny GUI, then configured Johnny's settings to point to `...\john\run\john.exe`.
2. **Hash Extraction:** Uploaded `My Locked PDF1.pdf` to extract the raw hash beginning with `$pdf$...` (removing any `b'` wrapper characters) and saved it as `hash1.txt`.
3. **Password Recovery:** Loaded `hash1.txt` into Johnny and initiated **Start new attack**, recovering the plaintext password (`password1`).
4. **Verification:** Unlocked `My Locked PDF1.pdf` using the recovered credential.

### Proof of Work (Module 1)
| Step | Screenshot |
| :--- | :--- |
| **1. Johnny Configuration** | ![Johnny Setup](screenshots1/johny-setup.png) |
| **2. Hash Extraction (`$pdf$`)** | ![Hash Extraction](screenshots1/hash-extraction.png) |
| **3. Hash Saving (`$pdf$`)** | ![Hash Saving](/screenshots1/hash1.png) |
| **4. Johnny Cracked Result** | ![Johnny Attack Success](screenshots1/johny-attack.png) |
| **5. Unlocked PDF Verification** | ![Unlocked PDF](screenshots1/unlocked-pdf1.png) |

---

## 🔹 Module 2: Password Cracking with Networkwalks Tools

### Tools & Environment
* **OS / Browser:** Windows Laptop (Web Browser)
* **Extraction Tool:** [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)
* **Cracking Tool:** [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)

### Methodology
1. **Hash Extraction:** Uploaded `My Locked PDF1.pdf` directly into the Networkwalks Hash Calculator and copied the complete `$pdf$...` hash string.
2. **Online Cracking Attack:** Pasted the extracted hash into the Networkwalks Password Cracker and launched the attack.
3. **Password Recovery & Verification:** Retrieved the matched password (`password1`) from the results screen and verified access to `My Locked PDF1.pdf`.

### Proof of Work (Module 2)
| Step | Screenshot |
| :--- | :--- |
| **1. Networkwalks Hash Calculator** | ![Hash Calculator](screenshots2/hash-calculator.png) |
| **2. Networkwalks Password Cracker** | ![Password Cracker](screenshots2/password-cracker-success.png) |
| **3. Unlocked PDF Verification** | ![Unlocked PDF](screenshots2/unlocked-pdf2.png) |

---

## 🛡️ Security Insights & Comparison
* **Local vs. Web Tools:** Local engines like **John the Ripper** offer full offline privacy, custom rule sets, and hardware acceleration (CPU/GPU) for complex hashes, whereas web-based tools like **Networkwalks** provide zero-installation convenience for quick audits.
* **Operational Security Note:** In real-world penetration testing, sensitive corporate documents or hashes should never be uploaded to third-party public web crackers; offline extraction (`pdf2john`) and local JTR instances should be used instead.
* **Remediation:** Protect sensitive files using strong, high-entropy passphrases (14+ characters) and AES-256 encryption to resist dictionary and brute-force attacks.

 ## 👤 Author Metadata

* **Name:** Abiodun Omotosho
* **Program:** Networkwalks Cybersecurity Internship
* **Focus Areas:** Cybersecurity | Network Security | Traffic Analysis
* **LinkedIn:** [Abiodun Omotosho Profile](https://www.linkedin.com/in/abiodunomotosho1)
