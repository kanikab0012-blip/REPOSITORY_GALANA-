PROJECT GALANA

SAP S/4 HANA PUBLIC CLOUD

User Training Manual

Module: Sales and Distribution

Process: Intercompany-warehouse sale

November 14, 2025

Version 1.0

ABOUT THIS MANUAL

This manual provides information and specific instructions on all the Galana To Delnet activity steps with the implication of vital processes in standard SAP S/4HANA system. You will see how each of the views is created, its obligatory data, optional fields, and how its creation reflects in the system.

The manual is intended to serve both as a training manual and a reference.

Icons Used

The following icons are used.

OVERVIEW

This scenario explains how Galana Energies and Delnet transact internally for fuel and lubricants when both entities operate from the same physical warehouse, but are treated as separate legal entities in SAP Public Cloud.

The process ensures financial/ownership transfer without physical movement.

Target Audience

This manual shall primarily be used by.

Stores and Finance team

Management and staff members in all other departments may carry Return Sales Order related activities.

Pre-Requisites

Required Knowledge

Working knowledge of Microsoft Office and Internet browsers

Familiarity with navigating of SAP S/4 HANA Public Cloud

Recommended Knowledge

Working knowledge of the Order management and administration business processes

Objective

Using this manual, you will be able to Understand:

Type of Sales Order

Way to Create, modify, display and print Sales Order.

Reports

TERMS, ACRONYMS, ABBREVIATIONS

INTRODUCTION- Galana To Delnet

For a client like Galana Energies where transactions might be infrequent or project-based, SAP uses a "one-time customer" master record approach. This is suitable when you do not want to create a full customer master record due to limited business frequency.

LOGIN TO SAP S/4 HANA PUBLIC CLOUD TENANT

Web Browser- Make sure you have updated web browsers like, Google Chrome, Mozilla Firefox, Microsoft Edge, or Apple Safari

Internet Speed – It depends on the number of concurrent users and app type you are accessing. Specially report, data migration needs download 10Mbp/s and upload speed 3Mbp/s

SAP Fiori Launchpad URL: is SAP Launchpad Uniform Resource Locator - Web address used to locate and access resources on the internet. SAP has three clients, Development, test/Quality and Production client. Each client will have its own URL For example: Test/Quality System URL: Test/Quality System URL

Login username and Password: Enter your SAP credentials (username and password) provided by your administrator.

User Roles Setup - Depending on your role (administrator, end user, or developer), you may need specific access and role assignments in SAP’s user and authorization system (SAP Identity Authentication and Authorization services).

Create Sales Order

This shows the SAP S/4HANA Cloud system interface, where users can access various modules like Purchasing, Sourcing, Production, and Shipping. The highlighted magnifying glass icon at the top right is the global search function, allowing users to quickly find transactions, apps, or data across the SAP system.

This screenshot shows how to use the global search bar in SAP S/4HANA Cloud to locate the "Create Sales Orders" app (transaction VA01). Simply type your desired transaction or app name into the search field, and matching results will appear in a dropdown. Selecting "Create Sales Orders - VA01" let users quickly access the sales order creation process without navigating through multiple menu paths. This feature speeds up workflow and improves efficiency for SD users.

This screen is the initial entry page for creating a Sales Order (Order Type: OR).
Manually we need to enter Sales Organization (GEKE) along with its assigned Distribution Channel (10) and Division (10) to control pricing, products, and delivery flow.
After entering the order type, click to Continue to proceed.

This screen shows the header overview of the Sales Order.
Need to enter Sold-to Party and Ship-to Party based on the customer selected.
The Customer Reference is the customer-provided order or reference number used to identify their request or transaction and the Reference Date captures the date on which the customer raised the order.
Below, the Sales tab shows delivery date, billing indicators, payment terms, etc., which control how the order will be processed, credited, and posted.

In this section, the material being ordered (e.g., E2000024-204) is entered along with the Order Quantity, which represents how many units the customer needs.
The system automatically fetches item details like description, pricing date, plant (WH01), and first delivery date, based on the material ordered.
After reviewing all details, click Save and Sales Order gets created, which then triggers the next steps: Delivery → Goods Issue → Billing Document.

In the SAP sales order screen, item data for Galana-to-Delnet orders are entered manually, including product, quantity, and pricing details. The "Conditions" tab lets users review and adjust prices, discounts, and taxes according to negotiated terms. After confirming all data, the order is saved and processed for delivery and billing

Standard Sales Order gets Created 7000000482

After This the sales Order will go for the Approval In My Inbox

Outbound Delivery

This SAP screen shows the launchpad where a user searches for "My Sales Order" apps. The highlighted option "My Sales Order Due for Delivery" allows users to view and manage sales orders that are ready for shipping or fulfillment. It's used for tracking, editing criteria, and ensuring timely next steps in the sales order process for Galana-to-Delnet transactions.

This SAP screen displays the "Sales Orders, Fast Display" app, where users filter sales orders using shipping point/receiving plant (like WH01). Relevant criteria, such as shipping conditions and sales organization, can be added for focused order retrieval. The "Run" button (bottom-right) executes the search, showing all matching sales orders for delivery processing

This SAP screen provides a fast display of "Activities Due for Shipping - Sales Orders" and is crucial for Galana Energies’ logistics and sales operations. It allows users to monitor and manage outbound deliveries, ensuring that customer orders are shipped on time and in compliance with business requirements.

This screen is part of the Delivery process, where the company records the physical Issue of goods ordered by the customer.
Under the Picking tab, the system shows the material (E2000024-204) and the storage location (WH01) where the picking will be placed.
The user enters the Picked Quantity (5) to confirm how many units have actually been issued to the customer, along with selecting the correct Batch if applicable.
Once all order quantities are verified, click to Save completes the picking confirmation and prepares the document for Goods Issue posting.

Outbound Delivery Created 80000313

This screen is part of the SAP S/4HANA Cloud process for handling outbound deliveries when processing a sales order manually. The user enters the outbound delivery number, then clicks "Continue" to proceed.

Change Outbound Delivery

This screen is part of the SAP S/4HANA Cloud process for handling outbound deliveries when processing Manually. The user enters the outbound delivery number associated with the return, then clicks "Continue" to proceed. This step is crucial for referencing the original delivery during returns, so that goods receipt, inspection, and financial reconciliation can be correctly performed as part of the return order business process

Post Goods Issue(PGI)

This screen shows the details of the outbound delivery linked to your sales order in SAP S/4HANA Cloud. Here, users review item and quantity information before posting the goods issue, which records the physical issue of products. This step confirms the material has been issued, updates inventory, and triggers the subsequent phases in the business flow, similar to the goods issue in an outbound delivery.

This screen shows that the PGI has been done from the user side.

This screen shows the SAP S/4HANA Cloud "Document Flow" for outbound delivery processing, providing Galana Energies business users with complete visibility into the life cycle and transaction status of a delivery

Create Billing Document:

This SAP S/4HANA Cloud screen shows the Home Page and the process for accessing the “Create Billing Documents” app

This screen is from SAP S/4HANA Cloud and shows the "Create Billing Documents" transaction, which is used for managing billing due list items in the Sales and Distribution (SD) module.

The screen enables users to select SD documents (like deliveries and orders) that are due for billing, and then generate billing documents for them.

This screen shows the "Invoice" details in SAP S/4HANA Cloud under the

"Manage Billing Documents" function. It appears immediately after creating a billing document, allowing users to review and confirm invoice details before saving

This screen is used by billing or finance users to confirm and post invoices created from SD documents (deliveries or orders), officially recording the transaction in SAP S/4HANA Cloud for downstream processes such as accounts receivable, financial reporting, and customer communication

This screen shows the finalized, completed invoice details within the SAP S/4HANA Cloud "Manage Billing Documents" app. The status for the invoice is now "Completed," indicating it has already been posted to accounting.

After posting, users typically use this view to confirm details, generate invoice printouts for customers, or check transaction information as part of ongoing AR (accounts receivable) and customer service processes in SAP S/4HANA Cloud

This is the printed or PDF invoice output generated in SAP S/4HANA Cloud for invoice number 90000285. It summarizes the sales transaction between the company DW01 - delnet warehouse and its customer.