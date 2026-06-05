---
client: Galana
solution: SAP GROW Public Cloud
module: SAP SD
document_type: KDS_KSD
repository_type: AI_RAG_Knowledge_Repository
process_name: Sales and Distribution Key Data Structure
company_or_entity: Delnet Services Limited (KE)
source_document: DEKE SD KDS.pdf
---

# DEKE SD KDS - KDS/KSD Guide

## 1. Purpose

This document preserves the Sales and Distribution (SD) Key Data Structure values from the signed PDF source document in Markdown format for the Galana SAP GROW Public Cloud AI/RAG knowledge repository.

## 2. Business Context

The KDS defines the SAP SD reference values required for customer master classification, pricing classification, tax determination, account assignment, incoterms, shipping/loading control, customer grouping, SD document number ranges, delivery number ranges, and billing number ranges.

## 3. Process Scope

### In Scope

- SD KDS values visible in the signed PDF.
- Customer account groups and number ranges.
- Customer price procedure and price list keys.
- Tax indicators.
- Account assignment groups.
- Incoterms.
- Shipping condition.
- Customer groups.
- Loading group.
- SD document, delivery document, and billing document number ranges.

### Out of Scope

- Transactional step-by-step user execution.
- Detailed SAP configuration rationale unless visible in the source PDF.
- Any value not visible in the scanned PDF pages.

## 4. User Roles and Responsibilities

| Role | Responsibility |
| --- | --- |
| SAP SD Consultant | Uses this KDS to configure, validate, and support SD master/configuration values. |
| Business Process Owner | Reviews and approves business meaning of the KDS values. |
| Master Data Team | Uses relevant codes while creating or validating master data. |
| Support Consultant | Uses the values to troubleshoot SD document creation, pricing, tax, account assignment, and number range issues. |

## 5. Prerequisites

- Sales organization, distribution channel, division, and sales area structure should be finalized.
- Customer master design should be aligned with customer account groups.
- Pricing, tax, account assignment, shipping, and document number range settings should be aligned with the BBP and BPML.
- Any unclear value must be treated as `Clarification Required`.

## 6. SAP Fiori Apps / Transactions Used

| App / Transaction | Purpose | Used By |
| --- | --- | --- |
| Manage Business Partner / Maintain Customer | Customer master creation and maintenance using account groups and customer classification values. | Master Data Team / SD Consultant |
| Manage Sales Orders | Sales document creation using sales document types, pricing, tax, incoterms, shipping conditions, and customer groups. | Sales / Operations / SD Consultant |
| Manage Billing Documents | Billing document creation using billing type and number range references. | Billing / Finance / SD Consultant |
| Configuration Activities | Maintain SD configuration and SSCUI-based settings in SAP Public Cloud. | SAP SD Consultant |

## 7. End-to-End Process Overview

This KDS is a configuration/master-data reference document, not a transaction procedure. It supports SD execution by defining values used during customer master creation, sales order processing, delivery processing, billing, tax handling, account determination, and document numbering.

## 8. Step-by-Step Procedure

This source document does not provide transactional screen-by-screen steps. It provides key SD data structures. Use it as follows:

1. Identify the SD process or master data object.
2. Refer to the relevant KDS section.
3. Use the exact code/value from the table.
4. Validate the value against BBP, BPML, configuration, and master data templates.
5. Treat unclear scanned values as `Clarification Required`.

## 9. Field-Level Explanation

| Field / Structure | Description | Mandatory? | Example Value | Business Impact |
| --- | --- | --- | --- | --- |
| Customer Account Group | Classifies customers and controls number range/master data behavior. | Yes | ZDCR, ZDCM | Wrong value may create customer under incorrect category or number range. |
| Customer Price Procedure | Customer-side pricing procedure classification. | Yes, where pricing applies | 1, 2, 3 | Wrong value may impact pricing determination. |
| Customer Price List | Customer price list classification. | As required | 1, 2, 3 | Wrong value may impact pricing or reporting. |
| Tax Indicator | Customer/material tax applicability. | Yes, where tax applies | 1, 2, 3 | Wrong value may create incorrect VAT/tax treatment. |
| Account Assignment Group | Revenue/account determination classification. | Yes | 10, 20, 30 | Wrong value may post revenue to wrong accounts. |
| Incoterm | Commercial delivery responsibility and freight/cost terms. | As required | CIF, FOB, DAP | Wrong value may impact commercial obligations and documentation. |
| Shipping Condition | Shipping behavior/classification. | As required | 01 | Wrong value may affect delivery/shipping processing. |
| Loading Group | Loading classification. | As required | 0001 | Wrong value may affect logistics/loading determination. |
| SD Document Number Range | Document number interval for sales, delivery, and billing documents. | Yes | 2100000000-2199999999 | Wrong range may break document sequencing/auditability. |

## 10. Business Rules

- Use exact codes and number ranges from the KDS.
- Do not change or reuse number ranges without approval.
- Tax indicators must reflect customer/material tax treatment.
- Account assignment groups must align with Finance account determination.
- Customer groups and price lists must align with business segmentation.
- Scanned or unclear values must be confirmed before production use.

## 11. Approval Workflow

## Sign-Off and Approval Details

| Category | Name | Approval Date | Signature |
| --- | --- | --- | --- |
| Process Champion | Patrick Wainaina | 17/09/2025 | Signed |
| Process Champion | Caroline Muthee | 22/09/2026 or 22/09/2025 - Clarification Required | Signed |
| Project Management Team | Anne Njoki | 19/01/2025 | Signed |
| Project Management Team | Faith Muthoni | 19/01/2025 | Signed |
| Project Management Team | James Mwangi | 19/09/2025 | Signed |
| Chief Financial Officer | Name not visible | Clarification Required | Signed |

## 12. Exception Scenarios

| Scenario | Reason | System Behaviour | User Action | Resolution |
| --- | --- | --- | --- | --- |
| Incorrect customer account group selected | Wrong master data classification | Customer may receive incorrect number range or control fields | Stop creation/change request and validate KDS | Correct master data or create a new customer under correct account group. |
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

Output/document references are listed under SD Document Number Range and Billing Document Type sections. They include Inquiry, Quotation, Standard Order, Return, Delivery, Billing, Credit Memo, Debit Memo, Proforma Invoice, and related SD documents.

## 15. Integration Touchpoints

- FI integration through account assignment and billing.
- MM/inventory integration through delivery, returns, and stock movements.
- Tax/compliance integration through tax indicators.
- Output/document control through number ranges.

## 16. Reports and Monitoring

- Customer master classification review.
- SD document number range monitoring.
- Billing/accounting posting validation.
- Tax report validation.

## 17. FAQs

**Q: Is this a transactional user manual?**  
A: No. This is a KDS reference for SAP SD key data structures.

**Q: Can these values be changed directly?**  
A: No. Changes should go through approval and configuration governance.

**Q: What should be done if a value is unclear because the PDF is scanned?**  
A: Mark it as `Clarification Required` and confirm with the process owner or SAP SD lead.

## 18. Related Documents

- Galana SAP SD BBP
- Relevant BPML documents
- Relevant User Manuals
- Configuration workbook/SSCUI records
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

- This document contains SAP SD KDS values for Delnet Services Limited (KE).
- Search terms: DEKE SD KDS, Delnet Services, customer account group, number range, price procedure, price list, tax indicator, account assignment group, incoterm, shipping condition, loading group, SD document number range, billing document type.

# Source KDS Tables

## Customer Account Groups and Number Range

| Code | Main Category | Number Range From | Number Range To |
| --- | --- | --- | --- |
| ZDCR | Retail | 1100000000 | 1199999999 |
| ZDCM | Commercial | 1200000000 | 1299999999 |
| ZDAV | Aviation | 1700000000 | 1799999999 |
| ZDSF | Internal Customer | 1800000000 | 1899999999 |
| ZDPT | Plant | External | Clarification Required |

## Customer Price Procedure

| Customer Price Procedure Key | Description |
| --- | --- |
| 1 | Local Fuels |
| 2 | Aviation |
| 3 | Lubricants |
| 4 | LPG |
| 7 | STO |

## Customer Price List

| Customer Price List Key | Description |
| --- | --- |
| 1 | Local Fuels |
| 2 | Aviation |
| 3 | Lubricants |
| 4 | LPG |
| 7 | STO |

## Tax Indicator

### Customer

| Tax Indicator | Description |
| --- | --- |
| 1 | Exempted |
| 2 | Taxable |

### Material

| Tax Indicator | Description |
| --- | --- |
| 1 | Exempted |
| 2 | 16% - Taxable |
| 3 | 0% - Taxable |

### Tax Code Description

| Tax Rate | Tax Code Description |
| --- | --- |
| 16% | VAT 16% |
| 0% | ZERO RATED 0% |
| Clarification Required | EXEMPT VAT |

## Account Assignment Group

### Customer

| A/C Assignment Group | Description |
| --- | --- |
| 10 | Local |
| 40 | Related Company |

### Material

| A/C Assignment Group | Description |
| --- | --- |
| 10 | White Fuels |
| 20 | Black Fuels |
| 30 | Lubricants |
| 40 | Bottled LPG |
| 50 | Bulk LPG |
| 60 | Auto-Gas |
| 70 | Aviation |
| 80 | Non-trading Goods |

## Incoterm

| Incoterm | Description |
| --- | --- |
| CIF | Cost Insurance Freight |
| FOB | Free on Board |
| DAP | Delivered at Place |
| C&F | Cost & Freight |
| DDU | Delivered Duty Unpaid |
| DDP | Delivered Duty Paid |

## Shipping Condition

| Shipping Condition | Description |
| --- | --- |
| 01 | Standard |

## Customer Groups

| Customer Group | Description |
| --- | --- |
| 10 | Station |
| 14 | Fuel Card |
| 40 | Commercial Consumer |
| 41 | Trader |
| 60 | Internal Customer |
| 80 | Aviation |

## Customer Group 1

| Customer Group 1 | Description |
| --- | --- |
| PRE | Prepaid |
| PST | Postpaid |

## Loading Group

| Loading Group | Description |
| --- | --- |
| 0001 | Standard |

## SD Document Number Range

### Sales Document Type

| Sales Document Type | Description | Number Range From | Number Range To |
| --- | --- | --- | --- |
| IN | Inquiry | 2100000000 | 2199999999 |
| QT | Quotation | 2200000000 | 2299999999 |
| CBAR | Standard Return | 2300000000 | 2399999999 |
| CBFD | Deliv. Free of Charge | 2400000000 | 2499999999 |
| CBLQ | Returns Order | 2500000000 | 2599999999 |
| CCFU | Consignment Fill-Up | 2600000000 | 2699999999 |
| CCIS | Consignment Issue | 2700000000 | 2799999999 |
| CCLN | Ret. Packaging Issue | 2800000000 | 2899999999 |
| CCPI | Consignment Pick-Up | 2900000000 | 2999999999 |
| CCRE | Consignment Return | 3000000000 | 3099999999 |
| CR | Credit Memo Request | 3100000000 | 3199999999 |
| CQM | Quantity Contract | 3200000000 | 3299999999 |
| DR | Debit Memo Request | 3300000000 | 3399999999 |
| RK | Invoice Correct. Req. | 3400000000 | 3499999999 |
| SD2 | Replcmnt Deliv. Ord. | 3500000000 | 3599999999 |
| OR | Standard Order | 3600000000 | 3699999999 |
| VC01 | Value Contract | 3700000000 | 3799999999 |
| CBRE | Lean Return | 3800000000 | 3899999999 |

### Delivery Document Type

| Delivery Document Type | Description | Number Range From | Number Range To |
| --- | --- | --- | --- |
| CCBF | Returns Issue Delivery | 3800000000 | 3899999999 |
| CCLR | ConsReturn Delivery | 3900000000 | 3999999999 |
| LF | Outbound Delivery | 4000000000 | 4099999999 |
| LO | Delivery w/o Ref. | 4100000000 | 4199999999 |
| LR | Deliv.forCust.Returns | 4200000000 | 4299999999 |
| LR2 | Std Returns Delivery | 4300000000 | 4399999999 |
| NL | Replenishment Dlv. | 4400000000 | 4499999999 |

### Billing Document Type

| Billing Document Type | Description | Number Range From | Number Range To |
| --- | --- | --- | --- |
| CBRE | Credit Memo for Returns | 4500000000 | 4599999999 |
| F2 | Invoice | 4600000000 | 4699999999 |
| F5 | Pro Forma for Order | 4700000000 | 4799999999 |
| F8 | Pro Forma for Delivery | 4800000000 | 4899999999 |
| FAS | Down Payment Request Cancellation | 4900000000 | 4999999999 |
| FAZ | Down Payment Request | 5000000000 | 5099999999 |
| G2 | Credit Memo | 5100000000 | 5199999999 |
| L2 | Debit Memo | 5200000000 | 5299999999 |
| S1 | Invoice Cancellation | 5300000000 | 5399999999 |
| S2 | Credit Memo Cancellation | 5400000000 | 5499999999 |

# Quality Check

- Visible scanned PDF values have been converted into Markdown tables.
- Ambiguous scanned values are marked as `Clarification Required`.
- No visible KDS section from the 12-page PDF was intentionally omitted.
