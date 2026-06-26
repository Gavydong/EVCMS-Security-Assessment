# EVCMS-Security-Assessment

This repository provides supplementary materials for our publication on global EVCMS security assessment in IEEE Transactions on Network and Service Management (TNSM).

## Repository Contents

### LLM Prompts for Banner Analysis (Section III-B)

We use GPT-4o for all LLM-based classification steps. The following prompts correspond to the three-phase banner analysis pipeline described in Section III-B:

| File | Description | Status |
|------|-------------|--------|
| `ev_charging_classifier.txt` | Phase 2: Determines whether a management system banner is EV-charging-related | ✅ Available (vendor list redacted) |
| `management_system_classifier.txt` | Phase 1: Determines whether a banner represents a management system | ✅ Available |
| `vendor_extractor_validator.txt` | Phase 3: Extracts vendor names from confirmed EVCMS banners | ❌ Removed |

### Keyword Expansion (Section III-B-4)

| File | Description | Status |
|------|-------------|--------|
| `EVCMS_keywords.txt` | Discovered EVCMS-related keywords | ❌ Removed |
| Keyword expansion prompt | LLM prompt for generating new search keywords from vendor information | ❌ Removed |

### Datasets

| File | Description | Status |
|------|-------------|--------|
| `EVCMS_architecture.csv` | Deployment properties of discovered vendors (IP counts, categories) | ✅ Available (vendor names anonymized) |
| `EVCMS_vulnearbility.csv` | Vulnerability assessment results per vendor | ✅ Available (vendor names anonymized) |

> **Note:** The dataset with IP addresses is not uploaded due to ethical concerns. The datasets contain vendors collected after manuscript submission, so counts may exceed those reported in the paper.

## Removed Files — Ethical Disclosure Notice

The following files have been removed from this repository for responsible disclosure purposes:

- **`vendor_extractor_validator.txt`** (vendor name extraction prompt)
- **`EVCMS_keywords.txt`** (discovered keyword list)
- **Keyword expansion prompt**

These materials contain vendor-specific identifiers, product names, and search keywords that could be used to directly locate Internet-exposed EVCMS web portals with known vulnerabilities described in our paper. Releasing them would undermine the vendor anonymization applied throughout the manuscript and could facilitate exploitation of systems that remain unpatched.

The vendor list in `ev_charging_classifier.txt` has been redacted for the same reason, with the prompt structure preserved for methodological transparency.


## Contact

For questions regarding this work, please contact: [d_jiawe@live.concordia.ca](mailto:d_jiawe@live.concordia.ca)
