# SQL Security Analysis

![GitHub Actions Status](https://img.shields.io/github/actions/workflow/status/martinzambonino/sql-security-analysis/ci.yml?branch=main)
![License](https://img.shields.io/github/license/martinzambonino/sql-security-analysis)

## What It Does

A project focused on leveraging SQL for cybersecurity-oriented data analysis in controlled, educational environments:

- **Anomaly Detection:** SQL queries to identify unusual access patterns, login failures, and privilege escalation attempts in synthetic audit logs.
- **Access Auditing:** Role-based access control (RBAC) analysis and permission gap identification.
- **Log Forensics:** Structured query techniques for parsing and correlating security events across synthetic datasets.
- **Database Hardening Checks:** Queries to audit database configurations against CIS Benchmark recommendations.

## Skills Demonstrated

| Skill | Details |
|---|---|
| SQL (Advanced) | CTEs, window functions, subqueries, aggregation |
| Data Forensics | Event correlation, timeline reconstruction |
| Database Security | RBAC auditing, CIS Benchmarks, hardening |
| Python (Auxiliary) | Data generation with Faker, analysis automation |

## How to Run

```bash
# Clone the repository
git clone https://github.com/martinzambonino/sql-security-analysis.git
cd sql-security-analysis

# Option A: Use SQLite with synthetic data
sqlite3 data/synthetic_audit.db < src/create_schema.sql
sqlite3 data/synthetic_audit.db < src/anomaly_detection.sql

# Option B: Use Python to generate synthetic data first
python -m venv venv
source venv/bin/activate  # Linux/macOS
pip install -r requirements.txt
python src/generate_synthetic_data.py
```

## Methodology

- **CIS Benchmarks:** Database configuration auditing against industry standards.
- **NIST SP 800-92:** Guide to Computer Security Log Management.
- **MITRE ATT&CK:** Mapping detected anomalies to known attack techniques.

## Limitations

- All datasets are **100% synthetic** — generated algorithmically using Faker.
- SQL queries are optimized for readability and educational value, not production performance.
- Database hardening checks cover SQLite and PostgreSQL configurations only.

## ⚖️ Ethical & Legal Disclaimer

> [!WARNING]
> **This repository is strictly for academic and educational purposes.**
> The SQL queries and analysis techniques must **not** be executed against production databases or systems without explicit, written authorization.
> The author assumes no liability for misuse.

### 🇪🇨 Compliance Note (Ecuador — LOPDP/SPDP)

This project adheres to Privacy by Design and Default principles.
**No real personal data is used, stored, or processed.** All datasets are purely synthetic (generated via `Faker`) or officially public academic datasets. This is compliant with the *Ley Orgánica de Protección de Datos Personales (LOPDP)* and auditable by the *Superintendencia de Protección de Datos Personales (SPDP)*.
