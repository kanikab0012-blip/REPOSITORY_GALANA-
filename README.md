# Galana SAP SD KDS Markdown Conversion

This folder contains AI/RAG-ready Markdown conversions of the uploaded SAP SD KDS/KSD source documents.

## Files

| Markdown File | Source Document |
| --- | --- |
| SD_KDS_DELNET_-_FINAL.md | SD KDS DELNET - FINAL .xls |
| SD_KDS_-_ZE.md | SD KDS - ZE.xls |
| GEUL_SD_KDS.md | GEUL SD KDS.xls |
| Nishati_SD_KDS.md | Nishati SD KDS.xls |
| GERL_SD_KDS.md | GERL SD KDS.xls |
| DEKE_SD_KDS.md | DEKE SD KDS.pdf |

## Usage

Place these files inside the Galana repository under a KDS/KSD or Master Data / Configuration reference folder, for example:

```text
GALANA_SAP_GROW_SD_REPOSITORY/
└── 03_Master_Data_and_KDS/
    ├── SD_KDS_DELNET_-_FINAL.md
    ├── SD_KDS_-_ZE.md
    ├── GEUL_SD_KDS.md
    ├── Nishati_SD_KDS.md
    ├── GERL_SD_KDS.md
    └── DEKE_SD_KDS.md
```

## Notes

- Spreadsheet-based KDS files were converted from workbook sheets into Markdown tables.
- The scanned PDF was converted based on visible page images; unclear handwritten/scanned values are marked as `Clarification Required`.
