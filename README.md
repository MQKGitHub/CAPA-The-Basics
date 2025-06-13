### 🛡️ CAPA: The Basics

**Room:** [CAPA: The Basics — TryHackMe](https://tryhackme.com/room/capabasics)  
**Status:** ✅ Completed  
**Date:** *12 June 2025*

---

### 🎯 Objective  
This room introduced **CAPA**, a tool for static malware analysis. The goal was to understand how CAPA detects malware behaviour using pre-defined rules and how it maps behaviours to MITRE ATT&CK, MBC, and MAEC frameworks. It also explored the use of CAPA Web Explorer for reviewing results more clearly.

---

### 🗝️ Key Concepts  
- **CAPA** — A static analysis tool from Mandiant that detects capabilities in binaries like PE, ELF, shellcode, etc.  
- **Static Analysis** — Examining code or files without executing them.  
- **MITRE ATT&CK** — A framework that CAPA references to show tactics and techniques of malware.  
- **MBC (Malware Behaviour Catalogue)** — Lists goals and behaviours of malware, e.g. process creation, file access.  
- **MAEC** — Describes malware attributes like “launcher” or “downloader” behaviours.  
- **Namespace** — Categories in CAPA that group similar behaviours, e.g. `anti-analysis`, `data-manipulation`.  
- **Verbose Output (-v, -vv)** — Extra detailed CAPA output, great for seeing exact rule matches.  
- **CAPA Web Explorer** — A GUI to visualise CAPA's output in a much more digestible way.

---

### 🛠️ Tools Used  
- **CAPA** — Used to analyse binary files and detect malware-like behaviours.  
- **PowerShell** — Used to run CAPA and view output files.  
- **CAPA Web Explorer** — Used to explore JSON output for easier analysis.  
- **JSON Output + -vv flag** — Used for deeper insight into how rules were triggered.

---

### ⚠️ Challenges Faced  
- Reading large CAPA output in plain text was overwhelming (thousands of lines).  
- Understanding all the mapping between Capability, Namespace, and Behaviour frameworks was tricky.  
- Solved by using the **CAPA Web Explorer** and taking notes on each framework separately.

---

### 🧠 What I Learned  
- How CAPA uses rules to detect behaviours like creating processes, HTTP communication, or using Base64.  
- The structure of CAPA’s output: Capability → Namespace → Rule file (YAML).  
- The link between malware actions and frameworks like MITRE ATT&CK and MBC.  
- How to use `-vv` and export JSON for better analysis and understanding of rule triggers.

---

### 🌐 Real-World Application:  
>CAPA is used by malware analysts and threat hunters to understand a binary’s intent without needing to execute it.  
> For example, if a file shows behaviours like “Base64 encoding” and “creating scheduled tasks,” it may be trying to hide its payload and stay persistent on the system.

---

### 💭 Reflections:  
- This room made static analysis feel much more accessible.  
- The CAPA Web Explorer is a must-use — it made analysis 100x easier.  
