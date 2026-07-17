# SOC Güvenlik Proje Portföyü / SOC Security Project Portfolio

Bu depo, Murat Karateke'nin SOC Analyst hedefiyle yürüttüğü, uçtan uca bir SOC (Security Operations Center) ortamı kurulumunu belgeleyen 9 projeden oluşur — çevre güvenliğinden (perimeter security) ağ/host tespitine, SIEM korelasyonuna, DFIR'a, otomasyona ve saldırgan perspektifli değerlendirmeye (zafiyet taraması) kadar. Her proje gerçek komutlar, gerçek servis/log çıktıları ve ekran görüntüsü kanıtlarıyla belgelenmiştir.

This repository is Murat Karateke's SOC Analyst portfolio, consisting of 9 projects documenting an end-to-end SOC (Security Operations Center) build — from perimeter security to network/host detection, SIEM correlation, DFIR, automation, and an attacker-perspective assessment (vulnerability assessment). Each project is documented with real commands, real service/log output, and screenshot evidence.

---

## Durum / Status

| Simge | Anlamı (TR) | Meaning (EN) |
|---|---|---|
| ✅ | Ekran görüntüsü kanıtlarıyla tam yayında | Fully published with screenshot evidence |
| 🕒 | README hazır, ekran görüntüleri bekleniyor | README ready, screenshots pending |
| 🔜 | Yakında | Coming soon |

**Tam/hazır (✅): Proje 01-09** · **Yakında (🔜): Proje 10-11**

---

## Türkçe (TR)

| # | Proje | Açıklama | Araçlar | Durum | README |
|---|---|---|---|---|---|
| 01 | Web Çevre Güvenliği | Cloudflare + Nginx + ModSecurity WAF ile çok katmanlı perimeter savunması; XSS/SQLi gerçek saldırılarla ve sqlmap ile test edildi | Cloudflare, Nginx, ModSecurity, OWASP CRS 3.3.8 | ✅ | [TR/01](TR/01-web-perimeter-security/README.md) |
| 02 | Ağ Trafiği Tespit Laboratuvarı | İmza tabanlı IDS/IPS (Suricata) ve protokol seviyesi ağ görünürlüğü (Zeek) birlikte kuruldu | Suricata, Zeek, zeekctl | ✅ | [TR/02](TR/02-network-traffic-detection-lab/README.md) |
| 03 | Host Tabanlı Tehdit Tespiti | Host seviyesinde runtime tespit + otomatik IP engelleme, gerçek saldırı denemeleriyle test edildi; Fail2Ban kök neden analizi (Cloudflare real-IP sorunu) projenin öne çıkan bölümü | Falco, Auditd, CrowdSec, Fail2Ban | ✅ | [TR/03](TR/03-host-based-threat-detection/README.md) |
| 04 | SIEM Log Korelasyon Platformu | Dağınık logların (WAF, IDS, host) merkezi bir SIEM'de toplanıp MITRE ATT&CK ile korelasyonu, Splunk ile çapraz doğrulama | Wazuh (Manager/Indexer/Dashboard), Splunk Enterprise | ✅ | [TR/04](TR/04-siem-log-correlation-platform/README.md) |
| 05 | DFIR Dijital Adli Bilişim Laboratuvarı | Canlı sistem üzerinde uzaktan artefakt toplama, VQL sorgulama ve olay müdahalesi altyapısı | Velociraptor | ✅ | [TR/05](TR/05-dfir-digital-forensics-lab/README.md) |
| 06 | Zararlı Yazılım Tespiti Otomasyonu | Otomatik zamanlanmış tam sistem taraması, EICAR test dosyasıyla tespit doğrulaması | ClamAV, cron | ✅ | [TR/06](TR/06-malware-detection-automation/README.md) |
| 07 | Otomatik Yedekleme ve Kurtarma Sistemi | Bütünlük doğrulamalı (SHA256) ve saklama politikalı (retention) otomatik yedekleme, geri yükleme testi | Bash, cron, tar, sha256sum | ✅ | [TR/07](TR/07-automated-backup-recovery-system/README.md) |
| 08 | n8n ile SOC Otomasyonu | SIEM verisinden otomatik Cloudflare aksiyonuna uzanan bir SOAR iş akışı | n8n (Docker), Wazuh API, Splunk API, Cloudflare API | ✅ | [TR/08](TR/08-soc-automation-with-n8n/README.md) |
| 09 | Zafiyet Değerlendirme Laboratuvarı | karateke.online'ın kendisine karşı dış saldırgan perspektifiyle CVE tabanlı zafiyet taraması; 0 kritik/yüksek bulgu, WAF fingerprint tespiti/tarpitting bulguları | Kali Linux, GVM/OpenVAS, Nuclei, Nikto, Nmap | ✅ | [TR/09](TR/09-vulnerability-assessment-lab/README.md) |
| 10 | Active Directory Güvenlik Değerlendirmesi | İzole bir Windows Server lab ortamında AD DS altyapısı kurulup enum4linux, CrackMapExec, BloodHound ile yaygın yanlış yapılandırmaların tespiti | Windows Server, Kali Linux, enum4linux, CrackMapExec, BloodHound | 🔜 | — |
| 11 | Web Uygulaması Sızma Testi | İzole, kasıtlı-zafiyetli bir hedef (DVWA) üzerinde Burp Suite ile OWASP Top 10 kapsamındaki zafiyet sınıflarının sistematik testi | Burp Suite, DVWA | 🔜 | — |

## English (EN)

| # | Project | Description | Tools | Status | README |
|---|---|---|---|---|---|
| 01 | Web Perimeter Security | Multi-layered perimeter defense with Cloudflare + Nginx + ModSecurity WAF; XSS/SQLi tested with real attacks and sqlmap | Cloudflare, Nginx, ModSecurity, OWASP CRS 3.3.8 | ✅ | [EN/01](EN/01-web-perimeter-security/README.md) |
| 02 | Network Traffic Detection Lab | Signature-based IDS/IPS (Suricata) combined with protocol-level network visibility (Zeek) | Suricata, Zeek, zeekctl | ✅ | [EN/02](EN/02-network-traffic-detection-lab/README.md) |
| 03 | Host-Based Threat Detection | Host-level runtime detection + automated IP blocking, tested with real attack attempts; the Fail2Ban root-cause analysis (Cloudflare real-IP issue) is the project's standout section | Falco, Auditd, CrowdSec, Fail2Ban | ✅ | [EN/03](EN/03-host-based-threat-detection/README.md) |
| 04 | SIEM Log Correlation Platform | Correlating scattered logs (WAF, IDS, host) in a central SIEM with MITRE ATT&CK mapping, cross-verified with Splunk | Wazuh (Manager/Indexer/Dashboard), Splunk Enterprise | ✅ | [EN/04](EN/04-siem-log-correlation-platform/README.md) |
| 05 | DFIR Digital Forensics Lab | Remote live-system artifact collection, VQL querying, and incident response infrastructure | Velociraptor | ✅ | [EN/05](EN/05-dfir-digital-forensics-lab/README.md) |
| 06 | Malware Detection Automation | Automated scheduled full-system scanning, detection verified with the EICAR test file | ClamAV, cron | ✅ | [EN/06](EN/06-malware-detection-automation/README.md) |
| 07 | Automated Backup & Recovery System | Integrity-verified (SHA256) automated backups with a retention policy and restore testing | Bash, cron, tar, sha256sum | ✅ | [EN/07](EN/07-automated-backup-recovery-system/README.md) |
| 08 | SOC Automation with n8n | A SOAR workflow taking SIEM data all the way to an automated Cloudflare action | n8n (Docker), Wazuh API, Splunk API, Cloudflare API | ✅ | [EN/08](EN/08-soc-automation-with-n8n/README.md) |
| 09 | Vulnerability Assessment Lab | CVE-based vulnerability scan against karateke.online itself from an external attacker's perspective; 0 critical/high findings, WAF fingerprinting/tarpitting findings | Kali Linux, GVM/OpenVAS, Nuclei, Nikto, Nmap | ✅ | [EN/09](EN/09-vulnerability-assessment-lab/README.md) |
| 10 | Active Directory Security Assessment | Building AD DS infrastructure in an isolated Windows Server lab and detecting common misconfigurations with enum4linux, CrackMapExec, and BloodHound | Windows Server, Kali Linux, enum4linux, CrackMapExec, BloodHound | 🔜 | — |
| 11 | Web Application Penetration Testing | Systematic testing of OWASP Top 10 vulnerability classes with Burp Suite against an isolated, intentionally-vulnerable target (DVWA) | Burp Suite, DVWA | 🔜 | — |

---

## Genel Mimari Akış / Overall Architecture Flow

```
  Perimeter (01) → Network/Host Detection (02, 03) → SIEM Correlation (04)
        → DFIR (05) → Malware Automation (06) → Backup/Recovery (07)
        → SOAR Automation (08)
        → Offensive Assessment: Vulnerability Scan (09)
```
