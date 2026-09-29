# 🚩 Tools Source — DFIR & Reverse Engineering 

Welcome to **tools Source**, a curated command-line reference and tool documentation repository designed for Digital Forensics, Incident Response (DFIR), and Malware Reverse Engineering.

---

## 📁 Repository Structure

```text
hack4gov-source/
├── README.md
├── disk-forensics/
│   ├── sleuth-kit.md       # TSK CLI suite (mmls, fls, icat, fsstat)
│   ├── ewf-tools.md         # Expert Witness Format (.E01) handling
│   ├── testdisk.md          # Partition recovery & repair
│   ├── foremost.md          # File carving via headers/footers
│   └── autopsy.md           # Digital forensics browser interface
├── memory-forensics/
│   └── volatility3.md       # Volatile memory (RAM) analysis
├── timeline/
│   └── plaso.md             # Super-timeline extraction (log2timeline / psort)
├── file-metadata/
│   ├── exiftool.md          # Document & media metadata extraction
│   ├── binwalk.md           # Firmware analysis & binary extraction
│   └── strings-file.md      # Built-in Linux static analysis tools
├── network-forensics/
│   ├── wireshark.md         # GUI packet inspection
│   ├── tshark.md            # CLI packet filtering & field extraction
│   └── tcpdump.md           # Lightweight packet capture engine
└── malware-reverse-engineering/
    ├── yara.md              # Pattern-matching malware rules
    ├── ghidra.md            # SRE suite & headless analysis
    ├── radare2.md           # CLI disassembler & debugger
    └── gdb.md               # GNU dynamic binary debugger
