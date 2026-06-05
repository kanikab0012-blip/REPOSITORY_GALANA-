---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
process_name: Returnable Packaging Issue Billing
repository_type: AI_RAG_Knowledge_Repository
---

# Returnable Packaging Issue Billing

## Objective
Bill customers for LPG cylinders that were not returned.

## Process Flow
CCLN Order -> Delivery -> PGI -> Billing -> FI Posting

## Step 1: Create Returnable Packaging Issue Order
Order Type: CCLN

Enter:
- Sales Organization
- Distribution Channel
- Division

Create with reference to original sales order.

## Step 2: Reference Original Order
Example:
- Sales Order: 7000000253

Click Copy.

## Step 3: Maintain Material
- Material: LPG-1005 (6KG Cylinder)
- Quantity: 5 PC
- Requested Delivery Date: 11.11.2025
- Net Value: 4,500 KES

Save order.

## Step 4: Delivery Processing
App:
- Change Outbound Delivery (VL02N)

Example Delivery:
- 210000004

## Step 5: Picking and PGI
- Storage Location: LP01
- Delivery Quantity: 5 PC
- Batch: 2500000008

Click Post Goods Issue.

## Step 6: Billing
App:
- Create Billing Documents

Select delivery and create invoice.

## Integration
- SD
- MM
- FI

## Business Impact
Ensures accountability for non-returned cylinders and automatic customer charging.
