SAP S/4HANA Public Cloud Implementation

END USER MANUAL

LPG Cylinder Sales Process

Submitted to
Galana Energies Limited

Prepared by
Yatendra Pratap Singh

Table of Contents

1. Objective

2. Business Process Overview

3. Accessing the Application

4. Creating LPG Sales Order

5. Understanding Key Fields

6. Order Approval and Release

7. Delivery Creation and Post Goods Issue

8. System Integration and Business Impact

Objective

This manual provides a detailed step-by-step guide for creating and processing LPG Cylinder Sales orders in SAP S/4HANA Public Cloud. It covers order creation, approval, delivery, and post goods issue stages for both cylinders and gas elements. The objective is to standardize the process flow, ensuring accuracy, traceability, and proper integration across SD, MM, and FI modules.

Business Process Overview

The LPG Cylinder Sales process involves creation of a Standard Sales Order (Order Type OR) under the B2B Local channel. Each sales order undergoes an approval workflow before proceeding to delivery. Deliveries are made from specific warehouse plants, followed by picking, batch assignment, and goods issue posting and billing.

Key Process Steps:
1. Create Sales Order – VA01
2. Order Approval Workflow
3. Create Delivery – My Sales Orders Due for Delivery
4. Picking, Batch, and Transporter Details
5. Post Goods Issue
6. Billing and Financial Posting

Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. Search for ‘Create Sales Orders – VA01’.
3. Select the app under Sales and Distribution.
📸 Refer to Screenshot 1: Accessing the App.

Creating LPG Sales Order

Step 1 – Enter Sales Order Type and Organizational Data
• Order Type: OR (Standard Order)
• Sales Organization: GEKE (Galana Energies Ltd.)
• Distribution Channel: 10 (B2B Local)
• Division: 30 (LPG)
• Sales Office: WH01 (NTL Warehouse)
• Sales Group: NR3 (Nairobi Depot)
📸 Refer to Screenshot 2: Organizational Data.

Step 2 – Maintain Customer and Reference Details
• Sold-to Party: 1100000000 – GE Athi River
• Ship-to Party: 1100000000 – GE Athi River
• Customer Reference: cust ref (Customer Order reference)
• Customer Reference Date: 11.11.2025
📸 Refer to Screenshot 3: Customer Details.

Step 3 – Add Material Details
• Material 1: LPG-1005 (6 KG Cylinder)
• Material 2: LPG-1009 (6 KG Gas Element)
• Order Quantity: 10 PC each
• Delivering Plant: WH02 (Warehouse 2)
📸 Refer to Screenshot 4: Item Details.

Once all details are entered, click ‘Save’. System confirms: ‘Standard Order 7000000253 has been saved.’

Understanding Key Fields

• Order Type (OR): Identifies a Standard Order for regular sales.
• Sales Organization (GEKE): Represents Galana Energies Ltd as the selling entity.
• Distribution Channel (10): Indicates a B2B local business channel.
• Division (30): Product line for LPG.
• Sales Office (WH01): Physical warehouse managing the sale.
• Delivering Plant (WH02): Dispatch location for goods.
• Customer Reference: Links to customer PO.
• Material Codes: Represents the LPG product and its components.

Order Approval and Release

1. After order creation, it enters the approval workflow.
2. Navigate to ‘My Sales Order Due for Delivery’ app.
3. Select the created order (7000000253).
4. Click ‘Dialog’ → Review Order.
5. Click ‘Release’ to approve the order.
📸 Refer to Screenshot 5: Sales Order Approval.

Delivery Creation and Post Goods Issue

Step 1 – Create Delivery
• Go to ‘My Sales Orders Due for Delivery’.
• Select the approved sales order.
• Click ‘Dialog’ to generate delivery.
📸 Refer to Screenshot 6: Delivery Creation.

Step 2 – Enter Picking and Transport Details
• Storage Location: LP01 (LPG Storage)
• Picked Quantity: As per order quantity.
• Batch: 0000000016 (batch-managed LPG stock).
• Driver Name, Transporter, and Vehicle Reg No are updated under Custom Fields.
📸 Refer to Screenshot 7: Picking and Custom Fields.

Step 3 – Post Goods Issue (PGI)
• After picking and transporter details are updated, click ‘Post Goods Issue’.
• System confirms: ‘Outbound Delivery 80000127 saved, Material Document 4900000100 created.’  
📸 Refer to Screenshot 8: PGI Confirmation.

Billing processing

System Integration and Business Impact

• SD-FI Integration: Triggers revenue posting and accounts receivable updates.
• SD-MM Integration: Reduces stock and records batch movement in inventory.
• Approval Workflow ensures compliance and pricing validation.
• PGI completion marks physical stock transfer and triggers accounting entries.
• Business Impact: Provides visibility into LPG sales, batch traceability, and accurate stock depletion per depot.

Stock Reconciliation Report

Stock Overview – LPG Materials (Multiple Materials App)

The Stock – Multiple Materials Fiori app provides an overview of available LPG stock across plants and storage locations.

In this example, Plant WH02 (Warehouse 2) has been selected to display the current inventory status. The list shows both regular and special stock types, including returnable packaging with customers.

Highlighted Fields Explanation:

Plant (WH02): Specifies the warehouse or depot where the LPG stock is managed.

Customer (1100000000 – GE Athi River): Indicates special stock belonging to or reserved for a specific customer.

Storage Location (LP01): Denotes the physical sub-location within the plant where the stock is stored (LPG Sale SL).

Material & Description: Identifies each LPG product, such as 6 KG Cylinder or 6 KG Gas Element.

Unrestricted Stock: Displays the quantity available for sale and delivery, showing total unrestricted stock = 3,917 PC in this case.