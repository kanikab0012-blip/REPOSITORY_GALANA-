---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: White Fuel Local Sales - Delivery and Billing
---

# White Fuel Local Sales - Delivery and Billing

## Objective
Process delivery creation, transporter details, output documents, PGI, and billing for White Fuel Local Sales.

## SAP Apps Used
- My Sales Orders Due for Delivery
- Change Outbound Delivery
- Create Billing Documents (VF04)

## Process Flow
Sales Order → Delivery → Picking → Transport Details → Output Documents → PGI → Billing → FI Posting

## Delivery Creation

### Step 1 - Identify Sales Order
- Open My Sales Orders Due for Delivery
- Locate Sales Order (Example: 7000000252)
- Ship-To Party: 1100000000
- Click Create Delivery

### Step 2 - Picking and Batch Details

| Field | Value |
|---|---|
| Storage Location | KLE1 |
| Delivery Quantity | 10 M3 |
| Picked Quantity | 10 M3 |
| Batch | Auto-populated (example 0000000006) |

Business Rule: Batch must match KRA batch number.

## Transporter Details

### Header Level

| Field |
|---|
| Driver Name |
| Driver Passport/ID |
| Transporter |
| Vehicle Registration Number |

### Item Level

| Field |
|---|
| Galana Seal Number |
| Customs Seal Number |
| Temperature (Example 20.00°C) |

## Output Control

Menu → Extras → Delivery Output → Output Control

Document Types:
- DELIVERY_NOTE
- DELIVERY_PICK_LIST

Templates:
- FDP_V2_DELIVERY_NOTE_V1
- FDP_V2_PICKING_LIST

## Post Goods Issue (PGI)

Expected Example:
Outbound Delivery 80000125 saved, Material Document 4900000098 created.

Business Impact:
- Stock reduction
- Material document creation
- Accounting entries generated

## Billing

App:
Create Billing Documents - VF04

Steps:
1. Select Delivery 80000125
2. Verify Billing Type F2
3. Execute Billing

Accounting Impact:
- Customer Account (AR) Debit
- Sales Revenue Credit
- VAT Payable Credit

## Integration

- SD
- MM
- FI

## Output Documents

| Document |
|---|
| Delivery Note |
| Picking List |
| Material Document |
| Billing Document |
| Invoice |
