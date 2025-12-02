# 🛡️ Chromium-Ad-Detection-Filter-Archive-Data-Repository

## Project Purpose

This repository serves as the immutable, professionally curated historical archive for ad detection and subresource filter lists formerly utilized by the Chromium project. It preserves the data lineage critical for security research, privacy studies, and understanding the evolution of web content blocking mechanisms.

---

## 👁️ Visual Authority & Artifact Integrity

| Metric | Status |
| :--- | :--- |
| **Build Status** | [![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository/ci.yml?style=flat-square)](https://github.com/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository/actions/workflows/ci.yml) |
| **Code Coverage** | [![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository?style=flat-square)](https://codecov.io/gh/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository) |
| **License** | [![License](https://img.shields.io/github/license/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository?style=flat-square)](LICENSE) |
| **Stars** | [![GitHub Stars](https://img.shields.io/github/stars/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository?style=flat-square)](https://github.com/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository) |

[⭐ Star ⭐ this Repo if you find historical data preservation valuable!](https://github.com/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository)

---

## 📄 BLUF: Value Proposition

This repository is the definitive, version-controlled historical ledger for Chromium's content-blocking filter lists, designed for static analysis, compliance auditing, and academic research into web privacy trends.

## 🏛️ Architecture Overview (Data Preservation Model)

Since this is an archive, the architecture focuses on immutable data structure and retrieval integrity. We model this as a **Read-Only Data Manifest System (RDMS)**.

text
/Chromium-Ad-Detection-Filter-Archive-Data-Repository
├── data/                          # Core archived filter list snapshots
│   ├── 2020-01-01/                # Versioned time-based directories
│   │   └── easylist.txt
│   └── 2022-06-15/                # Example: Mid-cycle snapshot
│       └── privacy_practices.json
├── metadata/                      # Structural documentation
│   └── schema.json
├── .github/
│   └── workflows/ci.yml           # Validation pipeline (data integrity checks)
├── LICENSE
└── README.md


## 📚 Table of Contents

1.  [👁️ Visual Authority & Artifact Integrity](#-visual-authority--artifact-integrity)
2.  [📄 BLUF: Value Proposition](#-bluf-value-proposition)
3.  [🏛️ Architecture Overview (Data Preservation Model)](#-architecture-overview-data-preservation-model)
4.  [📚 Table of Contents](#-table-of-contents)
5.  [🤖 AI Agent Directives (The Apex Protocol)](#-ai-agent-directives-the-apex-protocol)
6.  [📋 Development & Verification Standards](#-development--verification-standards)
7.  [⚖️ License](#-license)

---

## 🤖 AI Agent Directives (The Apex Protocol)

<details>
<summary>Click to view the mandatory directives for any AI agent interacting with this repository.</summary>

# 🎯 AGENTS.md: APEX DIRECTIVES (DATA ARCHIVE EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are an **Apex Data Integrity Auditor** operating under the authority of the Apex Technical Architect (chirag127). Your primary function is **READ-ONLY VALIDATION** and data retrieval. **NO WRITES, MODIFIES, OR DELETIONS ARE PERMITTED.**
**Philosophy:** *Fidelity Over Functionality.* Preserve the original state.

## 2. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)

*   **PRIMARY SCENARIO: DATA ARCHIVE / AUDIT (Static/Validation Focus)**
    *   **Stack:** This archive is treated as **immutable JSON/Text Manifests**. The validation pipeline uses Python 3.11+ orchestrated by **uv** for dependency isolation.
    *   **Validation Tools:** **Ruff** (for structural syntax checks on metadata files) and **Pytest** (for end-to-end data integrity comparison against known SHA hashes stored in `metadata/`).
    *   **Architecture:** **Immutable Data Ledger.** All processing must simulate read-only operations.

## 3. MANDATORY OPERATIONAL PROTOCOLS

1.  **IMUTABILITY LOCK:** Confirm that all operations target read-only file systems. If write access is detected, immediately halt and report a security anomaly.
2.  **METADATA CROSS-REFERENCE:** Before serving any data from `data/`, cross-reference the directory structure and file hashes against the `metadata/schema.json` to ensure data integrity since archival.
3.  **NO API CALLS:** Do not attempt to initiate external network calls (APIs, external services) unless strictly for badge verification or CI/CD pipeline maintenance.

## 4. VERIFICATION COMMANDS (Read-Only Integrity Check)

To confirm the environment is correctly configured for auditing:

bash
# 1. Clone Repository
git clone https://github.com/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository.git
cd Chromium-Ad-Detection-Filter-Archive-Data-Repository

# 2. Setup Environment (Using uv)
# Create and activate virtual environment
uv venv
source .venv/bin/activate

# Install necessary validation dependencies (e.g., pytest, ruff)
# Note: Actual dependencies will be in a generated requirements.txt or pyproject.toml
pip install pytest ruff

# 3. Run Data Integrity Validation (Simulated Pytest Execution)
pytest tests/validation_suite.py

# 4. Run Linter Check (Structural Check)
ruff check . --fix

# 5. Final State Confirmation
echo "AGENT MODE: READY FOR READ-ONLY AUDIT OF ARCHIVAL DATA."


</details>

---

## 📋 Development & Verification Standards

### Repository Initialization (For Auditors/Researchers)

This repository is static. Setup involves cloning and installing validation dependencies.

bash
# 1. Clone the repository
git clone https://github.com/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository.git
cd Chromium-Ad-Detection-Filter-Archive-Data-Repository

# 2. Setup Environment (Placeholder using standard Python tools)
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt # Assuming requirements.txt defines validation libraries


### Execution Scripts

| Script Name | Description | Command |
| :--- | :--- | :--- |
| `validate:data` | Runs Pytest suite to verify data hashes and structure. | `pytest tests/validation_suite.py` |
| `lint:static` | Runs Ruff linter across all metadata/configuration files. | `ruff check .` |
| `tree:view` | Displays the immutable file structure. | `tree -L 2` |

### Guiding Principles

1.  **DRY (Don't Repeat Yourself):** Metadata schemas must be centrally defined.
2.  **YAGNI (You Ain't Gonna Need It):** No executable code or processing logic is stored here; only data and verification scaffolding.
3.  **SOLID (Applicable to Validation Logic):** The validation layer must maintain clear separation between data source parsing and assertion logic.

---

## ⚖️ License

This project is preserved under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. Data reuse requires attribution and is prohibited for commercial purposes.

[![License](https://img.shields.io/github/license/chirag127/Chromium-Ad-Detection-Filter-Archive-Data-Repository?style=flat-square)](LICENSE)