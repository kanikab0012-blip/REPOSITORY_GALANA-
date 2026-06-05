---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: Create Sales Order - White Fuel Local Sales
source_document: White_Fuel_Local_Sales_Order_Manual_Galana.docx
---

# Create Sales Order - White Fuel Local Sales

## 1. Objective

This document guides users on creating a Sales Order for White Fuel Local Sales in SAP S/4HANA Public Cloud. It covers order creation, field-level data, pricing condition determination, approval workflow, and system integration for accurate order-to-cash processing.

## 2. Business Context

White Fuel Local Sales orders represent B2B customer sales for petroleum products. These orders are created with standard order type **OR**. Pricing, credit checks, and taxes are automatically determined based on master data and configuration.

## 3. SAP Applications Used

| SAP App | Purpose |
|---|---|
| Create Sales Orders - VA01 | Create White Fuel Local Sales order |
| Services for Object | Attach supporting customer documents |
| My Inbox | Approval workflow review |

## 4. Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. Search for **Create Sales Orders**.
3. Select **Create Sales Orders - VA01**.

## 5. Creating Sales Order for White Fuels

### Step 1 - Define Order Type and Organizational Data

| Field | Value |
|---|---|
| Order Type | OR - Standard Order |
| Sales Organization | GEKE - Galana Energies Ltd. |
| Distribution Channel | 10 - B2B Local |
| Division | 10 - White Fuels |
| Sales Office | ELDT - KPC Eldoret |
| Sales Group | EL1 - Eldoret Depot |

### Step 2 - Select Customer and Reference Details

| Field | Value / Example |
|---|---|
| Sold-to Party | 1100000000 - GE Athi River |
| Ship-to Party | 1100000000 - GE Athi River |
| Customer Reference | Customer LPO / order reference number |
| Reference Date | Auto-filled based on entry date |
| Payment Terms | PC04 - 15 days from invoice date |
| Incoterms | DAF - Delivered at Frontier |

### Step 3 - Attach Supporting Documents

Use **Create Attachment** under **Services for Object** to attach:

- LPO
- Customer correspondence
- Any supporting order authorization document

Business purpose: This supports auditability and order authorization.

### Step 4 - Enter Item Details

| Field | Value |
|---|---|
| Delivery Plant | KLE1 - KPC Eldoret Local Sale |
| Material | WF-1001 - Petrol PMS |
| Order Quantity | 10 M3 |
| Requested Delivery Date | 10.11.2025 |

## 6. Item Level Data and Pricing Conditions

Double-click the line item to access item details. Navigate to the **Conditions** tab to review pricing.

### Condition Types Used

| Condition Type | Description |
|---|---|
| ZPR0 | Base Price, automatically determined based on price setup |
| ZPR1 | Price Variance; system allows price to increase above base price but not decrease below it |
| TTX1 | Tax, determined based on tax master setup |

## 7. Approval Workflow

After the Sales Order is created, it enters an approval workflow before delivery.

Approvers review the Sales Order in **My Inbox**.

Approval checks include:

- Pricing validation
- Credit validation
- Master data validation
- Completeness check

After approval, the sales order becomes eligible for delivery creation.

## 8. System Impact and Integration

After successful creation and approval:

| Impact Area | Description |
|---|---|
| Sales Document | Unique sales document number is generated, for example 7000000252 |
| FI | Credit management and payment terms validation |
| MM | Material stock check and plant assignment |
| SD | Pricing, tax determination, delivery scheduling |
| ATP | Available-to-Promise check confirms stock availability |
| Document Flow | Maintained from order creation to billing |

## 9. Output Documents

| Document | Example |
|---|---|
| Sales Order | 7000000252 |

## 10. Business Rules

| Rule | Description |
|---|---|
| Standard order type | White Fuel Local Sales uses OR |
| B2B Local channel | Distribution Channel 10 is used |
| White Fuel division | Division 10 represents White Fuels |
| Customer reference | LPO/order reference should be maintained |
| Supporting documents | LPO/customer documents should be attached |
| Approval required | Order requires approval before delivery |
| Price protection | ZPR1 allows increase above base price but not decrease below base price |

## 11. Troubleshooting

| Issue | Possible Cause | Resolution |
|---|---|---|
| Pricing missing | Condition records not maintained | Check ZPR0/ZPR1 setup |
| Approval pending | Workflow not approved | Check My Inbox approval status |
| Delivery not possible | Sales order not approved | Complete approval workflow |
| ATP failure | Insufficient stock | Check stock at KLE1 |

## 12. RAG Search Keywords

Galana, SAP SD, SAP S/4HANA Public Cloud, White Fuel Local Sales, Create Sales Orders, VA01, GEKE, B2B Local, White Fuels, ELDT, EL1, KLE1, WF-1001, Petrol PMS, ZPR0, ZPR1, TTX1, My Inbox, Approval Workflow, ATP, Sales Order 7000000252.
