---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: Mass Change of Sales Documents
---

# Mass Change of Sales Documents

## Objective
Perform bulk updates on sales documents without changing orders individually.

## SAP App
Mass Change of Sales Documents

## Supported Documents
- Sales Orders
- Sales Quotations
- Sales Contracts
- Customer Returns
- Debit Memo Requests
- Credit Memo Requests

## Process

### Step 1
Search:
Mass Change of Sales Documents

### Step 2
Select Sales Orders.

### Step 3
Apply Filters

Possible Filters:
- Sales Order
- Sales Organization
- Product
- Sold-To Party
- Ship-To Party
- Delivery Status

Click Go.

### Step 4
Select Orders

Examples:
- 7000000494
- 7000000495

### Step 5
Click Change

Available Actions:
- Change Header Data
- Change Header Partner
- Remove Header Partner
- Reject
- Set Billing Block
- Remove Billing Block
- Set Delivery Block
- Remove Delivery Block
- Update Prices
- Cancel Rejection

### Step 6
Reject Example

Reason:
Rejected by Customer (70)

Click Continue.

### Step 7
Submit Job

Example Job:
SD_Mass_Update_11/21/2025

Click Submit.

## Benefits
- Bulk processing
- Reduced manual effort
- Consistent updates
- Audit-friendly processing

## Monitoring
Use Monitor Mass Changes to review job execution status.
