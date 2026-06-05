---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: Sales Order for Hospitality Sales - Zena
source_document: Zena_Hospitality_Sales.docx
---

# Sales Order for Hospitality Sales - Zena

## 1. Document Purpose

This user manual explains the end-to-end SAP S/4HANA Public Cloud process for Hospitality Sales for Zena in Galana. It covers sales order creation, delivery creation, batch split, picking, post goods issue, billing creation, and billing release/accounting checks.

## 2. Business Context

Hospitality sales for Zena are processed after stock update of non-valuated material code using the **Post Goods Movement** app with movement type **501**. Since inventory valuation is not part of Zena, the sales order is created to bill the customer for hospitality sales.

## 3. Process Scope

The process covers:

1. Create Sales Order using **Create Sales Orders - VA01**
2. Enter organizational data
3. Maintain customer, commercial terms, and reference details
4. Maintain material, quantity, plant, and pricing conditions
5. Create outbound delivery
6. Maintain batch split and picking details
7. Change outbound delivery and post goods issue
8. Create billing document
9. Change billing document / release to accounting where applicable

## 4. SAP Applications Used

| SAP App | Purpose |
|---|---|
| Create Sales Orders - VA01 | Create hospitality sales order |
| Create Outbound Delivery | Create delivery with reference to sales order |
| Change Outbound Delivery | Review delivery and post goods issue |
| Create Billing Documents - VF01 | Create invoice/billing document |
| Change Billing Documents | Review/release billing document |

## 5. Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. Use the search bar.
3. Search for **Create Sales Orders**.
4. Select **Create Sales Orders - VA01**.

### Screenshot Handling Notes

The screenshots show SAP Fiori search results, sales order entry screens, item overview screens, pricing elements, delivery creation screens, batch split screens, goods issue confirmation, and billing screens. Highlighted areas show the fields and buttons the user must use.

## 6. Create Sales Order

### Step 1 - Enter Order Type and Organizational Data

Use the **Create Sales Orders - VA01** app.

| Field | Value | Description |
|---|---|---|
| Order Type | OR | Standard Order |
| Sales Organization | ZEAE | Zena sales organization |
| Distribution Channel | 50 | Hospitality / relevant channel |
| Division | 10 | Division used for the sales process |

After entering the required organizational data, click **Continue**.

### Step 2 - Maintain Customer and Commercial Details

| Field | Value / Example | Description |
|---|---|---|
| Sold-to Party | 1400000009 | Company TotalEnergies Marketing Kenya PLC, Kenya |
| Ship-to Party | 1400000009 | Same customer used as ship-to party |
| Customer Reference | Hospitality | Customer/business reference |
| Reference Date | 18.11.2025 | Date of customer reference |
| Requested Delivery Date | 18.11.2025 | Required delivery date |
| Incoterms | CIF | Commercial delivery terms |
| Payment Terms | PC03 | 7 days from invoice date |

### Step 3 - Maintain Item Details

| Field | Value | Description |
|---|---|---|
| Material | NWF-1001 | PMS, non-valuated inventory count |
| Order Quantity | 5 M3 | Ordered quantity |
| Plant | ZKT1 | Plant for Zena hospitality sales |
| Item Category | TAN | Standard item category |
| Delivery Date | 18.11.2025 | Delivery date |

### Step 4 - Resolve Pricing Error

If system displays:

```text
Pricing error: Mandatory condition ZPRM is missing
```

Maintain manual price condition.

| Condition Type | Description | Value |
|---|---|---|
| ZPRM | Price Manual | 1,000.00 USD per 1 M3 |
| ZHSP | Hospitality Service | 200.00 USD |
| ZKPC | KPC Charges | 50.00 USD |

Important note: **ZPRM is statistical only and has no accounting impact**.

### Step 5 - Final Review and Save

Before saving, review:

- Required delivery date: 18.11.2025
- Incoterms: CIF
- Payment terms: PC03 - 7 days
- Material: NWF-1001
- Quantity: 5 M3
- Plant: ZKT1

Click **Save**.

Expected system message:

```text
Standard Order 7000000404 has been saved
```

## 7. Create Outbound Delivery

### Step 1 - Access Create Outbound Delivery

Search and open **Create Outbound Delivery**.

### Step 2 - Enter Delivery Reference Data

| Field | Value |
|---|---|
| Shipping Point | ZKT1 |
| Selection Date | 18.11.2025 |
| Order | 7000000404 |

Click **Continue**.

### Step 3 - Batch Split

The delivery screen allows batch management and batch split.

| Field | Value |
|---|---|
| Material | NWF-1001 |
| Quantity | 5 M3 |
| Plant | ZKT1 |
| Batch | 2500000038 |

For another batch split example:

| Line | Batch | Picked Quantity | Plant / SLoc |
|---|---|---|---|
| 10 | Main item | 10 M3 | ZKT1 |
| 900002 | 2500000046 | 5 M3 | ZKT1 |

Click **Save**.

Expected system message:

```text
Outbound Delivery 80000261 has been saved
```

## 8. Change Outbound Delivery and Post Goods Issue

### Step 1 - Open Change Outbound Delivery

Search for **Change Outbound Delivery**.

Enter outbound delivery:

```text
80000261
```

Click **Continue**.

### Step 2 - Review Delivery

Review:

- Delivery document: 80000261
- Sales order: 7000000404
- Shipping point: ZKT1
- Material: NWF-1001
- Quantity: 5 M3
- Customer: TotalEnergies Marketing Kenya PLC

### Step 3 - Post Goods Issue

Click **Post Goods Issue**.

Expected system message:

```text
Outbound Delivery 80000261 saved, material document 4900000292 created
```

## 9. Billing and Financial Impact

### Step 1 - Open Billing App

Search for:

```text
Create Billing Documents - VF01
```

### Step 2 - Select Delivery for Billing

Use outbound delivery:

```text
80000261
```

Review item details before saving.

### Step 3 - Save Billing Document

Click **Save**.

Expected system message:

```text
Document 90000239 has been saved
```

### Step 4 - Change / Release Billing Document

Search for **Change Billing Documents**.

Use billing document:

```text
90000239
```

The screen may show that the document has already been passed to accounting.

## 10. Business Rules

| Rule | Description |
|---|---|
| Non-valuated stock update | Stock is updated using Post Goods Movement with movement type 501 |
| Manual pricing | ZPRM must be entered manually when mandatory price condition is missing |
| Statistical pricing | ZPRM is statistical only and has no accounting impact |
| Delivery reference | Delivery must be created with reference to the sales order |
| PGI requirement | Billing follows goods issue posting |
| Billing document | Invoice is created after delivery/PGI completion |

## 11. Integration Touchpoints

| Area | Impact |
|---|---|
| SD | Sales order, delivery, billing, document flow |
| MM / Inventory | Goods issue updates stock movement |
| FI | Billing document supports accounting/receivables where relevant |

## 12. Output Documents Generated

| Document | Example |
|---|---|
| Sales Order | 7000000404 |
| Outbound Delivery | 80000261 |
| Material Document | 4900000292 |
| Billing Document | 90000239 |

## 13. Troubleshooting

| Issue | Cause | Resolution |
|---|---|---|
| Mandatory condition ZPRM missing | Manual price not entered | Maintain ZPRM in Pricing Elements |
| Delivery cannot proceed | Incorrect shipping point/order reference | Verify ZKT1 and sales order number |
| Billing not possible | PGI not completed | Complete Post Goods Issue first |
| Billing already passed to accounting | Document already released | Review accounting status in billing document |

## 14. RAG Search Keywords

Galana, SAP SD, SAP S/4HANA Public Cloud, Zena Hospitality Sales, Sales Order, VA01, ZEAE, ZKT1, NWF-1001, ZPRM, ZHSP, ZKPC, Outbound Delivery, Post Goods Issue, Billing, VF01, 7000000404, 80000261, 90000239.
