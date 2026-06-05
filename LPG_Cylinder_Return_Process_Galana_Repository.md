SAP S/4HANA Public Cloud Implementation

END USER MANUAL

LPG Cylinder Return Process – Returnable Transportation Packing

Submitted to
Galana Energies Limited

Prepared by
Yatendra Pratap Singh

Table of Contents

1. Objective

2. Business Process Overview

3. Accessing the Application

4. Creating Return Order for Empties

5. Consignment Stock Selection (Customer Returns)

6. Processing Lean Return Delivery and Goods Receipt

7. System Integration and Business Impact

Objective

This user manual explains the process for handling LPG Cylinder Returns under the Returnable Transportation Packing (RTP) model. It details how to create a return order for empty cylinders (Order Type CBG0), select consignment stock at customer location, and post goods receipt to bring the returned cylinders back into the warehouse inventory.

Business Process Overview

The LPG Cylinder Return process is used when customers return empty cylinders after consumption. The transaction is handled as a consignment return where the stock moves from the customer’s location back to the plant. The process ensures accurate tracking of returnable assets and inventory reconciliation at depot and plant level.

Process Flow:
1. Create Return Sales Order (CBG0 – Return Pack./Empties)
2. Reference original LPG Sales Order
3. Select batch from ‘Consignment Stock at Customer’
4. Create Lean Return Delivery
5. Post Goods Receipt for returned cylinders
6. Stock updated back to unrestricted inventory in warehouse.

Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. Search for ‘Create Sales Orders – VA01’ in the search bar.
3. Select the app from the list.
📸 Refer to Screenshot 1: Accessing VA01 App.

Creating Return Order for Empties

Step 1 – Enter Order Type 
• Order Type: CBG0 – Return Pack./Empties
• Sales Organization: GEKE – Galana Energies Ltd.
• Distribution Channel: 10 – B2B Local
• Division: 30 – LPG
📸 Refer to Screenshot 2: Order Type and Organizational Data.

Step 2 – Create Order with Reference
• Click on ‘Create with Reference’.
• Select the ‘Order’ tab.
• Enter original Sales Order number (e.g., 7000000253).
• Click ‘Copy’ to reference all relevant item details from the sales order.
📸 Refer to Screenshot 3: Create with Reference.

Step 3 – Update Material and Quantity
• Material: LPG-1005 (6KG Cylinder)
• Order Quantity: 5 PC (based on returned quantity).
• Requested Delivery Date: 11.11.2025
Click ‘Save’ to create the return order. 
System message: ‘Return Pack./Empties 600000038 has been saved (delivery 84000011 created).’ 
📸 Refer to Screenshot 4: Order Creation Confirmation.

Processing Lean Return Delivery and Goods Receipt

Step 5 – Open Lean Return Delivery
• Navigate to ‘Change Outbound Delivery – VL02N’ app.
• Enter Delivery Number: 84000011
• Click ‘Continue’ to access the delivery document.
📸 Refer to Screenshot 6: Delivery Access.

Consignment Stock Selection (Customer Returns)

Step 4 – Select Batch from Consignment Stock
• During batch selection, choose the option ‘W: Consignment Stock at Customer’.
• Enter:
   - Material: LPG-1005
   - Plant: WH02
   - Customer: 1100000000 (GE Athi River)
• Click ‘Go’ to fetch available consignment stock batches.
📸 Refer to Screenshot 5: Batch Selection for Consignment Stock.

Step 6 – Update Picking Details
• Go to the Picking tab.
• Enter:
   - Storage Location: LP01 (LPG Sale SL)
   - Delivery Quantity: 5 PC
   - Batch: 0000000016 (as per returned stock)
📸 Refer to Screenshot 7: Picking Details.

Step 7 – Post Goods Receipt
• Click ‘Post Goods Receipt’ to confirm return of empty cylinders into warehouse stock.
• System displays: ‘Lean Returns Dlv. 84000011 has been saved.’
📸 Refer to Screenshot 8: PGI Confirmation.

System Integration and Business Impact

• SD Integration: Return Order (CBG0) and Delivery documents ensure full traceability to the original sales order.
• MM Integration: Cylinder stock moves from ‘Consignment at Customer’ to unrestricted warehouse stock can be checked through report “Stock -multiple materials”.
• FI Integration: No direct financial posting until cylinders are reused or scrapped.
• Business Impact: Enables full visibility of returnable LPG cylinders, prevents stock loss, and ensures compliance with asset management policy.