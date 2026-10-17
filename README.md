# Pustaka Terbuka — JPPKK (Perpustakaan Jabatan Pendidikan Politeknik dan Kolej Komuniti)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Perpustakaan Jabatan Pendidikan Politeknik dan Kolej Komuniti (JPPKK) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Perpustakaan Jabatan Pendidikan Politeknik dan Kolej Komuniti** (`JPPKK`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `politeknik` |
| **Agency Code** | `JPPKK` |
| **Official Name** | Perpustakaan Jabatan Pendidikan Politeknik dan Kolej Komuniti |
| **Institution Type** | `university` |
| **State / Territory** | Putrajaya |
| **Target End Bib** | 300,000 |
| **OPAC Base URL** | [https://library.polycc.edu.my/](https://library.polycc.edu.my/) |
| **Subject Focus** | Vocational education, mechanical trades, hospitality, civil engineering, and TVET |

---

## Directory Structure

```text
politeknik/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/politeknik/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/politeknik/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-politeknik.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/politeknik/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Perpustakaan Jabatan Pendidikan Politeknik dan Kolej Komuniti (JPPKK)** & **Pustaka Terbuka**.
