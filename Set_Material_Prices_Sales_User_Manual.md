---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: Set Material Prices – Sales
source_document: Set_Material_Prices_and_Discount_Manual_Galana.docx
---

# Set Material Prices – Sales

## Objective
Guide users on creating, managing, and maintaining material pricing and customer discounts using the Set Material Prices – Sales application.

## Overview
- ZPR0: Base Material Price
- ZDCM: Customer-Specific Discount

## Navigation
SAP Fiori Launchpad → Sales Pricing → Set Material Prices – Sales

## Create Material Price (ZPR0)

### Launch App
- Open Set Material Prices – Sales
- Select Change Condition Records
- Enter Condition Type: ZPR0

### Selection Criteria

| Field | Value |
|---|---|
| Sales Organization | GEKE |
| Plant | KLE1 |
| Distribution Channel | 10 |
| Material | WF-1001 |
| Valid On | 10.11.2025 |

### Maintain Price

| Field | Value |
|---|---|
| Amount | 100.00 KES per M3 |
| Valid From | 10.11.2025 |
| Valid To | 30.11.2025 |

### Save
Click Save to create the ZPR0 condition record.

## Create Material Discount (ZDCM)

### Launch App
Enter Condition Type: ZDCM

### Discount Details

| Field | Value |
|---|---|
| Sales Organization | GEKE |
| Distribution Channel | 10 |
| Customer | 1100000000 (GE Athi River) |
| Material | WF-1001 |
| Amount | 5.00- KES per M3 |
| Valid From | 10.11.2025 |
| Valid To | 31.12.9999 |

### Save
Click Save to create the discount condition record.

## Edit Existing Records
Use Change Condition Records and search by:
- Condition Type
- Material
- Customer
- Validity Dates

## Verification Reports
- Display Price Conditions (F1873)
- Manage Prices – Sales (F3363)

## Verification Checklist
- No overlapping validity dates
- Correct customer and material assignment
- Correct Sales Organization and Distribution Channel
- Currency = KES
- UoM = M3

## Summary

| Activity | Condition Type | Purpose |
|---|---|---|
| Create Material Price | ZPR0 | Maintain base price |
| Create Material Discount | ZDCM | Maintain customer discount |
| Update Pricing | ZPR0/ZDCM | Modify validity and value |
