---
client: Galana
solution: SAP GROW Public Cloud
module: SAP SD
document_type: KDS_KSD
repository_type: AI_RAG_Knowledge_Repository
process_name: Sales and Distribution Key Data Structure
company_or_entity: GALANA ENERGIES LIMITED(TANZANIA)
source_document: Nishati SD KDS.xls
---

# Nishati SD KDS - KDS/KSD Guide

## 1. Purpose

This document preserves the Sales and Distribution (SD) Key Data Structure values from the source KDS/KSD workbook in Markdown format for the Galana SAP GROW Public Cloud AI/RAG knowledge repository.

## 2. Business Context

The KDS defines the master and configuration reference values required for SAP SD execution, including customer account groups, pricing-related keys, tax indicators, account assignment groups, incoterms, shipping/loading conditions, customer groups, SD document number ranges, and output numbering. These values help future consultants understand how the Galana SD solution is structured and how business transactions are classified in SAP.

## 3. Process Scope

### In Scope

- SAP SD key data structures captured in the source workbook.
- Customer, pricing, tax, account assignment, shipping, loading, document number range, and output reference data where available.

### Out of Scope

- Step-by-step transactional execution is not contained in this KDS workbook unless explicitly shown in the source.
- Configuration rationale is not available unless explicitly stated in the source.

## 4. User Roles and Responsibilities

| Role | Responsibility |
| --- | --- |
| SAP SD Consultant | Uses this KDS to configure, validate, and support SD master/configuration values. |
| Business Process Owner | Reviews and approves business meaning of the KDS values. |
| Master Data Team | Uses relevant codes while creating or validating master data. |
| Support Consultant | Uses the values to troubleshoot SD document creation, pricing, tax, account assignment, and number range issues. |

## 5. Prerequisites

- Sales organization, distribution channel, division, and sales area structure should be finalized.
- Business partner/customer master design should be aligned with the customer account groups.
- Pricing, tax, account assignment, shipping, and document type design should be aligned with the BBP and BPML.
- Any value marked as blank or unclear should be treated as `Clarification Required` before configuration or migration.

## 6. SAP Fiori Apps / Transactions Used

| App / Transaction | Purpose | Used By |
| --- | --- | --- |
| Manage Business Partner / Maintain Customer | Customer master creation and maintenance using account groups and customer classification values. | Master Data Team / SD Consultant |
| Manage Sales Orders | Sales document creation using sales document types, pricing, tax, incoterms, shipping conditions, and customer groups. | Sales / Operations / SD Consultant |
| Manage Billing Documents | Billing document creation using billing type and number range references. | Billing / Finance / SD Consultant |
| Configuration Activities | Maintain SD configuration and SSCUI-based settings in SAP Public Cloud. | SAP SD Consultant |

## 7. End-to-End Process Overview

This KDS is a reference document, not a transaction procedure. It supports the end-to-end SD lifecycle by defining values used during customer master creation, sales order processing, delivery processing, billing, account determination, tax determination, pricing classification, and output/document numbering.

## 8. Step-by-Step Procedure

This source document does not provide transactional screen-by-screen steps. It provides configuration and master-data key structures. Therefore, the procedure for using this KDS is:

1. Identify the relevant SD process or entity.
2. Refer to the appropriate KDS section below.
3. Use the key/value/code during SAP configuration, master data creation, testing, or issue resolution.
4. Validate the selected value against BBP, BPML, and User Manual documents.
5. Mark any missing or unclear value as `Clarification Required` before production use.

## 9. Field-Level Explanation

| Field / Structure | Description | Mandatory? | Example Value | Business Impact |
| --- | --- | --- | --- | --- |
| Customer Account Group | Classifies customers and controls number range/master-data behavior. | Yes | See KDS tables below | Incorrect value may create customer under wrong category or number range. |
| Customer Price Procedure | Determines customer-side pricing procedure classification. | Yes, where pricing applies | See KDS tables below | Incorrect value may result in wrong pricing procedure determination. |
| Customer Price List | Classifies customer price list group. | As required | See KDS tables below | Incorrect value may result in wrong pricing/price list reporting. |
| Tax Indicator | Determines taxable or exempt classification. | Yes, where tax applies | See KDS tables below | Incorrect tax indicator may cause wrong VAT/tax treatment. |
| Account Assignment Group | Supports revenue/account determination. | Yes | See KDS tables below | Incorrect value may post revenue to wrong accounts. |
| Incoterm | Defines commercial delivery responsibility and freight/cost terms. | As required | CIF, FOB, DAP, etc. | Incorrect value may affect commercial obligations and documentation. |
| Shipping Condition | Defines shipping behavior/classification. | As required | Standard | Incorrect value may affect delivery/shipping processing. |
| Loading Group | Defines loading classification. | As required | Standard | Incorrect value may affect logistics/loading determination. |
| SD Document Number Range | Defines number ranges for SD documents. | Yes | See KDS tables below | Incorrect number range may break document sequencing/auditability. |

## 10. Business Rules

- Use the exact codes and descriptions from the KDS tables below.
- Do not reuse number ranges for unrelated document types unless approved.
- Tax indicators must reflect customer/material tax applicability.
- Account assignment groups must align with finance revenue/account determination design.
- Customer group and price list values must align with Galana's business segmentation.
- Missing or blank values require confirmation from the business or solution owner.

## 11. Approval Workflow

The source workbook does not contain a detailed workflow. Approval/sign-off details may exist in the original signed document version or related approval record. `Clarification Required` if approval dates/signatures are needed for this entity.

## 12. Exception Scenarios

| Scenario | Reason | System Behaviour | User Action | Resolution |
| --- | --- | --- | --- | --- |
| Incorrect customer account group selected | Wrong master data classification | Customer may receive incorrect number range or control fields | Stop creation/change request and validate KDS | Correct master data or create new customer under correct account group. |
| Wrong tax indicator used | Tax classification mismatch | Incorrect tax may be calculated | Validate customer/material tax setup | Correct tax indicator and retest sales/billing. |
| Wrong account assignment group used | Revenue/account posting mismatch | FI postings may go to incorrect account | Validate with Finance | Correct account assignment and repost if required. |
| Missing number range | Document type not mapped or not maintained | Document creation may fail | Check KDS and configuration | Maintain/confirm number range. |

## 13. Common Errors and Troubleshooting

| Error / Issue | Possible Cause | Resolution |
| --- | --- | --- |
| Sales order cannot be created | Missing or incorrect document type/number range | Check SD Document Number Range section. |
| Pricing not determined correctly | Wrong customer price procedure or price list | Validate Customer Price Procedure and Customer Price List sections. |
| Tax calculated incorrectly | Wrong customer/material tax indicator | Validate Tax Indicator section. |
| Revenue posting issue | Wrong account assignment group | Validate Account Assignment Group section with Finance. |

## 14. Output Documents

Output/document references are listed in the SD Document Number Range and Outputs sections where available. They may include Proforma Invoice, Standard Order, Delivery, Billing, Credit Memo, Debit Memo, Returns, and related SD documents.

## 15. Integration Touchpoints

- FI integration through account assignment and revenue posting.
- MM/inventory integration through delivery, goods movement, and loading-related structures.
- Tax/compliance integration through tax indicators.
- Output/document control through SD document and output number ranges.

## 16. Reports and Monitoring

- Monitor customer master data completeness and classification.
- Monitor SD document number range utilization.
- Validate billing and accounting postings by account assignment group.
- Review tax reporting by tax indicator.

## 17. FAQs

**Q: Is this a user manual?**  
A: No. This is a KDS/KSD reference document for SD key data structures.

**Q: Can these codes be changed directly?**  
A: No. Changes should be controlled through configuration governance and business approval.

**Q: What should I do if a required value is blank?**  
A: Mark it as `Clarification Required` and confirm with the process owner or SD lead.

## 18. Related Documents

- Galana SAP SD BBP
- Relevant BPML for the process using these values
- Relevant User Manual
- Configuration workbook or SSCUI configuration record
- Master data templates

## 19. Glossary

| Term | Meaning |
| --- | --- |
| KDS/KSD | Key Data Structure / Knowledge Sharing Document, depending on project terminology. |
| SD | Sales and Distribution. |
| VAT | Value Added Tax. |
| Incoterm | International commercial term defining buyer/seller responsibility. |
| Number Range | Defined sequence used by SAP to assign document numbers. |
| Account Assignment Group | SAP classification used in account determination. |

## 20. RAG Notes

- This document contains SAP SD KDS values for `GALANA ENERGIES LIMITED(TANZANIA)`.
- Search terms: SD KDS, customer account group, number range, customer price procedure, customer price list, tax indicator, account assignment group, incoterm, shipping condition, loading group, SD document number range, outputs.

# Source KDS Tables


## Sheet: Index

| Column 1 | Column 2 | Column 3 | Column 4 |
| --- | --- | --- | --- |
| KDS Elements | Sr. No. | Description | Status |
| Organisatonal Structure | 1.1 | Sales Organizaton | Already shared |
|  | 1.2 | Distribution Channel | Already shared |
|  | 1.3 | Division | Already shared |
|  | 1.4 | Sales Area | Already shared |
|  | 1.5 | Sales Office | Already shared |
|  | 1.6 | Sales Group | Already shared |
|  | 1.7 | Shipping Point | Already shared |
| Customer Master data Keys | 2.1 | Customer Group & Number Range |  |
|  | 2.2 | Customer Price Procedure Key |  |
|  | 2.3 | Customer Price List |  |
|  | 2.4 | Account Assignment Group Customer |  |
|  | 2.5 | Incoterm |  |
|  | 2.6 | Shipping Condition |  |
|  | 2.7 | Customer Group |  |
|  | 2.8 | Tax indicator customer |  |
| Material Master Keys | 3.1 | Tax indicator material |  |
|  | 3.2 | Account assignment group Material |  |
|  | 3.3 | Loading Group |  |
| O2C Solution process keys | 4.1 | SD Document Number |  |


## Sheet: Customer Group & Number range

| Column 1 | Column 2 | Column 3 | Column 4 |
| --- | --- | --- | --- |
| GALANA ENERGIES LIMITED(TANZANIA) |  |  |  |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |  |  |
| Customer Account Groups & Number Range |  |  |  |
| Customer Account Group |  | Range (10 digit) |  |
| Code | Main Category | From | To |
| ZRET | Retail | 1100000000 | 1199999999 |
| ZCOM | Commercial | 1200000000 | 1299999999 |
| ZTRE | Transit and Export | 1300000000 | 1399999999 |
| ZTRD | Trading | 1400000000 | 1499999999 |
| ZLPG | LPG | 1500000000 | 1599999999 |
| ZLUB | Lubricants | 1600000000 | 1699999999 |
| ZAVI | Aviation | 1700000000 | 1799999999 |
| ZSTF | Internal Customer | 1800000000 | 1899999999 |
| ZPLT | Plant | External |  |


## Sheet: Customer Price Procedure

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Customer Price Procedure |  |
| Customer Price Procedure Key | Description |
| 1 | Local Fuels |
| 2 | Aviation |
| 3 | Lubricants |
| 4 | LPG |
| 5 | Transit/Export |
| 6 | Trading |
| 7 | STO |


## Sheet: Customer price List

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Customer Price List |  |
| Customer Price list key | Description |
| 1 | Local Fuels |
| 2 | Aviation |
| 3 | Lubricants |
| 4 | LPG |
| 5 | Transit/Export |
| 6 | Trading |
| 7 | STO |


## Sheet: Tax Indicator

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Tax Indicator |  |
| Customer |  |
| Tax Indicator | Description |
| 1 | Exempted |
| 2 | Taxable |
| Material |  |
| Tax Indicator | Description |
| 1 | Exempted |
| 2 | 18% -Taxable |
| 3 | 0% -Taxable |
| Tax Rate | Tax Code Description |
| 0.18 | VAT 18% |
| 0 | ZERO RATED 0% |
|  | EXEMPT VAT |
| 0.18 | VAT 18% |
| 0 | ZERO RATED 0% |
|  | EXEMPT VAT |


## Sheet: Account assignment Group

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Account Assignment Group |  |
| Customer |  |
| A/C Assignment Grp | Description |
| 10 | Local |
| 20 | Transit |
| 30 | Trading |
| 40 | Related Company |
| 50 | Subsidiaries |
| Material |  |
| A/C Assignment Grp | Description |
| 10 | White Fuels |
| 20 | Black Fuels |
| 30 | Lubricants |
| 40 | Bottled LPG & Accessories |
| 50 | Bulk LPG |
| 60 | Auto-Gas |
| 70 | Aviation |
| 80 | Non-trading Goods |


## Sheet: Incoterm

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Incoterm |  |
| Customer |  |
| Incoterm | Description |
| CIF | Cost Insurance Freight |
| FOB | Free on Board |
| DAP | Delivered at Place |
| C&F | Cost & Freight |
| DDU | Delivered Duty Unpaid |
| DDP | Delivered Duty Paid |


## Sheet: Shipping Condition

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Shipping Condition |  |
| Shp. Cond. | Description |
| 01 | Standard |


## Sheet: Customer Group

| Column 1 | Column 2 | Column 3 | Column 4 | Column 5 | Column 6 | Column 7 | Column 8 | Column 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |  |  |  |  |  |  |  |
| Customer Groups |  |  |  |  |  |  |  |  |
| Customer Group | Description | Customer Group 1 | Description |  |  | Customer Group Key | Customer Price Group Code | Customer Price Group |
| 10 | Financial Dealer |  |  |  |  |  |  |  |
|  |  |  |  |  |  | 10,11,12,13 | OC | Off court |
| 11 | Non-Financial Dealer |  |  |  |  |  | BK | Bulk |
|  |  |  |  |  |  |  | UC | Under Canopy |
| 12 | Dealer Owned Dealer Operated |  |  |  |  |  |  |  |
| 13 | Delnet |  |  |  |  |  |  |  |
| 14 | Fuel Card | PRE | Prepaid |  |  |  |  |  |
|  |  | PST | Postpaid |  |  |  |  |  |
| 15 | Retail LPG | RG1 | Retail Distributor |  |  |  |  |  |
|  |  | RG2 | Retail Bulk |  |  |  |  |  |
| 16 | Retail Lubricants |  |  |  |  |  |  |  |
| 17 | Consumer |  |  |  |  |  |  |  |
| 18 | Contractor |  |  |  |  |  |  |  |
| 19 | Independent Stations |  |  |  |  |  |  |  |
| 20 | Commercial Consumer | LB1 | Transport |  |  |  |  |  |
|  |  | LB2 | Manufacuring |  |  |  |  |  |
|  |  | LB3 | Agriculture |  |  |  |  |  |
|  |  | LB4 | Construction |  |  |  |  |  |
|  |  | LB5 | Engineering Services |  |  |  |  |  |
|  |  | LB6 | Mining |  |  |  |  |  |
|  |  | LB7 | Government Institutions |  |  |  |  |  |
|  |  | LB8 | Private Instutions |  |  |  |  |  |
| 21 | Tender |  |  |  |  |  |  |  |
| 22 | Marine |  |  |  |  |  |  |  |
| 23 | Autocentres |  |  |  |  |  |  |  |
| 24 | 2W/3W |  |  |  |  |  |  |  |
| 25 | Network Lubes |  |  |  |  |  |  |  |
| 30 | Tourism & Hospitality |  |  |  |  |  |  |  |
| 31 | Health Institutions |  |  |  |  |  |  |  |
| 32 | Learning Institutions |  |  |  |  |  |  |  |
| 33 | Wholesale & Retail |  |  |  |  |  |  |  |
| 34 | Manufacturing |  |  |  |  |  |  |  |
| 35 | Real Estate & Construction |  |  |  |  |  |  |  |
| 36 | Others |  |  |  |  |  |  |  |
| 37 | Network LPG |  |  |  |  |  |  |  |
| 40 | Internal Customer |  |  |  |  |  |  |  |
| 51 | Trading Tanzania |  |  |  |  |  |  |  |
| 63 | Transit Rwanda |  |  |  |  |  |  |  |
| 70 | Aviation |  |  |  |  |  |  |  |


## Sheet: Loading Group

| Column 1 | Column 2 |
| --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |
| Loading Group |  |
| Loading Group | Description |
| 0001 | Standard |


## Sheet: SD Document Number Range

| Column 1 | Column 2 | Column 3 | Column 4 |
| --- | --- | --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |  |  |
| SD Document Number Range |  |  |  |
| Sales Document Type | Description | Number Range From | Number range to |
| IN | Inquiry | 2100000000 | 2199999999 |
| QT | Quotation | 2200000000 | 2299999999 |
| CBAR | Standard Return | 2300000000 | 2399999999 |
| CBFD | Deliv.Free of Charge | 2400000000 | 2499999999 |
| CBG0 | Return Pack./Empties | 2500000000 | 2599999999 |
| CCFU | Consignment Fill-Up | 2600000000 | 2699999999 |
| CCIS | Consignment Issue | 2700000000 | 2799999999 |
| CCLN | Ret. Packaging Issue | 2800000000 | 2899999999 |
| CCPU | Consignment Pick-Up | 2900000000 | 2999999999 |
| CCRE | Consignment Return | 3000000000 | 3099999999 |
| CR | Credit Memo Request | 3100000000 | 3199999999 |
| CQ | Quantity Contract | 3200000000 | 3299999999 |
| DR | Debit Memo Request | 3300000000 | 3399999999 |
| RK | Invoice Correct. Req | 3400000000 | 3499999999 |
| SD2 | Replcmnt Deliv. Ord. | 3500000000 | 3599999999 |
| OR | Standard Order | 7000000000 | 8999999999 |
| VC01 | Value Contract | 3600000000 | 3699999999 |
| CBRE | Lean Return | 3700000000 | 3799999999 |
| Delivery Document Type | Description | Number Range From | Number range to |
| CCLF | Consi/Ret.Issue Dely | 3800000000 | 3899999999 |
| CCLR | ConsiReturn Delivery | 3900000000 | 3999999999 |
| LF | Outbound Delivery | 4000000000 | 4099999999 |
| LO | Delivery w/o Ref. | 4100000000 | 4199999999 |
| LR | Lean Returns Dlv. | 4200000000 | 4299999999 |
| LR2 | Std Returns Delivery | 4300000000 | 4399999999 |
| NL | Replenishment Dlv. | 4400000000 | 4499999999 |
| Billing Type | Description | Number Range From | Number range to |
| CBRE | Credit Memo for Returns | 4500000000 | 4599999999 |
| F2 | Invoice | 4600000000 | 4699999999 |
| F5 | Pro Forma for Order | 4700000000 | 4799999999 |
| F8 | Pro Forma Invoice for Delivery | 4800000000 | 4899999999 |
| FAS | Down Payment Request Cancellation | 4900000000 | 4999999999 |
| FAZ | Down Payment Request | 5000000000 | 5099999999 |
| G2 | Credit Memo | 5100000000 | 5199999999 |
| L2 | Debit Memo | 5200000000 | 5299999999 |
| S1 | Invoice Cancellation | 5300000000 | 5399999999 |
| S2 | Credit Memo Cancellation | 5400000000 | 5499999999 |


## Sheet: Outputs

| Column 1 | Column 2 | Column 3 | Column 4 | Column 5 |
| --- | --- | --- | --- | --- |
| SALES & DISTRIBUTION - KEY DATA STRUCTURE |  |  |  |  |
| Outputs |  |  |  |  |
| Sales Document Type | Description | No. Range Int. Asst | Number range from | Number range to |
| PFI | Proforma Invoice | 05 | 200000000 | 299999999 |
| OR | Standard Order | 01 | 360000000 | 369999999 |
| BF | Standard Order-Black Fuels |  | 370000000 | 379999999 |
| TR | Standard Order-Transit |  | 380000000 | 389999999 |
| LUB | Standard Order-Lubricants |  | 410000000 | 419999999 |
| BG | Standard Order-Bulk LPG |  | 150000000 | 159999999 |
| LPG | Standard Order-LPG |  | 140000000 | 149999999 |
| CIWF | Local Commercial Invoice-White Fuels | 01 | 00000001 | 49999999 |
| CIBF | Local Commercial Invoice-Black Fuels |  |  |  |
| TCI | Transit Commercial Invoice |  |  |  |
| CILB | Local Commercial Invoice-Lubricants |  |  |  |
| CIBG | Local Commercial Invoice-Bulk LPG |  |  |  |
| CIG | Local Commercial Invoice-LPG |  |  |  |
| RMA | Return order |  |  |  |
| CN | Local Credit Memo | 13 | 60000000 | 64999999 |
| TCN | Transit Credit Memo |  |  |  |
| DN | Local Debit Memo |  |  |  |
| TCN | Transit Credit Memo |  |  |  |
| LDN | Local Delivery Note-White Fuels | 01 | 00000001 | 49999999 |
| BDN | Local Delivery Note-Black Fuels |  |  |  |
|  | Transit Delivery Note |  |  |  |
|  | Lubricants Delivery Note |  |  |  |
|  | Bulk LPG Local Delivery Note |  |  |  |
|  | LPG Delivery Note |  |  |  |
|  | White Fuels Gate Pass | 01 | 00000001 | 49999999 |
|  | Black Fuels Gate Pass |  |  |  |
|  | Transit Gate Pass |  |  |  |
|  | Lubricants Gate Pass |  |  |  |
|  | Bulk LPG Gate Pass |  |  |  |
|  | LPG Empty Cylinder Gate Pass |  |  |  |
|  | LPG Empty Faulty Cylinder Gate Pass |  |  |  |
|  | LPG Bottled Gas Gate Pass |  |  |  |
|  | Stock Transfer Order |  |  |  |


# Quality Check

- No non-empty worksheet was intentionally omitted.
- All available worksheet rows with visible values were converted into Markdown tables.
- Blank values are preserved as blank cells and should be reviewed as `Clarification Required` when business-critical.
