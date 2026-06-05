PROJECT GALANA

SAP S/4 HANA PUBLIC CLOUD

User Training Manual

Module: Sales and Distribution

Process: Consignment

14 November, 2025

Version 1.0

Objective

The objective of consignment in SAP SD is to optimize inventory and cash flow management by allowing goods to be stored at the customer's location without transferring ownership until they are consumed. This arrangement reduces inventory carrying costs for customers and minimizes financial liabilities for the vendor until consumption occurs. It strengthens supplier-customer relationships through transparency and trust, while providing customers with ready access to stock, which enhances service levels and reduces lead times. Consignment also streamlines supply chain efficiency, enabling real-time stock visibility and improving overall operational coordination. Additionally, it supports demand-driven supply models by aligning inventory with actual consumption, helping businesses reduce excess stock and optimize resource allocation. Overall, consignment in SAP SD aims to improve sales flexibility, financial planning, and collaboration between trading partners for mutual business benefits.

Consignment Fill-Up

Consignment from an SD (Sales and Distribution) perspective is a special stock arrangement where goods are physically sent to the customer's location but remain the property of the supplying company until sold. The customer (consignee) holds the stock and sells it, but payment to the supplier (consignor) occurs only when the goods are consumed or sold by the customer. The process includes key steps such as consignment fill-up (stock delivery to customer), consignment issue (sale and invoicing when goods are used), consignment return (return of unused stock), and consignment pickup (return of stock to supplier). This arrangement reduces inventory carrying costs for the customer and helps maintain closer inventory control and availability. In SAP SD, consignment is managed through specific sales orders, delivery, and billing processes tailored to track ownership and billing appropriately.

Accessing the Application:

1. Navigate to SAP Launchpad.
2. In the search bar, type 'Create Sales Orders'.
3. Select the application 'Create Sales Orders - VA01'.

This screen is used to create a consignment fill-up sales document in SAP S/4HANA Cloud, with the order type set to "CCFU". Key organizational data such as Sales Organization (GEKE), Distribution Channel (10 – B2B Local), and Division (10 – White Fuels) must be selected to route and process the transaction correctly. Users can enter optional values for Sales Office and Sales Group if required. Once the required fields are filled, clicking "Continue" allows users to move forward with creating the sales document. This step ensures that consignment transactions are linked to the right business unit and market segment.

This screen shows the main details for creating a consignment fill-up sales order in SAP S/4HANA Cloud. The Sold-to Party and Ship-to Party fields are filled with customer codes, and a customer reference (“Fill up”) with a specific date is entered for tracking purposes. Pricing and payment information, including payment terms (“PC04”) and pricing date (“11/18/2025”), are highlighted for sales processing. Delivery terms are specified using Incoterms (“DAF”) and the delivery location, ensuring clear shipment instructions between parties. Once all relevant data is checked, saving the order posts it in the system for further processing.Highlighting one material line for WF-1001. Relevant fields shown are the order quantity (10), item category (CFN), delivery date, plant (KLE1), batch, and amount. The pricing is specified with a condition type (ZPRO), showing a net price of 100.00 KES per unit.

This screenshot shows the confirmation message after successfully saving a consignment fill-up sales order in SAP S/4HANA Cloud. The green notification at the bottom states, "Consignment Fill-Up 7000000389 has been saved," indicating that the document is now recorded in the system. All the sales, items, and organizational details previously entered have been accepted for processing. Users can proceed to the next logistics or consignment step, knowing the sales document is stored and ready for further action.

Outbound Delivery

Consignment in SAP SD is a process where a company sends goods to a customer, but ownership remains with the company until the goods are consumed or sold by the customer. The customer stores the goods on-site and only pays for what is used or sold, reducing upfront costs. Consignment involves specialized processes like consignment fill-up (stock sent), issue (usage/sale), return (unused stock returned), and pickup (stock collection by supplier). Outbound deliveries for consignment in SAP can be created with or without reference to a sales order, supporting flexible logistics and accurate stock tracking.

This screen is used to initiate the creation of an outbound delivery referencing a consignment sales order in SAP S/4HANA Cloud. Users must specify the shipping point (“KLE1 – KPC Eldoret Local Sale”) and select the sales order to be delivered (7000000389) with its corresponding selection date (11/18/2025). Once these details are entered, clicking the “Continue” button moves the process forward to the delivery details stage. This ensures that the consignment goods are dispatched from the correct location and linked to the right order in the system.

This screenshot displays the Picking tab for an outbound delivery in SAP S/4HANA Cloud, detailing the selection of consignment stock for shipment. The material WF-1001 is listed with a delivery quantity and picked quantity of 10 units, confirming the allocation of stock from the specified storage location (KLE1). Additional fields such as batch, staging date, and unit of measure help users validate the logistics details before finalizing the outbound movement. These entries ensure that the correct goods are selected and accounted for prior to saving and continuing the delivery process.

This screenshot confirms the successful creation of an outbound delivery with order reference in SAP S/4HANA Cloud. The green message at the bottom indicates that outbound delivery document 80000250 was saved and associated material document 4900000278 was created, meaning the goods issue and physical movement are now posted in the system. Key details like shipping point (KLE1), order (7000000389), and selection date (11/18/2025) are displayed at the top. Users can now proceed confidently to the next process step, knowing that inventory and logistics records have been accurately updated.

Consignment Issue

Consignment Issue means that a company keeps its products at the customer’s place, but the customer will only pay once they actually use the product. Instead of buying it upfront, the customer can keep the stock with them and consume it whenever needed. When they use the material, it becomes a “Consignment Issue,” and the company then creates a bill only for the quantity consumed. This helps customers reduce risk and cash blockage, and at the same time helps the company increase sales and build trust, because the material is always available at the customer location when required.

Sales order for Consignment Issue:

This screen is for creating a sales document in SAP S/4HANA Cloud with the order type set to "CCIS". The required organizational data includes Sales Organization ("GEKE") and Distribution Channel ("10"), which must be entered to proceed. The Division field is available for input if required, along with optional fields for Sales Office and Sales Group. After filling in the necessary details, users should click the "Continue" button to move to the next step in sales order creation. This ensures the order is routed correctly within the organization for further processing.​

This screen displays the main entry page for creating a consignment issue in SAP S/4HANA Cloud, where consignment stock is issued to the customer. The Sold-to Party and Ship-to Party fields are populated with the customer’s codes and names, and a customer reference (“Issue”) is entered for tracking. Important sales details such as required delivery date, pricing date, payment terms (“PC04 – 15 days from invoice date”), and Incoterms (DAF) with location are clearly shown. This setup ensures the consignment issue is correctly documented and ready for the next logistics or billing step after saving.

This section lists the item details for a consignment issue document in SAP S/4HANA Cloud. It features the material (WF-1001), order quantity (10 M3), item description (PMS), and relevant logistics data like item category (CIN) and required delivery date (11/18/2025). Users can review this summary to ensure all product and delivery details are correct before saving the consignment issue for further process steps. This helps confirm accurate inventory movement and customer fulfillment.

This screenshot displays the Conditions tab for a consignment issue item in SAP S/4HANA Cloud, showing detailed pricing elements for material WF-1001. Pricing and calculation breakdown includes price (ZPRO), gross amount, net amount, surcharges/discounts, and output tax (TTX1), along with the respective values in KES and unit M3. Users can review how the system arrives at the total net price and the tax amount before saving the document. This ensures that all pricing and tax computations are clearly visible and verified as part of the consignment issue process.

This screenshot confirms the successful creation of a consignment issue document in SAP S/4HANA Cloud. The green notification at the bottom states, "Consignment Issue 2000000016 has been saved," indicating that all details entered have been accepted and the stock has been issued to the customer as consignment. Users can now proceed with the logistics or billing steps, confident that the inventory movement is correctly recorded in the system.

Creation of Delivery

This screen is used to create an outbound delivery with reference to a consignment issue order in SAP S/4HANA Cloud. The user must enter the shipping point (KLE1) and the relevant consignment issue order number (2000000016), along with the selection date (11/18/2025). After inputting this data, clicking the “Continue” button advances the process to item and logistics details, ensuring the goods movement is linked accurately to the correct consignment issue. This step is essential for tracking consignment inventory as it moves to the customer.

This screen shows the Picking tab of a consignment return issue delivery in SAP S/4HANA Cloud, where the consignment stock is being processed for return or issue. The ship-to party is specified, and the detailed item line shows material WF-1001, with a delivery and picked quantity of 10 M3 from storage location KLE1 and a specific batch. This tab ensures that the correct items, quantities, and batches are selected before saving the delivery for final posting. The process helps maintain accurate inventory records when handling customer consignment returns or issues.

This screenshot confirms that a consignment return issue delivery has been successfully saved in SAP S/4HANA Cloud. The green tick notification at the bottom states, "Consign/Ret.Issue Dely 2100000015 has been saved," indicating that all relevant data has been accepted and the consignment inventory transaction is now recorded in the system. Users can proceed to the next step in processing or logistics, assured that the document is securely posted.

Invoice

This screen is part of the billing process in SAP S/4HANA Cloud, where users select a delivery for invoicing. The delivery document 2100000015 is shown under "Documents to Be Processed," categorized as a delivery with a processing status of "Fully Invoiced." By selecting this document and clicking "Save," users proceed to generate or update the billing document for the selected consignment return delivery. This ensures that only completed and eligible deliveries are processed for billing.

This screenshot displays the overview of billing items for the creation of an invoice in SAP S/4HANA Cloud. The invoice references material WF-1001 (PMS) with an invoiced quantity of 10 M3. The billing details include net value (1,000 KES), tax amount (160 KES), and the billing date (11/18/2025). Users can review and confirm these details before saving the invoice, ensuring that the financial and tax information is correctly recorded for the consignment return delivery.

This screenshot confirms the successful creation of a billing document in SAP S/4HANA Cloud. The system displays a green notification stating, "Document 90000228 has been saved," indicating that the invoice is now recorded and complete. Users can now proceed with any subsequent financial or reporting steps required, assured that the billing process for the corresponding delivery is finalized in the system.

Sales Return with Reference

This screen is for creating a credit memo request (order type "CCRE") in SAP S/4HANA Cloud. Users must either manually enter organizational data or choose the "Create with Reference" option to base the credit memo on an existing sales document for quick and accurate processing. This step is essential for handling customer returns or granting credits while keeping all relevant references and structure intact.

This screen shows the "Create with Reference" dialog in SAP S/4HANA Cloud, used for creating a credit memo request using an existing billing document as a reference. The user has selected the "Bill Doc" tab and entered billing document 90000228 to serve as the reference for the new credit memo. This speeds up and standardizes the process, ensuring all key billing details flow automatically into the new credit request.

This screen displays a consignment return overview in SAP S/4HANA Cloud. It shows key partner details for the sold-to and ship-to parties, the selected billing block (“Check Credit Memo”), and the item list containing material WF-1001 with an order quantity of 5 M3, item category CRN, and delivery date. All commercial settings such as payment terms and Incoterms are configured. After review, the user can save the document, officially recording the return transaction and enabling subsequent return logistics and credit memo processing.

This screenshot confirms that the consignment return sales document has been successfully saved in SAP S/4HANA Cloud. The green notification states, "Consignment Return 2000000017 has been saved," indicating that all header and item data have been accepted and posted. This document is now ready for subsequent logistics or financial processes, ensuring that the return is officially recorded in the system.

Return Delivery

This screen is for creating an outbound delivery with order reference in SAP S/4HANA Cloud, specifically linked to consignment or return processes. The shipping point is set as "KLE1 – KPC Eldoret Local Sale," and the referenced sales order number is 2000000017 with a selection date of 11/18/2025. After entering these details, clicking "Continue" allows users to proceed to the next step in the logistics flow. This ensures the outbound movement is tied to the correct order and shipping location for accurate inventory handling.

This screenshot is from the consignment return delivery creation process in SAP S/4HANA Cloud, showing the step just before posting goods receipt for returned items. It displays ship-to party details, item (WF-1001, 5 M3, batch, item category CRN), and the "Post Goods Receipt" button at the top, which finalizes inventory movement for returned goods. This step ensures that returned consignment stock is properly received into inventory and documented in the system.

This screenshot confirms that a consignment return delivery (document 2100000016) has been saved in SAP S/4HANA Cloud. The green notification at the bottom indicates successful posting, meaning the referenced return order 2000000017 is now linked to an officially recorded outbound delivery for the returned consignment stock. The process can now continue with goods receipt posting or other subsequent steps in logistics and inventory management.

Return Invoice

This screen shows the billing document creation process in SAP S/4HANA Cloud, specifically for consignment return deliveries. Document 210000016, listed under "Documents to Be Processed," is ready to be selected for invoicing. After selecting the delivery and clicking "Save," the user can generate a credit memo or billing document for the returned consignment items, ensuring accurate financial and inventory reconciliation.

This screenshot displays the overview of a Credit Memo for Returns created in SAP S/4HANA Cloud for billing document 90000229. Material WF-1001, with an invoiced quantity of 5 M3, appears on the document with a net value of 500.00 KES and a tax amount of 80.00 KES. The billing date is 11/18/2025, and the cost associated with the return is also visible. This credit memo finalizes the financial reversal for the returned consignment, reflecting the correct values to be credited to the customer.

This screenshot confirms that credit memo document 90000229 has been successfully saved in SAP S/4HANA Cloud. The green notification at the bottom of the screen indicates the completion of the credit memo process, meaning the customer return and associated financial reversal are now officially recorded in the system.

Consignment Pickup

Consignment Pickup in SAP SD is the process where unsold or unused consignment stock is retrieved from the customer and brought back to the supplier's inventory. The pickup begins with creating a consignment pickup order (order type KA) using transaction VA01, where necessary details like sales area, customer, and quantity are entered. The system then processes a return delivery, transferring the goods back into the supplier’s standard inventory while updating stock balances. No billing occurs in this process since the goods were not consumed or sold by the customer. This step ensures accurate reversal and stock reconciliation for consignment management

Sales Order

This screen is the starting point for creating a Consignment Pick-Up order in SAP S/4HANA Cloud, with the order type "CCPU" selected. The sales organization is "GEKE - Galana Energies Ltd." and the distribution channel is "10 - B2B Local," with the division set to "10 - White Fuels." After confirming or entering these organizational details, users click "Continue" to proceed, or use "Create with Reference" if basing the document on existing sales data. This ensures the consignment pick-up process is initiated correctly under the right commercial structure.

This screen displays the details of a Consignment Pick-Up order in SAP S/4HANA Cloud. The form captures the sold-to and ship-to party data, includes a customer reference ("Pickup"), and the requested date of 11/18/2025. Incoterms are specified as DAF with the location provided, and other organizational and sales information is filled in. This step ensures that all necessary details for the consignment pick-up process are captured before saving the document and proceeding with the physical or financial movement of the stock.

This screenshot confirms that a consignment pick-up document (number 7000000392) has been successfully saved in SAP S/4HANA Cloud. The green notification at the bottom of the screen states, "Consignment Pick-Up 7000000392 has been saved," indicating that all entered details have been accepted and the pick-up order is now officially recorded in the system. This allows the user to proceed with subsequent consignment management or inventory processing steps.​

Outbound Delivery

This screenshot shows the starting step for creating an outbound delivery with order reference in SAP S/4HANA Cloud, referencing consignment pick-up order 7000000392. The shipping point is set as KLE1 (KPC Eldoret Local Sale) and the selection date is 11/18/2025. After entering these details, clicking “Continue” will advance the process so the consignment pick-up goods movement can be managed and tracked appropriately in the system.

This screen displays the Picking tab for a lean returns consignment delivery in SAP S/4HANA Cloud, ready for posting goods receipt. The highlighted section shows ship-to party details, material WF-1001 with a delivery and picked quantity of 5 M3 (batch included), and necessary logistics information. The “Post Goods Receipt” button at the top will confirm the stock movement back into inventory upon execution, finalizing the consignment pick-up process in the system.

This screenshot confirms that a lean returns delivery (document 840000039) has been saved in SAP S/4HANA Cloud. The green notification at the bottom verifies that the outbound delivery for consignment pick-up order 7000000392 is now officially recorded. Users can proceed with the next logistics steps, such as posting the goods receipt, to complete the consignment cycle in the system.