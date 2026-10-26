# Network Security Lab: Experiment 5b

## Web Mirroring Using GNU Wget (Task T11)

**Student Name:** Dyuthi S Sarath  
**Roll Number:** 11 
**Course Outcome:** CO2 (Experiment 5b: Task T11)
**Module:** Module 2 — Application Layer Protocols, Network Reconnaissance, and Web Content Mirroring  

---

## 1. Aim
To create a local mirror of a target website (`http://example.com`), save all assets and recursively linked resources to a local directory, and verify offline functionality via a web browser under disconnected network conditions.

---

## 2. Tools & Environment
- **Utility:** GNU Wget (version 1.21.3)
- **Web Browser:** Mozilla Firefox 115.0+ ESR
- **Environment:** Kali Linux / Windows (WSL2 / Git Bash)

---

## 3. Execution Commands
```bash
# 1. Create target workspace directory and navigate into it
mkdir -p ~/11Dyuthi/web_mirrors/example && cd ~/11Dyuthi/web_mirrors/example

# 2. Mirror website with link conversion and page requisites
wget --mirror --convert-links --page-requisites --no-parent [https://example.com](https://example.com)

# 3. Disconnect network and launch offline verification
nmcli networking off
firefox [example.com/index.html](https://example.com/index.html) &# SNS_Httrack
