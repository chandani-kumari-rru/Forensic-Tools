# Forensic-Tools

A curated collection of **Digital Forensics, Cyber Forensics, and Incident Response tools**, organized by their primary forensic use case.

> **Note:** Always verify tool versions, licenses, and acquisition procedures before using any forensic tool in a real investigation. Preserve original evidence and work on forensic copies whenever possible.

---
# 🔎 Quick DFIR Tool Selection Guide

| Investigation Task | Recommended Tools |
|---|---|
| Disk Imaging | FTK Imager, Guymager, dc3dd, dd |
| Damaged Disk Acquisition | GNU ddrescue |
| E01 / EWF Analysis | libewf, Autopsy, The Sleuth Kit |
| File Carving | PhotoRec, Scalpel, Foremost, Autopsy |
| Windows Registry | Registry Explorer, RECmd |
| Memory Analysis | Volatility, MemProcFS |
| Network / PCAP | Wireshark, TShark, tcpdump, NetworkMiner |
| Disk / File System | Autopsy, The Sleuth Kit |
| Mobile Forensics | Cellebrite UFED, Magnet AXIOM, Oxygen Forensic Detective |
| Browser Artifacts | Hindsight, Autopsy |
| Timeline | Plaso, Timeline Explorer, Autopsy |
| Malware Analysis | Ghidra, IDA Pro, x64dbg, radare2 |
| Rapid Triage | KAPE, Velociraptor |
| Hash Verification | SHA-256, md5sum, HashCheck |

---

# 🧪 Suggested Digital Forensics Workflow

```text
                    DIGITAL FORENSICS
                           │
                           ▼
                  Evidence Identification
                           │
                           ▼
                       Preservation
                           │
                           ▼
                  Forensic Acquisition
                           │
                           ▼
                    Hash Verification
                           │
                           ▼
              +------------+------------+
              │            │            │
              ▼            ▼            ▼
          Disk/FS       Memory       Network
          Analysis      Analysis      Analysis
              │            │            │
              +------------+------------+
                           │
                           ▼
                   Artifact Extraction
                           │
                           ▼
                   Timeline Analysis
                           │
                           ▼
                   Evidence Correlation
                           │
                           ▼
                  Findings & Reporting
                           │
                           ▼
                       Presentation
```

---
## 📑 Table of Contents

- [Forensic Imaging Tools](#forensic-imaging-tools)
- [Forensic Carving Tools](#forensic-carving-tools)
- [Windows Artifact Analysis Tools](#windows-artifact-analysis-tools)
- [Memory Forensic Tools](#memory-forensic-tools)
- [Network Forensic Tools](#network-forensic-tools)
- [Disk & File-System Forensic Tools](#disk--file-system-forensic-tools)
- [Mobile Forensic Tools](#mobile-forensic-tools)
- [Browser & Internet Artifact Tools](#browser--internet-artifact-tools)
- [Email Forensic Tools](#email-forensic-tools)
- [Timeline Analysis Tools](#timeline-analysis-tools)
- [Malware Analysis / Reverse Engineering Tools](#malware-analysis--reverse-engineering-tools)
- [Hashing & Evidence Verification Tools](#hashing--evidence-verification-tools)
- [Incident Response / Triage Tools](#incident-response--triage-tools)
- [Quick DFIR Tool Selection Guide](#-quick-dfir-tool-selection-guide)
- [Suggested Digital Forensics Workflow](#-suggested-digital-forensics-workflow)

---

# Forensic Imaging Tools

| Download | Forensic Tool | Description |
|---|---|---|
| [Click](https://www.gnu.org/software/coreutils/manual/html_node/dd-invocation.html) | **dd** | Standard Unix utility used for bit-by-bit copying and creating raw disk images. |
| [Click](https://sourceforge.net/projects/dc3dd/) | **dc3dd** | Enhanced forensic version of `dd` with hashing, logging, and verification capabilities. |
| [Click](https://www.gnu.org/software/ddrescue/) | **GNU ddrescue** | Data-recovery utility designed to efficiently recover data from damaged or failing storage media. |
| [Click](https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-1) | **FTK Imager** | GUI-based forensic acquisition and preview tool for creating and verifying forensic images. |
| [Click](https://guymager.sourceforge.io/) | **Guymager** | Open-source GUI forensic imager supporting raw and EWF image formats with detailed acquisition logs. |
| [Click](https://github.com/libyal/libewf) | **libewf / EWF Tools** | Open-source library and utilities for handling Expert Witness Format (E01/EWF) forensic images. |
| [Click](https://www.kroll.com/en/insights/publications/cyber/kape) | **KAPE** | Rapid triage and forensic artifact collection tool for Windows systems. |

---

# Forensic Carving Tools

| Download | Forensic Tool | Description |
|---|---|---|
| [Click](https://www.autopsy.com/) | **Autopsy** | Open-source digital forensics platform with file-system analysis, keyword search, timeline analysis, and carving capabilities. |
| [Click](https://github.com/simsong/bulk_extractor) | **bulk_extractor** | Extracts useful forensic information such as email addresses, URLs, credit-card-like numbers, and other features directly from disk images. |
| [Click](https://www.cgsecurity.org/wiki/PhotoRec) | **PhotoRec** | File-carving utility that recovers files by identifying known file signatures rather than relying on the file system. |
| [Click](https://github.com/sleuthkit/scalpel) | **Scalpel** | High-performance file-carving tool based on file headers, footers, and configurable carving rules. |
| [Click](https://foremost.sourceforge.net/) | **Foremost** | File-carving utility that recovers files using configurable header and footer signatures. |

---

# Windows Artifact Analysis Tools

| Download | Tool | Primary Use |
|---|---|---|
| [Click](https://www.magnetforensics.com/products/magnet-axiom/) | **Magnet AXIOM** | Commercial forensic platform for analyzing computer, mobile, cloud, and other digital artifacts. |
| [Click](https://github.com/EricZimmerman/RegistryExplorer) | **Registry Explorer** | Advanced Windows Registry hive analysis, including transaction-log support and artifact interpretation. |
| [Click](https://github.com/EricZimmerman/RECmd) | **RECmd** | Command-line Windows Registry analysis and artifact extraction. |
| [Click](https://github.com/EricZimmerman/AmcacheParser) | **AmcacheParser** | Parses Windows Amcache.hve data for application execution and installation-related artifacts. |
| [Click](https://github.com/EricZimmerman/AppCompatCacheParser) | **AppCompatCacheParser** | Parses ShimCache / AppCompatCache data from Windows Registry hives. |
| [Click](https://github.com/EricZimmerman/BAMParser) | **BAMParser** | Parses Background Activity Moderator artifacts containing information about executable activity. |
| [Click](https://github.com/EricZimmerman/UserAssist) | **UserAssist** | Parses UserAssist Registry artifacts containing information about GUI-based application execution. |
| [Click](https://github.com/EricZimmerman/TimelineExplorer) | **Timeline Explorer** | GUI tool for examining CSV/TSV forensic timelines and artifact output. |
| [Click](https://github.com/EricZimmerman/PECmd) | **PECmd** | Parses Windows Prefetch files to extract execution-related metadata. |

### Common Windows Execution / Timestamp Artifacts

```text
AmCache
   │
   ├── Application installation / execution-related information
   │
ShimCache / AppCompatCache
   │
   ├── Application compatibility cache information
   │
BAM / DAM
   │
   ├── Background Activity information
   │
UserAssist
   │
   ├── GUI application execution information
   │
Prefetch
   │
   └── Application execution and performance-related information
```

> **Important:** These artifacts do not all represent the same type of "execution proof." Their meaning, timestamp semantics, retention, and evidentiary value differ by Windows version and artifact state. Interpret them in context and correlate multiple artifacts.

---

# Memory Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://volatilityfoundation.org/) | **Volatility** | Open-source memory forensics framework for analyzing RAM captures and extracting processes, network information, handles, DLLs, and other artifacts. |
| [Click](https://github.com/504ensicsLabs/LiME) | **LiME** | Linux Memory Extractor used to acquire volatile memory from Linux and Android systems. |
| [Click](https://github.com/Velocidex/velociraptor) | **Velociraptor** | Endpoint visibility, digital forensic collection, and incident-response platform capable of collecting volatile and persistent artifacts. |
| [Click](https://github.com/ufrisk/MemProcFS) | **MemProcFS** | Memory-analysis framework that presents a memory dump as a virtual file system for forensic investigation. |

### Common Memory Forensics Workflow

```text
RAM Acquisition
      ↓
Memory Image Verification
      ↓
Operating-System Identification
      ↓
Process Analysis
      ↓
DLL / Module Analysis
      ↓
Network Connection Analysis
      ↓
Command-Line / Handle Analysis
      ↓
Malware / Injection Investigation
      ↓
Evidence Correlation & Reporting
```

---

# Network Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.wireshark.org/) | **Wireshark** | GUI network protocol analyzer for capturing and analyzing PCAP/PCAPNG traffic. |
| [Click](https://www.tcpdump.org/) | **tcpdump** | Command-line packet capture and network traffic analysis utility. |
| [Click](https://zeek.org/) | **Zeek** | Network security monitor that generates structured logs and metadata from network traffic. |
| [Click](https://suricata.io/) | **Suricata** | Open-source network threat detection engine supporting IDS, IPS, and network security monitoring. |
| [Click](https://www.netresec.com/?page=NetworkMiner) | **NetworkMiner** | Network forensic analysis tool for extracting hosts, files, credentials, sessions, and other artifacts from captured traffic. |
| [Click](https://github.com/fox-it/Dissect) | **Dissect** | Digital forensics framework that includes tools and libraries useful for incident-response and network-related investigations. |
| [Click](https://www.tcpdump.org/manpages/tcpdump.1.html) | **TShark** | Command-line network protocol analyzer distributed with Wireshark. |

---

# Disk & File-System Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.sleuthkit.org/) | **The Sleuth Kit (TSK)** | Collection of command-line tools for file-system and disk-image forensic analysis. |
| [Click](https://www.autopsy.com/) | **Autopsy** | GUI digital forensics platform built around The Sleuth Kit and additional forensic modules. |
| [Click](https://github.com/EricZimmerman/NTFS) | **MFTECmd** | Parses NTFS Master File Table (MFT) records and related NTFS metadata. |
| [Click](https://github.com/EricZimmerman/LECmd) | **LECmd** | Parses Windows LNK shortcut files and extracts forensic metadata. |
| [Click](https://github.com/EricZimmerman/JLECmd) | **JLECmd** | Parses Windows Jump List files for application and file-access artifacts. |
| [Click](https://github.com/EricZimmerman/SDBExplorer) | **SDBExplorer** | Examines Windows Shim Database (SDB) files. |

---

# Mobile Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://cellebrite.com/en/ufed/) | **Cellebrite UFED** | Commercial mobile-device acquisition and extraction platform. |
| [Click](https://www.magnetforensics.com/products/magnet-axiom/) | **Magnet AXIOM** | Commercial platform for examining mobile, computer, cloud, and other digital evidence. |
| [Click](https://www.oxygenforensics.com/) | **Oxygen Forensic Detective** | Commercial digital forensic platform for mobile-device, cloud, computer, and application-data analysis. |
| [Click](https://github.com/abrignoni/iLEAPP) | **iLEAPP** | Open-source tool for parsing iOS forensic artifacts. |
| [Click](https://github.com/abrignoni/aLEAPP) | **ALEAPP** | Open-source tool for parsing Android forensic artifacts. |
| [Click](https://github.com/abrignoni/LEAPP) | **LEAPP** | Artifact parsing framework used to extract forensic artifacts from supported platforms. |

> Commercial tools may require a license, dongle, account, or institutional authorization.

---

# Browser & Internet Artifact Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://github.com/obsidianforensics/hindsight) | **Hindsight** | Extracts and analyzes Chromium-based browser artifacts such as history, downloads, cookies, and cache-related data. |
| [Click](https://github.com/log2timeline/plaso) | **Plaso** | Framework for extracting timestamped events from many forensic artifact sources. |
| [Click](https://www.sleuthkit.org/autopsy/) | **Autopsy** | Supports browser history, downloads, cookies, web artifacts, and other Internet-related evidence. |

### Common Browser Artifacts

```text
Browser History
Downloads
Cookies
Cache
Bookmarks
Saved Logins
Web Storage
Session Data
Search Queries
Autocomplete Data
```

---

# Email Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.sleuthkit.org/autopsy/) | **Autopsy** | Can assist with analysis of email artifacts and associated files. |
| [Click](https://github.com/SpamScope/mail-parser) | **mail-parser** | Python-based email parsing library useful for extracting headers and message information. |
| [Click](https://github.com/DidierStevens/DidierStevensSuite) | **oledump / Didier Stevens Suite** | Collection of forensic and malware-analysis tools, including utilities useful for examining suspicious email attachments and Office documents. |
| [Click](https://www.maltiverse.com/) | **Maltiverse** | Threat-intelligence platform that can help investigate indicators extracted from suspicious messages or attachments. |

### Important Email Evidence

```text
From / To / CC / BCC
Message-ID
Date / Time
Received Headers
Return-Path
X-Originating-IP (when present)
Attachments
URLs
Authentication Results
SPF / DKIM / DMARC
```

---

# Timeline Analysis Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://github.com/log2timeline/plaso) | **Plaso / log2timeline** | Creates super timelines by extracting timestamped events from many forensic artifacts. |
| [Click](https://github.com/EricZimmerman/TimelineExplorer) | **Timeline Explorer** | GUI application for viewing, filtering, and analyzing large forensic timeline datasets. |
| [Click](https://www.sleuthkit.org/autopsy/) | **Autopsy Timeline** | Provides timeline visualization and event analysis within Autopsy. |

### Timeline Correlation

```text
File Created
     ↓
File Modified
     ↓
File Accessed
     ↓
Application Execution
     ↓
UserAssist / Prefetch / BAM / AmCache
     ↓
Browser Activity
     ↓
Network Activity
     ↓
External Device Activity
     ↓
Final Event Timeline
```

---

# Malware Analysis / Reverse Engineering Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.ghidra-sre.org/) | **Ghidra** | NSA-developed software reverse-engineering framework for analyzing compiled programs. |
| [Click](https://hex-rays.com/ida-pro/) | **IDA Pro** | Commercial disassembler and debugger widely used for reverse engineering. |
| [Click](https://x64dbg.com/) | **x64dbg** | Open-source debugger for Windows applications. |
| [Click](https://github.com/radareorg/radare2) | **radare2** | Open-source reverse-engineering framework for binary analysis. |
| [Click](https://cuckoosandbox.org/) | **Cuckoo Sandbox** | Automated malware-analysis and sandboxing framework. |
| [Click](https://www.virustotal.com/) | **VirusTotal** | Online service for analyzing files, URLs, domains, and IP addresses using multiple security engines and intelligence sources. |

---

# Hashing & Evidence Verification Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html) | **md5sum** | Generates MD5 hashes for integrity verification and identification. |
| [Click](https://www.gnu.org/software/coreutils/manual/html_node/sha2-utilities.html) | **sha256sum** | Generates SHA-256 hashes for evidence integrity verification. |
| [Click](https://www.nist.gov/publications/secure-hash-standard) | **SHA-2 / SHA-256** | Cryptographic hashing standard commonly used to verify digital evidence integrity. |
| [Click](https://github.com/gurnec/HashCheck) | **HashCheck** | Windows shell extension for calculating and verifying file hashes. |

### Evidence Integrity Concept

```text
Original Evidence
       ↓
Forensic Acquisition
       ↓
Hash Calculation
       ↓
Forensic Image
       ↓
Hash Verification
       ↓
Analysis Copy
       ↓
Final Verification
       ↓
Forensic Report
```

> Hash values help demonstrate that evidence has remained unchanged. Maintain complete acquisition logs, examiner notes, chain-of-custody records, and tool/version information as part of the forensic process.

---

# Incident Response / Triage Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.kroll.com/en/insights/publications/cyber/kape) | **KAPE** | Rapid collection and processing of Windows forensic artifacts. |
| [Click](https://www.velociraptor.com/) | **Velociraptor** | Endpoint monitoring, forensic collection, and incident-response platform. |
| [Click](https://github.com/ForensicArtifacts/artifacts) | **Forensic Artifacts** | Repository describing common forensic artifacts and their locations across operating systems. |
| [Click](https://github.com/fox-it/Dissect) | **Dissect** | Python-based DFIR framework for examining forensic evidence at scale. |
| [Click](https://github.com/DidierStevens/DidierStevensSuite) | **Didier Stevens Suite** | Collection of Windows forensic, malware-analysis, and incident-response utilities. |

---

