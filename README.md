# CMMC GCP Automation — Evidence Collection Portfolio

A cybersecurity portfolio project exploring how Google Cloud configuration data can support **CMMC evidence collection and control reviews**.

> **Scope:** This repository contains access-control mappings, export scripts, and guidance. The scripts were not executed or validated against a live cloud environment during this documentation review. This project is not a certification or formal CMMC assessment.

## Problem and approach

Compliance teams must collect technical evidence consistently. These example scripts illustrate how an analyst might export IAM, logging, firewall, and VPC information before evaluating it against security requirements.

```text
Google Cloud settings → Export scripts → Evidence files → Analyst control review → Findings
```

Exporting configuration information **does not automatically prove** that a control is effective.

## What's in the repository?

| Folder or file | Purpose |
| --- | --- |
| [Level 1 mapping](Level1/control_mapping_AC_L1.csv) | Access-control mapping for Level 1 |
| [Level 1 evidence scripts](Level1/evidence_scripts) | IAM, firewall, audit log, and project configuration exports |
| [Level 2 mapping](Level2/control_mapping_AC_L2.csv) | Access-control mapping for Level 2 |
| [Level 2 evidence scripts](Level2/evidence_scripts) | Service account, logging sink, and VPC inspection |
| [Framework overview](docs/framework_overview.md) | Background and control context |
| [Evidence packaging standards](docs/evidence_packaging_standards.md) | Guidance for organizing evidence |

## How to explore it

1. Read the framework overview.
2. Compare the two control-mapping CSV files.
3. Open the scripts and note which Google Cloud settings each script inspects.
4. Before running a script, inspect its permissions, required tools, output files, and sensitive-data handling.
5. Test only in an authorized cloud environment. Never publish real audit evidence or credentials.

## What this demonstrates

Python and shell scripting · cloud IAM and networking concepts · evidence collection design · control mapping · audit-readiness documentation.

## Important limitations

- The mappings focus on access-control examples; this is **not full CMMC coverage**.
- Human review, system scoping, policy evidence, and assessment judgment remain essential.
- Additional deployment, validation, security testing, and operational controls are required for production use.

## License

See [LICENSE](LICENSE).
