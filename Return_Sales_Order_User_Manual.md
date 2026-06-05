---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
process_name: Return Sales Order
repository_type: AI_RAG_Knowledge_Repository
---

# Return Sales Order

## Objective
Manage customer returns and process inventory and financial impacts.

## Navigation
SAP Fiori Launchpad → Create Sales Orders (VA01)

## Create Original Sales Order

### Organizational Data
- Order Type: OR
- Sales Organization: GEKE
- Distribution Channel: 10
- Division: 10

### Header Data
- Sold-To Party
- Ship-To Party
- Customer Reference
- Reference Date

### Item Data
- Material: WF-1001
- Order Quantity

Save Sales Order.

## Create Delivery

App:
- Create Outbound Delivery

Example:
- Sales Order: 7000000386
- Shipping Point: KLE1

## Picking

Maintain:
- Picked Quantity
- Batch
- Storage Location

Save.

## Post Goods Issue
Use outbound delivery and execute PGI.

## Billing
Create Billing Document for completed delivery.

## Return Order

Create return order referencing original sales order.

## Return Delivery
Create outbound/return delivery.

## Post Goods Receipt
Receive returned material into inventory.

## Credit Billing
Create return billing / credit processing.

## Business Benefits
- Customer return management
- Inventory reconciliation
- Financial adjustment
- Audit traceability
