PROJECT GALANA

SAP S/4 HANA PUBLIC CLOUD

User Training Manual

Module: Sales and Distribution

Process: Galana Dealer Station Sales

November 20, 2025

Version 1.0

Table of Contents:

Objective………………………………………………………………............................................... 2

Delivery Overview ..………………………………………………………………............................... 2

Accessing the Application ….…..…………………………………………………………................... 2

Creating Sales Order .............................................................................................. 3

Delivery................................................................................................................. 7

Billing.....................................................................................................................12

Objective

This document provides a detailed guide for processing Delivery and Billing for Galana dealer station Sales in SAP S/4HANA Public Cloud. It includes delivery creation, transporter details entry, document printing, goods issue posting, and billing generation.

Delivery Overview

After a Sales Order is approved, the system allows delivery creation via the ‘My Sales Orders Due for Delivery’ app. The delivery process includes batch selection, transporter information entry, and goods issue posting to record the physical movement of fuel products.

After the sales order is approved in SAP S/4HANA Cloud, users access the ‘My Sales Orders Due for Delivery’ app to initiate the delivery process. The system enables batch selection for products and entry of transporter information, ensuring the correct handling of fuel shipments. Picking, packing, and confirmation steps follow, allowing the selection of storage locations and split quantities if needed. The user reviews delivery details such as planned goods issue and shipment dates. Next, the PGI (Post Goods Issue) step is completed, which officially records the physical movement and reduces inventory. The delivery status is updated, and the document is ready for billing, integrating seamlessly with the rest of the sales cycle.

Accessing the Application:

1. Navigate to SAP Launchpad.
2. In the search bar, type 'Create Sales Orders'.
3. Select the application 'Create Sales Orders - VA01'.

Sales Order:

Sales order creation is the process where a company formally records a customer's request to purchase goods or services, specifying details like product, quantity, price, delivery date, and payment terms. This order serves as a commitment between the seller and buyer, initiating fulfillment activities such as procurement, delivery scheduling, and invoicing. It acts as the foundation for managing customer demand, ensuring timely product availability, accurate billing, and efficient revenue recognition, thereby driving customer satisfaction and business cash flow.

Creating Sales Order:

“Create Sales Orders" app (VA01). Type "create sales order" into the search and select the highlighted result to begin entering a new sales order. This shortcut helps users efficiently start the sales order process without navigating multiple menus. It improves workflow speed and user convenience in daily business operations.

This screen is used to initiate the creation of a sales order in SAP S/4HANA Cloud by selecting the necessary organizational data such as sales organization, distribution channel, and division. The order type "OR" indicates a standard sales order, triggering the full sales process from pricing to billing. The chosen sales organization, channel, and division ensure that the order is processed under the correct company structure and product category. After making these selections, users should click "Continue" to proceed with entering order-specific details.

This screen displays the overview of a standard sales order in SAP S/4HANA Cloud, where key transactional details are entered. The top section captures customer information including sold-to and ship-to parties, reference number, and order date. In the middle, payment terms ("30 days from invoice date") and Incoterms ("DAP") specify financial and shipping conditions for the order. At the bottom, the item list tab summarizes product details, quantities, and requested delivery dates for each item in the order. After verifying all information, the user clicks "Save" to complete the entry.

This screen shows the "Conditions" tab for an item in a standard sales order, where all pricing components are listed in detail. Each row under "Pricing Elements" presents a different price or tax component such as EPRA price, output tax, margin, and gross price, including their respective amounts, currencies, and units. The condition values and related data help calculate the final net price and taxes for the sales item, ensuring the user can review and validate all charges before saving the order. This breakdown supports accurate invoicing, transparency, and auditability in SAP S/4HANA Cloud sales processes.

This confirmation screen appears after successfully saving a standard sales order in SAP S/4HANA Cloud, indicated by the message “Standard Order 70000000466 has been saved” displayed at the bottom. All fields are now cleared for new entry, and users may proceed with creating additional sales documents or exit the transaction. The green status icon confirms that the order has been posted in the system, ensuring the transaction is complete and ready for follow-up processes like delivery or invoicing. This step marks the end of the sales order creation workflow.

Delivery:

This screenshot shows the SAP S/4HANA Cloud home page where the user searches for sales orders due for delivery using the integrated search bar. The dropdown displays relevant apps like "My Sales Order Due for Delivery" and other delivery-related sales order tools, allowing the user to quickly access overdue delivery documents and streamline their workflow. This feature simplifies navigation and ensures timely processing of pending deliveries, promoting efficiency in sales and distribution tasks. The visual layout combines to-do lists, news, and frequently used pages for an organized dashboard experience.

This screen in SAP S/4HANA Cloud is used for display and selection of sales orders, specifically referencing SD Document 70000000466. The user goes to the "Sales Orders" tab, enters criteria like shipping point (KLE1), and sets delivery creation dates to filter relevant records. After defining these parameters, clicking the "Run" button generates a list of matching sales orders for processing or review. This function streamlines order tracking and management, ensuring that scheduled deliveries align with operational requirements.

This SAP S/4HANA Cloud screen displays activities due for shipping, with a list showing all sales orders scheduled for goods issue. Each entry provides core details such as the GI date, delivery priority, ship-to party, route, origin document, gross weight, and volume for efficient shipment planning. The highlighted row corresponds to a sales order ready to be processed, ensuring logistics teams can accurately manage shipping operations. Users can proceed with delivery actions by selecting the order and using the "Dialog" button to confirm further steps.

This SAP S/4HANA Cloud screen is for creating and reviewing outbound delivery details for a specific sales order, focusing on the "Header Details" and "Item Overview" sections. It displays the planned goods issue date, total delivery quantity, and item specifics such as material code (WF-1001), description (PMS), and associated batch number (2500000079). The ship-to party is specified, ensuring that the delivery is scheduled for the right customer location, with all logistics data visible for tracking purposes.

This screen from SAP S/4HANA Cloud presents “Custom fields” during outbound delivery creation, allowing entry of additional transport and logistics details. Users can input specific data such as the driver's name, passport or ID number, transporter company, and vehicle registration number for the delivery. These values are recorded under the "Custom Fields" tab, supporting comprehensive tracking and compliance for each shipment.

This SAP S/4HANA Cloud screen is part of the outbound delivery process, specifically under the "Picking" tab, where the user confirms the quantity of materials picked for delivery. The item overview displays the material code, quantity picked (100 units), batch number, and relevant logistical details, ensuring accuracy in fulfilling customer orders. The pick date and warehouse information support efficient coordination between sales and warehouse operations. Once the picked quantity is validated, clicking "Save" updates the delivery record and moves the order forward in the shipping workflow.

This SAP S/4HANA Cloud confirmation screen shows that the outbound delivery process is complete and successful. The message at the bottom left indicates "Outbound Delivery 80000298 saved, material document 4900000334 created," confirming both the delivery and material movement have been recorded in the system. All relevant shipment details appear in the main row, ensuring users can proceed confidently with further logistics and invoicing steps. The green status icon assures that the transaction is finalized and safely stored.

Billing:

This SAP S/4HANA Cloud screenshot shows the user searching for billing apps by entering "Create billing documents" in the search bar at the top right. The dropdown offers multiple options, including the main "Create Billing Documents" app and transaction-specific shortcuts like VF01 and VF04 for billing document creation. This functionality helps users quickly find and launch tools needed to generate invoices for completed deliveries, streamlining the billing process. The home page remains visible in the background, providing access to additional purchasing and supply chain management tasks.

This SAP S/4HANA Cloud screen lists sales orders and deliveries that are ready for billing, allowing users to select the appropriate document for invoice creation. The highlighted row shows outbound delivery 80000298 for "GE Kabarak" with a net value of 14,268.90 KES and a billing date of 11/20/2025. Users can mark the delivery and click "Create Billing Documents" to generate the corresponding invoice, ensuring timely and accurate billing operations. The filter options and document details help streamline financial management workflows.

This SAP S/4HANA Cloud screen is for managing invoice creation, displaying the document's general information and organizational data for billing. The top section shows the payer and sold-to party, net value, tax amount, and total invoice amount in KES, alongside the billing date and type. Additional data includes company code, sales organization, distribution channel, and product division, plus key terms like Incoterms (Delivered at Place, DAP) and payment deadlines (30 days from invoice date). Users can review all details and click "Save" to finalize the billing document, ensuring accurate invoicing for completed sales transactions.

This SAP S/4HANA Cloud screen confirms that the invoice has been created and saved, displaying all billing details and business conditions for the transaction. The status bar at the bottom indicates "Billing document saved," showing successful posting after the user clicks "Post Billing Document". All essential information—such as payer, sold-to party, billing date, reference, organizational data, payment terms, and Incoterms—is reviewed here, ensuring the billing is accurate and complete before final account posting. This marks the last step in the order-to-cash process where billing data is officially registered in the system.

This SAP S/4HANA Cloud invoice screen confirms that the billing document has been officially posted for the sales transaction. The notification “Billing documents posted” in the center indicates successful registration in the financial system, while all key invoice details—such as payer, sold-to party, document status, reference, and terms—are displayed for review. Users can “Preview” the invoice using the button at the top, or proceed with further actions like printing or sending to the customer. This completes the billing cycle, ensuring everything is finalized for accounting and customer payment.

This screen displays the final printed invoice generated in SAP S/4HANA Cloud for sales order 7000000466 and outbound delivery 80000298. It summarizes all key transaction details—including company, reference number, delivery date, order and delivery IDs, product (WF-1001 PMS), quantity, pricing components, batch number, Incoterms (DAP), payment terms, and tax calculation—with the total invoice amount clearly presented for the customer. The invoice is formatted professionally for sharing with the customer, supporting compliance and transparency in business operations.

This SAP S/4HANA Cloud screen displays the complete Process flow for a business transaction, visualizing each step from order processing through delivery, billing, and accounting. The flowchart confirms the status of important documents: standard order (completed), outbound delivery (shipped), invoice (billed), and journal entry (posted but not cleared), providing a clear audit trail for the transaction lifecycle. Such process visualization helps users quickly review and track progress, ensuring transparency and compliance in order-to-cash operations.