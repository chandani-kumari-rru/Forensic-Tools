# Forensic-Tools

A curated collection of **Digital Forensics, Cyber Forensics, and Incident Response tools**, organized by their primary forensic use case.

> **Note:** Always verify tool versions, licenses, and acquisition procedures before using any forensic tool in a real investigation. Preserve original evidence and work on forensic copies whenever possible.

---
# 🔎 Quick DFIR Tool Selection Guide

| Investigation | Recommended Tools |
|---|---|
| Imaging Tool| FTK Imager(windows), Lime(Linux), osxpmem(mac) |
| File Carving Tool | Autopsy/PhotoRec/Scalpel (Cross-Platform Tools)|
| Memory Analysis | Volatility, MemProcFS |
| Network / PCAP | Wireshark, TShark, tcpdump, NetworkMiner |
| Mobile Forensics | Oxygen, MOBILedit, Cellebrite UFED, Magnet AXIOM |
| Extract Metadata | ExifTool|

---

# 🧪 Roadmap Digital Forensics Workflow

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
                    Hash Verification (Cyptography)
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

- [Artifact Analysis Tools](#artifact-analysis-tools)
- [Forensic Imaging Tools](#forensic-imaging-tools)
- [Forensic Carving Tools](#forensic-carving-tools)
- [Memory Forensic Tools](#memory-forensic-tools)
- [Network Forensic Tools](#network-forensic-tools)
- [Mobile Forensic Tools](#mobile-forensic-tools)
- [Incident Response / Triage Tools](#incident-response--triage-tools)

---

# Artifact Analysis Tools
 > Examine digital remnants like logs, registry hives, and browser history to reconstruct user activity and security incidents. 

| Purpose | Tool | Type |
|---|---|---|
| Disk Artifact Tool | [Autopsy](https://www.autopsy.com/) | GUI,Freemium |
| Browser & Internet Artifact Tools | [Autopsy](https://www.autopsy.com/), [Plaso](https://github.com/log2timeline/plaso) | GUI,Freemium |
| Memory Artifact Tool | [Volatility](https://volatilityfoundation.org/), Redline(https://fireeye.market/apps/211364)| GUI,Freemium |
| Network Artifact Tool | [Wireshark](https://www.wireshark.org/) | GUI,Freemium |
| Windows Registry Tool | [Eric Zimmerman's Tools](https://github.com/EricZimmerman/RECmd) | Command-line, Freemium|

---

# Forensic Imaging Tools

| Download | Forensic Tool | Description |
|---|---|---|
| [Click](https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-1) | **FTK Imager** | GUI-based forensic acquisition and preview tool for creating and verifying forensic images. |
| [Click](https://www.gnu.org/software/coreutils/manual/html_node/dd-invocation.html) | **dd/dc3dd** | Standard Unix utility used for bit-by-bit copying and creating raw disk images. |
| [Click](https://guymager.sourceforge.io/) | **Guymager** | Open-source GUI forensic imager supporting raw and EWF image formats with detailed acquisition logs. |
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

# Memory Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://volatilityfoundation.org/) | **Volatility** | Open-source memory forensics framework for analyzing RAM captures and extracting processes, network information, handles, DLLs, and other artifacts. |
| [Click](https://github.com/504ensicsLabs/LiME) | **LiME** | Linux Memory Extractor used to acquire volatile memory from Linux and Android systems. |
| [Click](https://github.com/Velocidex/velociraptor) | **Velociraptor** | Endpoint visibility, digital forensic collection, and incident-response platform capable of collecting volatile and persistent artifacts. |
| [Click](https://github.com/ufrisk/MemProcFS) | **MemProcFS** | Memory-analysis framework that presents a memory dump as a virtual file system for forensic investigation. |

---

# Network Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.wireshark.org/) | **Wireshark** | GUI network protocol analyzer for capturing and analyzing PCAP/PCAPNG traffic. |
| [Click](https://www.tcpdump.org/) | **tcpdump** | Command-line packet capture and network traffic analysis utility. |
| [Click](https://suricata.io/) | **Suricata** | Open-source network threat detection engine supporting IDS, IPS, and network security monitoring. |
| [Click](https://www.netresec.com/?page=NetworkMiner) | **NetworkMiner** | Network forensic analysis tool for extracting hosts, files, credentials, sessions, and other artifacts from captured traffic. |

---

# Mobile Forensic Tools

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.oxygenforensics.com/) | **Oxygen Forensic Detective** | Commercial digital forensic platform for mobile-device, cloud, computer, and application-data analysis. |
| [Click](https://cellebrite.com/en/ufed/) | **Cellebrite UFED** | Commercial mobile-device acquisition and extraction platform. |
| [Click](https://www.magnetforensics.com/products/magnet-axiom/) | **Magnet AXIOM** | Commercial platform for examining mobile, computer, cloud, and other digital evidence. |
| [Click](https://github.com/abrignoni/iLEAPP) | **iLEAPP** | Open-source tool for parsing iOS forensic artifacts. |
| [Click](https://github.com/abrignoni/aLEAPP) | **ALEAPP** | Open-source tool for parsing Android forensic artifacts. |
| [Click](https://github.com/abrignoni/LEAPP) | **LEAPP** | Artifact parsing framework used to extract forensic artifacts from supported platforms. |

---


# Incident Response 

| Download | Tool | Description |
|---|---|---|
| [Click](https://www.kroll.com/en/insights/publications/cyber/kape) | **KAPE** | Rapid collection and processing of Windows forensic artifacts. |
| [Click](https://www.velociraptor.com/) | **Velociraptor** | Endpoint monitoring, forensic collection, and incident-response platform. |
| [Click](https://github.com/ForensicArtifacts/artifacts) | **Forensic Artifacts** | Repository describing common forensic artifacts and their locations across operating systems. |
| [Click](https://github.com/fox-it/Dissect) | **Dissect** | Python-based DFIR framework for examining forensic evidence at scale. |
| [Click](https://github.com/DidierStevens/DidierStevensSuite) | **Didier Stevens Suite** | Collection of Windows forensic, malware-analysis, and incident-response utilities. |

