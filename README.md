# Forensic-Tools

A curated collection of **Digital Forensics, Cyber Forensics, and Incident Response tools**, organized by their primary forensic use case.

> **Note:** Always verify tool versions, licenses, and acquisition procedures before using any forensic tool in a real investigation. Preserve original evidence and work on forensic copies whenever possible.

---
# 🔎 Quick Review Forensic Tools

| Investigation Tool| Recommended Tools |
|---|---|
| Disk Imaging Tool| FTK Imager(windows), Lime(Linux), osxpmem(mac) |
| File Carving Tool | FTK, Autopsy|
| Browser Artifact | KAPE(windows) |
| Image Metadata Extraction Tool | ExifTool|
| Memory Analysis | Volatility, Redline |
| Network / PCAP | Wireshark, TShark, tcpdump, NetworkMiner |
| Mobile Forensics | Oxygen, MOBILedit, Cellebrite UFED, Magnet AXIOM |

---
## 📑 Table of Contents

- [Forensic Imaging & Carving Tools](#forensic-imaging-and-carving-tools)
- [Memory Forensic Tools](#memory-forensic-tools)
- [Network Forensic Tools](#network-forensic-tools)
- [Mobile Forensic Tools](#mobile-forensic-tools)
- [Incident Response](#incident-response)
- [Forensic Workflow](#forensics-workflow)

---

# Forensic Imaging and Carving Tools
  > [Autopsy](https://www.autopsy.com/download/) is not a Forensic Imaging Tool But it is a Forensic Image Analysis Tool & Also File Carving Tool.
  > [KAPE](https://www.kroll.com/en/insights/publications/cyber/kape) is used for Browser Artifact Tool. 

| Forensic Tool | Description |
|---|---|
| [FTK Imager](https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-1) | GUI-based forensic acquisition and preview tool for creating and verifying forensic images. |
| [dd/dc3dd](https://www.gnu.org/software/coreutils/manual/html_node/dd-invocation.html) | Standard Unix utility used for bit-by-bit copying and creating raw disk images. |
| [Guymager](https://guymager.sourceforge.io/) | Open-source GUI forensic imager supporting raw and EWF image formats with detailed acquisition logs. |

---

# Memory Forensic Tools

| ForensicTool | Description |
|---|---|
| [Volatility](https://volatilityfoundation.org/) | Open-source memory forensics framework for analyzing RAM captures and extracting processes, network information, handles, DLLs, and other artifacts. | 
| [Redline](https://fireeye.market/apps/211364) | It enables security analysts to collect and analyze data such as running processes, memory images, registry entries, network connections, and file metadata. | 
| [LiME](https://github.com/504ensicsLabs/LiME) | Linux Memory Extractor used to acquire volatile memory from Linux and Android systems. |
| [Velociraptor](https://github.com/Velocidex/velociraptor) | Endpoint visibility, digital forensic collection, and incident-response platform capable of collecting volatile and persistent artifacts. |

---

# Network Forensic Tools

| Forensic Tool | Description |
|---|---|
| [Wireshark](https://www.wireshark.org/) | GUI network protocol analyzer for capturing and analyzing PCAP/PCAPNG traffic. |
| [tcpdump](https://www.tcpdump.org/) | Command-line packet capture and network traffic analysis utility. |
| [Suricata](https://suricata.io/) | Open-source network threat detection engine supporting IDS, IPS, and network security monitoring. |
| [NetworkMiner](https://www.netresec.com/?page=NetworkMiner)| **NetworkMiner** | Network forensic analysis tool for extracting hosts, files, credentials, sessions, and other artifacts from captured traffic. |

---

# Mobile Forensic Tools
| Forensic Tool | Description |
|---|---|
| [Oxygen Forensic](https://www.oxygenforensics.com/) | Commercial digital forensic platform for mobile-device, cloud, computer, and application-data analysis. |
| [Cellebrite UFED](https://cellebrite.com/en/ufed/) | Commercial mobile-device acquisition and extraction platform. |
| [Magnet AXIOM](https://www.magnetforensics.com/products/magnet-axiom/) | **Magnet AXIOM** | Commercial platform for examining mobile, computer, cloud, and other digital evidence. |
| [iLEAPP](https://github.com/abrignoni/iLEAPP) | Open-source tool for parsing iOS forensic artifacts. |
| [ALEAPP](https://github.com/abrignoni/aLEAPP) | Open-source tool for parsing Android forensic artifacts. |

---


# Incident Response 

| DFIR Tool | Description |
|---|---|
| [KAPE](https://www.kroll.com/en/insights/publications/cyber/kape) | Rapid collection and processing of Windows forensic artifacts. |
| [Velociraptor](https://www.velociraptor.com/) | Endpoint monitoring, forensic collection, and incident-response platform. |
| [Dissect](https://github.com/fox-it/Dissect) | Python-based DFIR framework for examining forensic evidence at scale. |


---

# Forensics Workflow

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


