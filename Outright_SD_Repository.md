PROJECT GALANA

SAP S/4 HANA PUBLIC CLOUD

User Training Manual

Module: Sales and Distribution

Process: Sales Order for Outright

21 Novenber, 2025

Version 1.0

Table of Contents:

Objective ……………………………………………………………………………………………….2

Sales Order Creation ……………..……………………………………………………………............3

Outbound Delivery …...………………………………. ……………………………………………... 7

Posting Goods Issue (PGI) ………………………………………………………………………….11

Billing and Financial Impact ……………………………………………………………………….13

Objective

This document provides a detailed guide for processing Delivery and Billing for LPG Sales in SAP S/4HANA Public Cloud. “In LPG commercial model, when a customer opts to purchase LPG together with a new cylinder, the transaction is treated as an outright purchase. The cylinder is classified as a non-returnable asset( full ownership is transferred to the customer at the point of sale). Accordingly, the customer is invoiced for both:

The cylinder cost (treated as a material sale in SD), and

The LPG product (content).

Within the Sales and Distribution (SD) process, this scenario is handled like a standard sale involving multiple materials—one for the cylinder and one for the LPG content. Both items flow through the standard SD steps: sales order creation, delivery processing, goods issue, and billing, ensuring proper revenue recognition and inventory updates in S/4HANA Public Cloud.

Sales Order Creation

This shows the SAP S/4HANA Cloud system interface, where users can access various modules like Purchasing, Sourcing, Production, and Shipping. The highlighted magnifying glass icon at the top right is the global search function, allowing users to quickly find transactions, apps, or data across the SAP system.

This screenshot shows how to use the global search bar in SAP S/4HANA Cloud to locate the "Create Sales Orders" app (transaction VA01). Simply type your desired transaction or app name into the search field, and matching results will appear in a dropdown. Selecting "Create Sales Orders - VA01" lets users quickly access the sales order creation process without navigating through multiple menu paths. This feature speeds up workflow and improves efficiency for SD users.

Sales Organization: GEKE – Refers to the part of the company responsible for sales, ensuring the order is assigned to the correct business unit.

Distribution Channel: 10 – Represents the method or channel through which products reach customers, such as direct sales, retail, or online.

Division: 30 – Categorizes the order by product line or business area, supporting reporting and strategic decisions.

The highlighted areas in this SAP SD "Create Standard Order" screen represent key fields required for sales order processing.

Sold-to Party is the customer placing the order, and Ship-to Party is the customer location where goods will be delivered, typically both are filled automatically based on selection.

Customer Reference lets users enter the customer’s own reference number or note for tracking the order, while Customer Reference Date captures the date relevant to this reference

Delivery Plant specifies the warehouse or plant (here, WH02: GE Lake Oil Warehouse) from which goods will be shipped to fulfil the order.

This screenshot shows the item details section of a sales order in SAP S/4HANA Cloud, where individual products are listed. The highlighted fields display the ordered materials (LPG-1001 and LPG-1035) with their respective order quantities, as well as the plant code "WH02" indicating the warehouse supplying these items. Each line represents a separate item in the order, specifying the relevant material and delivery details. This ensures accurate picking and shipping of the correct products from the designated plant.

Pricing  For  Material LPG-1035

Pricing For  Material LPG-1001

This screen confirms successful sales order creation in SAP S/4HANA Cloud by displaying the message "Standard Order 7000000525 has been saved". The highlighted section at the bottom indicates the unique order number generated after saving. Users can note or copy this number to track, process, or reference the newly created sales order in future transactions. This message confirms the completion of the order entry process.

Outbound Delivery

This screenshot shows how to search for and select the "Create Outbound Delivery - With Order Reference" app in SAP S/4HANA Cloud. The highlighted area in the dropdown menu indicates the recommended option for creating outbound deliveries based on existing sales orders. By choosing this app, users can efficiently proceed to delivery processing linked to specific orders, ensuring goods are shipped accordingly. This helps streamline post-sales logistics and order fulfillment.

This screen is for creating an outbound delivery with reference to a sales order in SAP S/4HANA Cloud. The highlighted fields include "Shipping Point: WH02" (specifying the location for delivery processing), "Selection Date" (24.11.2025), and the sales order number "7000000525" to be delivered. After entering these details, click the highlighted "Continue" button to proceed with outbound delivery creation. These fields ensure the correct order and warehouse are selected for goods issue and shipment.

In this outbound delivery creation screen, the highlighted "Picking" tab lets users manage the picking process for each item before shipment in SAP S/4HANA Cloud. The material list includes items to be picked (LPG-1001 and LPG-1035) with delivery quantities and product details. The screen also displays planned goods issue date and item weights, supporting smooth warehouse operations. Clicking "Picking" allows warehouse users to confirm which items are physically picked and prepared for delivery.

In this SAP SD outbound delivery picking screen, the highlighted areas show key details before saving. "Plant" identifies the warehouse (WH02) responsible, and "Picked Qty" records the quantity physically picked for shipment. "Batch" indicates the specific batch numbers for each picked item, ensuring traceability. Click "Save" to confirm the picking process and update the delivery document in the system.

This screen confirms that the outbound delivery document has been successfully created in SAP S/4HANA Cloud. The highlighted area shows the outbound delivery number "80000345" and confirms it is saved, linking it to the specified sales order "7000000525" from shipping point WH02. Users can now proceed with post-processing steps such as goods issue or shipment for this delivery. This ensures that the order-to-delivery workflow is completed and recorded in the system.

Change Outbound Delivery:

This screenshot demonstrates how to search for and select the "Change Outbound Delivery" app in SAP S/4HANA Cloud. After successfully creating and saving an outbound delivery, users can use this function—highlighted in the dropdown—to modify or update delivery documents as needed. The bottom of the screen confirms the previously saved outbound delivery number and clicking "Change Outbound Delivery" allows for corrections or additional processing, such as posting goods issue or amending delivery details. This ensures flexibility and control in managing outbound logistics.

This SAP S/4HANA Cloud screen allows the user to enter an outbound delivery number (highlighted: 80000345) for editing or processing the delivery document. The highlighted "Continue" button advances to the next step, where detailed delivery or goods issue actions can be performed. This step ensures the correct outbound delivery is selected for further logistics tasks, such as updating picking, packing, or posting the goods issue

Post Goods Issue

This SAP S/4HANA Cloud screen presents outbound delivery details for the shipment process and highlights the "Post Goods Issue" button used to finalize delivery execution. Once all picking and shipment details are confirmed, users click this button to officially issue goods from inventory, updating stock and marking the items as delivered. This step is critical for completing the logistics chain, updating inventory, and progressing to billing.

This final SAP S/4HANA Cloud screen confirms the successful completion of the goods issue process for the outbound delivery. The highlighted message at the bottom shows, "Outbound Delivery 80000231 saved, material document 4900000250 created," indicating that inventory has been updated and the delivery is ready for shipment and billing. This message provides both the outbound delivery and material document numbers for reference and further logistics processing.

Create Billing:

This final SAP S/4HANA Cloud screen confirms the successful completion of the goods issue process for the outbound delivery. The highlighted message at the bottom shows, "Outbound Delivery 80000231 saved, material document 4900000250 created," indicating that inventory has been updated and the delivery is ready for shipment and billing. This message provides both the outbound delivery and material document numbers for reference and further logistics processing.

This SAP S/4HANA Cloud billing screen displays the document flow after outbound delivery, with the delivery document (highlighted: 90000308) ready for invoicing. The "Documents to Be Processed" section shows the delivery is fully invoiced, indicating billing can be executed or modifications made before completion. Users select the document and use the "Save" or "Execute" buttons to process billing or generate the final invoice for the customer. This step completes the SD cycle from order creation to billing.

This SAP S/4HANA Cloud screen confirms the billing document creation after processing delivery and goods issue. The highlighted message states, "Document 90000308 has been saved," indicating that the invoice (billing document) has been successfully generated and stored in the system. This final step completes the SD process, allowing the company to send the invoice to the customer and receive payment.

This SAP S/4HANA Cloud screen displays the option to search for and select the "Change Billing Documents" app, highlighted at the top. After a billing document is successfully created (see confirmation at the bottom), this app allows users to amend or update billing documents, for example, to adjust invoice details or correct errors. This functionality ensures flexibility and accuracy in the invoicing process by allowing billing data to be edited as needed.

This SAP S/4HANA Cloud invoice screen displays the final billing details after the SD process is completed. The highlighted section shows invoice type "F2 Invoice" and document number 90000206, along with the customer and billing date. Below, all items are listed with invoiced quantity, net value for each (in KES), and the computed tax amount for each product. This ensures all sales order items are correctly billed and posted for accounting and customer payment.

This SAP S/4HANA Cloud screen shows the step where users release the billing document (highlighted: 90000308) to accounting. The highlighted "Release to Accounting" button at the top completes the integration, ensuring the invoice is posted to financial accounting for revenue recognition and payment tracking. This action links the SD and FI modules, finalizing the billing process in SAP.

This SAP S/4HANA Cloud screen confirms that the billing document (highlighted: 90000308) has already been posted to accounting. The message at the bottom, "The document has already been passed on to accounting," ensures financial data from sales and distribution is now reflected in the company's accounting records. This status means no further release is needed and the SD-to-FI integration step is complete.