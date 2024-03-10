# **Web Tools**

Oczywiście, tutaj jest lista najważniejszych etapów testów penetracyjnych aplikacji internetowych wraz z przykładowymi narzędziami, sformatowana w formie Markdown w języku polskim:

### 1. **Rekonesans:**

   - **Opis etapu:** Zbieranie informacji o aplikacji internetowej i jej infrastrukturze.
   
   - **Przydatne narzędzia:**
     - **Sublist3r/Gobuster:** Do wykrywania subdomen.
     - **TheHarvester:** Pomaga w zbieraniu informacji z publicznych źródeł.
     - **[Nmap](NMAP_cheatsheet.pdf):** Do odkrywania i mapowania sieci.

### 2. **Skanowanie:**

   - **Opis etapu:** Identyfikacja podatności i słabości w testowanej aplikacji internetowej.
   
   - **Przydatne narzędzia:**
     - **Nikto:** Przeprowadza kompleksowe testy na serwerach WWW w poszukiwaniu podatności.
     - **OWASP ZAP:** Skaner bezpieczeństwa aplikacji internetowych do wykrywania podatności.
     - **Burp Suite:** Zawiera narzędzia do skanowania, przeszukiwania i analizy bezpieczeństwa aplikacji internetowych.

### 3. **Eskploracja:**

   - **Opis etapu:** Odkrywanie jak najwięcej informacji o aplikacji internetowej, takich jak katalogi, pliki i używane technologie.
   
   - **Przydatne narzędzia:**
     - **Dirb/Dirbuster:** Do siłowego przeszukiwania katalogów i plików na serwerach WWW.
     - **Wfuzz:** Pomaga w odkrywaniu ukrytego lub niepowiązanego kontentu.
     - **Gobuster:** Narzędzie do siłowego przeszukiwania katalogów i plików.

### 4. **Eksploracja podatności:**

   - **Opis etapu:** Wykorzystanie zidentyfikowanych podatności w celu oceny ich wpływu i uzyskania głębszego dostępu.
   
   - **Przydatne narzędzia:**
     - **Metasploit Framework:** Do tworzenia, testowania i wykonywania kodu wykorzystującego podatność na docelowym systemie.
     - **SQLMap:** Specjalnie zaprojektowane do wykrywania i wykorzystywania podatności na wstrzykiwanie SQL.
     - **BeEF (Browser Exploitation Framework):** Koncentruje się na podatnościach przeglądarki internetowej.
     - **[RevShells](https://www.revshells.com/):** prosty "generator" reverse shell-i.

### 5. **Po-eksploatacja:**

   - **Opis etapu:** Utrzymanie dostępu, zbieranie dalszych informacji i eskalacja uprawnień, jeśli to możliwe.
   
   - **Przydatne narzędzia:**
     - **Mimikatz:** Do wydobywania haseł, hashy i innych danych uwierzytelniających.
     - **PowerShell Empire:** Platforma po-eksploatacyjna dla środowisk Windows.
     - **Responder:** Pomaga w truciznowaniu LLMNR, NBT-NS i MDNS.
     - **[PEASS-ng](https://github.com/carlospolop/PEASS-ng/tree/master):** Privilege Escalation Awesome Scripts SUITE (with colors)
     - **[GTFObins](gtfobins.github.io):** curated list of Unix binaries that can be used to bypass local security restrictions in misconfigured systems.
 
### 6. **Raportowanie:**

   - **Opis etapu:** Dokumentowanie wyników, podatności i zalecanych poprawek w szczegółowym raporcie.
   
   - **Przydatne narzędzia:**
     - **Dradis:** Narzędzie do wspólnego tworzenia raportów, które integruje wyniki w jeden raport.
     - **Faraday:** Wspólna platforma do testów penetracyjnych do zarządzania raportami i podatnościami.
     - **LaTeX/Markdown:** Do tworzenia czytelnych i dobrze sformatowanych raportów.

# **IN ENG:**

### 1. **Reconnaissance:**

   - **Stage Description:** Gather information about the target web application and its infrastructure.
   
   - **Useful Tools:**
     - **Sublist3r:** For subdomain enumeration.
     - **TheHarvester:** Helps in email harvesting and gathering information from public sources.
     - **Nmap:** For network discovery and mapping.

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
     - **LaTeX/Markdown:** For creating well-formatted and structured reports.