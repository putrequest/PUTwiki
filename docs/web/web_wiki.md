# **Web**

## **Rekonesans:**

### **[Sublist3r](https://github.com/aboul3la/Sublist3r?tab=readme-ov-file#usage)/[Gobuster](https://github.com/OJ/gobuster?tab=readme-ov-file#manual):** Do wykrywania subdomen i nie tylko.
  - `gobuster dir -u [adres-celu] -w [wordlista]`
  - `python sublist3r.py -d [adres-celu] -p [porty]`
### **[Nmap](https://nmap.org/):** Do odkrywania i mapowania sieci.
  - [Cheatsheet](NMAP_cheatsheet.pdf)
  - Przykładowe skany:
    
    - `nmap -sp [adres-ip/maska]` - Ping scan, służy do sprawdzania które hosty w danej sieci odpowiedzą.
    - `nmap -sVC [adres-ip]` - Połączenie `-sV` (sprawdzania wersji serwisów na porcie) i `-sC` (użycia domyślnych skryptów).
    - `nmap -p 1-100 [adres-ip]` - Skanuje porty 1-100, `-p-` skanuje wszystkie porty.
    - `nmap -A -T5 [adres-ip]` - `-A` Detekcja serwisów i OS wraz z domyślnymi skryptami, `-T5` to szybsze wysyłanie pakietów.
    - `nmap -Pn --script vuln [adres-ip]` - Wyszukiwanie CVE za pomocą skryptów nastawionych na podataności.
    - `nmap -vv [adres-ip]` - Zwiększenie informacji o skanowaniu w outpucie.

### **TheHarvester:** Pomaga w zbieraniu informacji z publicznych źródeł.

## **Skanowanie:**

### **Burp Suite:** Zawiera narzędzia do skanowania, przeszukiwania i analizy bezpieczeństwa aplikacji internetowych.
### **Nikto:** Przeprowadza kompleksowe testy na serwerach WWW w poszukiwaniu podatności.
### **OWASP ZAP:** Skaner bezpieczeństwa aplikacji internetowych do wykrywania podatności.

## **Eskploracja:**

### **Dirb/Dirbuster:** Do siłowego przeszukiwania katalogów i plików na serwerach WWW.
### **Wfuzz:** Pomaga w odkrywaniu ukrytego lub niepowiązanego kontentu.
### **Gobuster:** Narzędzie do siłowego przeszukiwania katalogów i plików.

## **Eksploracja podatności:**

### **Metasploit Framework:** Do tworzenia, testowania i wykonywania kodu wykorzystującego podatność na docelowym systemie.
### **SQLMap:** Specjalnie zaprojektowane do wykrywania i wykorzystywania podatności na wstrzykiwanie SQL.
### **BeEF (Browser Exploitation Framework):** Koncentruje się na podatnościach przeglądarki internetowej.
### **[RevShells](https://www.revshells.com/):** prosty "generator" reverse shell-i.

## **Po-eksploatacja:**

### **Mimikatz:** Do wydobywania haseł, hashy i innych danych uwierzytelniających.
### **PowerShell Empire:** Platforma po-eksploatacyjna dla środowisk Windows.
### **Responder:** Pomaga w truciznowaniu LLMNR, NBT-NS i MDNS.
### **[PEASS-ng](https://github.com/carlospolop/PEASS-ng/tree/master):** Privilege Escalation Awesome Scripts SUITE (with colors)
### **[GTFObins](gtfobins.github.io):** curated list of Unix binaries that can be used to bypass local security restrictions in misconfigured systems.
 
## **Raportowanie:**

### **Dradis:** Narzędzie do wspólnego tworzenia raportów, które integruje wyniki w jeden raport.
### **Faraday:** Wspólna platforma do testów penetracyjnych do zarządzania raportami i podatnościami.
### **LaTeX/Markdown:** Do tworzenia czytelnych i dobrze sformatowanych raportów.

<!-- # **IN ENG:**

### 1. **Reconnaissance:**

   - **Stage Description:** Gather information about the target web application and its infrastructure.
   
   - **Useful Tools:**
     - **Sublist3r:** For subdomain enumeration.
     - **TheHarvester:** Helps in email harvesting and gathering information from public sources.
     - **Nmap:** For network discovery and mapping.
      - Sample scans:
        - `nmap -sp [IP address/mask]` - Ping scan, used to check which hosts in a given network will respond.
        - `nmap -sVC [IP address]` - Combination of `-sV` (service version detection) and `-sC` (default script usage).
        - `nmap -p 1-100 [IP address]` - Scans ports 1-100, `-p-` scans all ports.
        - `nmap -A -T5 [IP address]` - `-A` Service and OS detection with default scripts, `-T5` for faster packet transmission.
        - `nmap -Pn --script vuln [IP address]` - Searching for CVE using vulnerability-focused scripts.
        - `nmap -vv [IP address]` - Increased scan information in output.

### 2. **Scanning:**

   - **Stage Description:** Identify vulnerabilities and weaknesses in the target web application.
   
   - **Useful Tools:**
     - **Nikto:** Performs comprehensive tests against web servers for vulnerabilities.
     - **OWASP ZAP:** Web application security scanner for finding vulnerabilities.
     - **Burp Suite:** Includes tools for scanning, crawling, and analyzing web application security.

### 3. **Enumeration:**

   - **Stage Description:** Discover as much information as possible about the web application, such as directories, files, and technologies used.
   
   - **Useful Tools:**
     - **Dirb/Dirbuster:** For brute-forcing directories and files on web/application servers.
     - **Wfuzz:** Helps in discovering hidden or unlinked content.
     - **Gobuster:** Directory and file brute-forcing tool.

### 4. **Vulnerability Exploitation:**

   - **Stage Description:** Exploit identified vulnerabilities to assess the impact and gain deeper access.
   
   - **Useful Tools:**
     - **Metasploit Framework:** For developing, testing, and executing exploit code against a target machine.
     - **SQLMap:** Specifically designed for detecting and exploiting SQL injection flaws.
     - **BeEF (Browser Exploitation Framework):** Focuses on web browser vulnerabilities.

### 5. **Post-Exploitation:**

   - **Stage Description:** Maintain access, gather further intelligence, and escalate privileges if possible.
   
   - **Useful Tools:**
     - **Mimikatz:** For extracting passwords, hashes, and other credentials.
     - **PowerShell Empire:** Post-exploitation framework for Windows environments.
     - **Responder:** Helps in LLMNR, NBT-NS, and MDNS poisoning.

### 6. **Reporting:**

   - **Stage Description:** Document findings, vulnerabilities, and recommended fixes in a detailed report.
   
   - **Useful Tools:**
     - **Dradis:** Collaborative reporting tool that integrates findings into one report.
     - **Faraday:** Collaborative penetration testing platform for managing reports and vulnerabilities.
     - **LaTeX/Markdown:** For creating well-formatted and structured reports. -->