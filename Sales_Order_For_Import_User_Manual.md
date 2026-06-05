---
client: Galana
solution: SAP S/4HANA Public Cloud
module: SAP SD
document_type: User_Manual
process_name: Sales Order for Import
repository_type: AI_RAG_Knowledge_Repository
---

# Sales Order for Import

## Objective
Enable bulk creation of sales orders using the Import Sales Documents application.

## Navigation
SAP Fiori Launchpad → Import Sales Documents → Sales Orders

## Process Steps

### Step 1: Open Import Sales Documents
- Search for Import Sales Documents.
- Open the application.
- Select Sales Orders.

### Step 2: Download Template
- Click Download Template.
- Populate mandatory sales order header and item fields.
- Save and close the XLSX file before upload.

### Step 3: Upload Template
- Enter Import Name.
- Click Browse.
- Select completed template.
- Preview uploaded data.

### Header Fields
| Field |
|---------|
| Sales Order Type |
| Sales Organization |
| Distribution Channel |
| Division |
| Sold-To Party |
| Ship-To Party |
| Customer Reference |

### Item Fields
| Field |
|---------|
| Product |
| Requested Quantity |
| Requested Quantity Unit |
| Plant |

### Step 4: Import
- Click Import.
- System validates data.
- Errors are displayed if invalid details exist.

### Step 5: Review Import Status
- Review imported sales orders.
- Click View Import to monitor processing.
