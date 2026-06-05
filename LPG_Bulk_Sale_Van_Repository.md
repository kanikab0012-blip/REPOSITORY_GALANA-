PROJECT GALANA

SAP S/4 HANA PUBLIC CLOUD

User Training Manual

Module: Sales and Distribution

Process: Sales Order for LPG Bulk/ Van Sale

November 14, 2025

Version 1.0

ABOUT THIS MANUAL

This manual provides information and specific instructions on all the Return Order Process activity steps with the implication of vital processes in standard SAP S/4HANA system. You will see how each of the views is created, its obligatory data, optional fields, and how its creation reflects in the system.

The manual is intended to serve both as a training manual and a reference.

Icons Used

The following icons are used.

OVERVIEW

Bulk LPG sales in SAP SD involve specialized handling of material units, regulatory compliance, and process integration with inventory management. Bulk LPG is typically stored and sold in metric tons (MTO), liters, or kilograms depending on customer requirements and transaction type.

Target Audience

This manual shall primarily be used by.

Stores and Finance team

Management and staff members in all other departments may carry out Bulk/Van  Sales Order-related activities.

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

INTRODUCTION- Bulk LPG/Van Sales

Galana Energies, a leading company in Kenya, handles Bulk LPG sales as part of its commercial energy solutions. Their business model focuses on supplying high-quality LPG in bulk to commercial customers, leveraging a structured SAP SD process configured for bulk quantities measured mostly in metric tons (MTO) and liters. They manage LPG sales and distribution with regulatory compliance and safety as core priorities, reflecting their emphasis on safe, efficient, and reliable energy delivery.

In SAP SD for Galana Energies:

Bulk LPG is sold primarily in metric tons with supporting conversion to liters or kilograms, using standardized conversion factors.

Sales orders and pricing are tailored for bulk transactions, serving industrial and commercial clients.

Integration with inventory management ensures tracking of LPG in bulk tanks and cylinder management for cylinder refills and returns.

Safety documentation and regulatory compliance management are embedded in the process, matching Galana Energies' commitment to safety and quality.

This approach supports their mission of delivering personalized, efficient service with a strong customer focus, operational safety, and environmental responsibility.

LOGIN TO SAP S/4 HANA PUBLIC CLOUD TENANT

Web Browser- Make sure you have updated web browsers like, Google Chrome, Mozilla Firefox, Microsoft Edge, or Apple Safari

Internet Speed – It depends on the number of concurrent users and app types you are accessing. Specially report, data migration needs download 10Mbp/s and upload speed 3Mbp/s

SAP Fiori Launchpad URL: SAP Launchpad Uniform Resource Locator - Web address used to locate and access resources on the internet. SAP has three clients, Development, Test/Quality and Production client. Each client will have its own URL For example: Test/Quality System URL: Test/Quality System URL

Login username and Password: Enter your SAP credentials (username and password) provided by your administrator.

User Roles Setup - Depending on your role (administrator, end user, or developer), you may need specific access and role assignments in SAP’s user and authorization system (SAP Identity Authentication and Authorization services).

Create purchase Order

In this screenshot, the SAP S/4HANA Cloud system is displayed where the user searches for the "Create Purchase Order - Advanced" app, which is critical for initiating the Stock Transport Order (STO) process from an SD (Sales and Distribution) perspective at Galana Energies Pvt Ltd. The user begins by selecting this app to create an internal purchase order, which is the first step for moving inventory from one plant (supplying) to another (receiving) within the organization.

This screenshot shows the creation of a Stock Transport Order (STO) in SAP S/4HANA Cloud for Galana Energies Pvt Ltd. The "Stock Transfer Order" document type is selected, and crucial organizational details are filled: the supplying plant is HL01 Lake Oil Terminal, and the purchasing organization, group, and company code all correspond to Galana Energies Ltd

This screenshot shows the item details for a Stock Transport Order (STO) in SAP S/4HANA Cloud, focusing on the material, quantity, and plant information for Galana Energies Pvt Ltd. The material code (BOG-1001), bulk LPG description, and quantity (10 T) are specified, indicating what and how much is being transferred to Transporters created as a specific plant and s locs created as specific vans to those plants.

Outbound Delivery

This screenshot shows the SAP S/4HANA Cloud home page where the user searches for "My Purchase Orders - Due for Delivery". This app allows users at Galana Energies Pvt Ltd to monitor the status of their internal purchase orders, specifically those pending delivery as part of the Stock Transport Order (STO) process.

This screenshot displays the "Purchase Orders, Fast Display" view in SAP S/4HANA Cloud, used for managing Stock Transport Orders (STOs) at Galana Energies Pvt Ltd. The user enters the specific purchase document number (4700000022) and the relevant shipping/receiving plant (HL01), along with date criteria to filter the required STO for review.​

This step allows users to quickly verify the details and status of the STO. By clicking "Run," they can access all related logistics data—ensuring that the goods movement and internal distribution are tracked and managed seamlessly within the SD business process. It aids in monitoring order fulfillment and coordinating supply chain operations between company locations

This screenshot displays the "Activities Due for Shipping" section in SAP S/4HANA Cloud for Galana Energies Pvt Ltd, showing purchase orders ready for goods issue and delivery creation in the Stock Transport Order (STO) process. The user selects the relevant STO record with a checkbox on the left, indicating which item will be processed next in shipping.​

The list view provides details such as ship-to location (VG01), original document number, and other logistics fields. After selection, users can continue by clicking the "Background" button, which executes the delivery creation step—often processed in the background for efficiency. This part of the SD business process ensures that the planned stock transfer moves into physical shipment, facilitating operational flow between company locations.

This screenshot shows the "Activities Due for Shipping" function in SAP S/4HANA Cloud, focused on the next step for Stock Transport Order (STO) processing at Galana Energies Pvt Ltd. The user selects orders ready for goods issue using the checkbox and can view details in a hierarchical display for better order organization.​

After selecting the relevant item, clicking the "Background" button initiates delivery creation for the STO in the system. This step is essential for executing the internal movement between plants, as it generates the delivery document necessary for physical shipment. The process supports efficient and trackable logistics in the SD workflow, leading to successful completion of the STO business cycle

This screenshot displays the final view for "Activities Due for Shipping" in SAP S/4HANA Cloud, specifically highlighting the Stock Transport Order (STO) number (4700000022) for Galana Energies Pvt Ltd. The table confirms the relevant STO is selected for further processing, listing key details such as supplying plant (HL01), purchasing organization (GEKE), and delivery category.​

This step allows users to review and verify STO details before executing the goods issue or delivery creation. It ensures all shipment data aligns with business requirements, supporting controlled and audited stock transfers between plants. This review and confirmation step is critical in the SD business process to guarantee inventory accuracy and compliance with internal logistics procedures.

This screenshot confirms the successful delivery creation for the Stock Transport Order (STO) in SAP S/4HANA Cloud for Galana Energies Pvt Ltd. The table shows the original STO document number (4700000022) alongside the newly generated delivery document (80000251), which is essential for proceeding with the goods issue and shipment steps.​

This step completes the logistics preparation for the internal transfer, linking the STO to the corresponding delivery record for tracking and further SD processing. Having the delivery document number allows relevant teams to monitor, process, and post goods movements, ultimately ensuring efficient material flow and inventory accuracy between company plants.​

Outbound Delivery :

This screenshot displays the "Replenishment Delivery Change" screen in SAP S/4HANA Cloud, where Galana Energies Pvt Ltd processes the delivery linked with the Stock Transport Order (STO). Users can switch to edit mode (“Display <-> Change”), confirm picked quantity, batch number, supply plant (HL01), storage location, and view status in the "Picking" tab.​

To complete the internal goods movement, users click "Post Goods Issue" after verifying all picking details. This action records the transfer of stock out of the supplying plant, signifying the physical movement of goods within the company. Finally, clicking "Save" finalizes the process, updating inventory and enabling the receiving plant to proceed with goods receipt, thereby closing the STO business cycle.

This screenshot confirms the successful posting of a goods issue in SAP S/4HANA Cloud for Galana Energies Pvt Ltd.'s Stock Transport Order (STO) process. The table links the delivery document (80000251) to the originally created STO and shows all related shipping details.​

At the bottom, a notification verifies that “Replenishment Dlv. 80000251 saved, material document 4900000283 created,” which means the actual inventory movement has been posted from the supplying plant. This step finalizes the internal material transfer; the goods are now officially recorded as issued and can be received by the target location, ensuring traceable and compliant stock movement as required by SD business processes.​

Post Goods Movement

This screenshot shows the SAP S/4HANA Cloud home page, where the user searches for the "Post Goods Movement" app, a key step in the Stock Transport Order (STO) process for Galana Energies Pvt Ltd. After completing delivery creation and picking in previous steps, this function allows users to record goods issue or receipt transactions, updating inventory according to actual stock movements.​

Accessing this app ensures that all material movements—such as transferring stock from one plant to another—are reflected in system inventory. This is critical for maintaining accurate stock levels, ensuring compliance, and supporting transparent operations in the SD business process.​

This screenshot shows the "Goods Receipt Outbound Delivery" screen in SAP S/4HANA Cloud for Galana Energies Pvt Ltd, where the receiving plant completes the final step of the Stock Transport Order (STO) process. The outbound delivery number (80000251) is entered, along with the relevant goods receipt movement type (101), to confirm the actual receipt of transferred inventory.​

The system captures the receipt date, posting date, and other essential logistics information for compliance and record-keeping. Completing this step updates the inventory in the receiving plant, finalizing the internal stock movement initiated by the STO and ensuring proper tracking and reconciliation within the SD and MM modules

This screenshot displays the "Where" tab in the goods receipt process for outbound delivery in SAP S/4HANA Cloud, finalizing the Stock Transport Order (STO) for Galana Energies Pvt Ltd. The movement type (101) and status "GR stock in transit" indicate that goods are being received from internal transfer and will be posted into the receiving plant and storage location (VG01).​

After reviewing plant, storage location, and relevant logistics fields, marking the "Item OK" checkbox confirms the line item's readiness for posting. Clicking "Post" executes the goods receipt, updating inventory at the receiving plant and closing the STO cycle, ensuring compliance, visibility, and efficient internal logistics

This screenshot confirms the completion of the goods receipt process in SAP S/4HANA Cloud for Galana Energies Pvt Ltd’s Stock Transport Order (STO) workflow. The system displays a message at the bottom: "Material document 5000000118 posted," indicating that inventory for the transferred material has been successfully received and recorded at the destination plant.​

This final step closes the internal transfer cycle, ensuring all transactional data and inventory positions are updated. It reflects the completion of SD process requirements, providing full traceability and compliance for intra-company stock movements.​

Accessing the Application:

1. Navigate to SAP Launchpad.
2. In the search bar, type 'Create Sales Orders'.
3. Select the application 'Create Sales Orders - VA01'.

After this sales order and delivery are created from transporter as a plant and delivery note output is provided as “delivery instruction” to customer location.

Creating Sales Order:

“Create Sales Orders" app (VA01). Type "create sales order" into the search and select the highlighted result to begin entering a new sales order. This shortcut helps users efficiently start the sales order process without navigating multiple menus. It improves workflow speed and user convenience in daily business operations.

This screen captures the entry of key organizational data when creating a sales order, including Order Type, Sales Organization, Distribution Channel, and Division. These selections define the basic structure and rules for the sales transaction, ensuring the order is routed correctly within the company’s internal organization. Completing this step is necessary to guide the order to the right workflow, pricing, and business process for the customer’s requirements. Click "Continue" to advance with sales order creation after confirming all fields are set properly.

This screen is used by users to create a standard sales order in SAP S/4HANA Cloud by entering and reviewing all essential order details. Below are explanations for important fields as seen on the screen:

Sold-to-Party / Ship-to-Party: Identify the customer placing the order and the customer receiving the goods, which may be the same or different.

Cust. Reference / Cust. Ref. Date: Capture the customer’s purchase order number and purchase order date for tracking and compliance.

Delivery Plant: Indicates the plant/location from which goods will be delivered.​

Pyt Terms (Payment Terms): Specifies the conditions under which the customer will pay, such as immediate payment or net 30 days.

Incoterms: Defines the contractual terms of delivery relevant to shipping and risk transfer, e.g., CIF (Cost, Insurance, and Freight).

Req. Deliv. Date: The requested date by which the customer wants the goods delivered.

In this SAP sales order screen, double-clicking on the material number (in this case, "BOG-1001") in the "All Items" section will open the item detail’s view. From there, you can navigate to the "Conditions" tab to view and edit pricing, discounts, and other item-specific condition records. This step allows users to manage the pricing details for each material in the order.

The "Conditions" tab in the SAP sales order item details screen displays the pricing conditions that determine the final price of the material in the order. Each row represents a pricing element, such as base price, discounts, surcharges, and taxes, defined by different "Condition Types" (like ZPR0 for price, ZGRS for gross price, TTX1 for tax, DC01 for cash discount).

Condition Types: Each pricing element (e.g., ZPR0 for price, TTX1 for tax) represents a specific calculation or charge applied to the item.

Amount: Shows the value for the condition, which could be a price, discount, surcharge, or tax

Gross Price/Gross Amount: The initial amount before any deductions.

Discounts/Surcharges: Negative or positive amounts that adjust the base price according to business rules or agreements.

Output Tax: Represents applicable tax amounts calculated on the item.

Net Amount/Total Amount: The net price after applying all relevant discounts, surcharges, and taxes, providing the final payable amount for the item.

This screen confirms the successful creation of a standard sales order, as seen by the message "Standard Order 7000000381 has been saved" at the bottom. Saving the order completes the initial sales process and generates a unique order number for tracking and further processing. This step is essential because it officially records the customer’s request in the system and enables downstream activities like delivery and billing to proceed.

Create Outbound Delivery:

Accessing "Create Outbound Delivery – with Order Reference" also enables users to filter and prioritize sales orders using personalized criteria (such as customer, product group, or delivery urgency). This helps streamline daily tasks, making it easier for team members to follow up with logistics, plan shipments, and meet promised delivery dates. The main reason for this step is to efficiently manage pending deliveries and ensure a smooth order-to-cash process.

This SAP S/4HANA Cloud screen is for creating outbound delivery with reference to a specific sales order. Users enter the shipping point (VG01) and the relevant order number (7000000381), then confirm the selection date. After the required fields are filled, clicking "Continue" proceeds to the delivery creation, ensuring the logistics process is tied to the chosen sales order and shipping location.

After this sales order and delivery are created from transporter as a plant and delivery note output is provided as “delivery instruction” to customer location.

When transporter confirms how much quantity they have actually delivery to customer, picking quantity will be updated and customer will be billed a per actual quantity.

This screen in SAP S/4HANA Cloud shows the creation of an outbound delivery document. Users can review sales order details like the ship-to party, delivery date, and planned goods issue date. The "Item Overview" tab displays all materials included in the delivery along with their quantities and descriptions. This view ensures the correct items and quantities are prepared for shipping before posting the goods issue.

Click on Picking for entering picked quantity.

This "Picking" screen in SAP S/4HANA Cloud is part of the outbound delivery process. It displays the warehouse pick details, including the delivery quantity, picked quantity, and batch number for each item. Here, the system shows that 10 KG of material BOG-1001 has been picked from batch 2560000041. Users use this screen to confirm correct quantities and batches before proceeding to the next delivery step.

This SAP S/4HANA Cloud screen confirms the successful creation and saving of an outbound delivery document. It shows the shipping point (VG01), linked sales order number (7000000381), and includes a notification at the bottom indicating "Outbound Delivery 80000238 has been saved." This message assures users that the outbound delivery process is completed, and the record is now available in the system for further processing.

Posting Goods Issue (PGI):

PGI stands for Post Goods Issue in SAP, and it is a crucial step in the outbound delivery process. PGI is performed after picking is completed; when executed, it officially records that goods have physically left the warehouse and are handed over to the customer or carrier. This step reduces inventory in the system, posts relevant accounting entries (like cost of goods sold), and transfers ownership of the goods from the company to the customer. PGI is necessary because it updates inventory, confirms the delivery is complete, and is a prerequisite for billing the customer for the shipped goods.

This screen in SAP S/4HANA Cloud is used to select and open an outbound delivery for further processing. By entering the outbound delivery number (80000238), users can search for and display delivery details. After selecting the desired delivery document from the search results, clicking "Continue" allows the user to proceed, for actions such as Post Goods Issue (PGI). This step is essential for updating the delivery’s status and moving forward in the shipping process.

This screen in SAP S/4HANA Cloud is used to select and open an outbound delivery for further processing. By entering the outbound delivery number (80000238), users can search for and display delivery details. After selecting the desired delivery document from the search results, clicking "SAVE" allows the user to proceed, for actions such as Post Goods Issue (PGI). This step is essential for updating the delivery’s status and moving forward in the shipping process.

This SAP S/4HANA Cloud screen confirms the successful execution of Post Goods Issue (PGI) for an outbound delivery. The system displays a message: "Outbound Delivery 80000238 saved, material document 4900000260 created," indicating that the goods have officially left the warehouse and the corresponding material document has been generated. This step finalizes the delivery process, updates inventory and triggers financial accounting entries in the system.

Billing and Financial Impact:

This screen demonstrates how to quickly access the "Create Billing Documents" app in SAP S/4HANA Cloud using the search function. This step is essential after the outbound delivery process because it allows users to generate billing documents directly linked to shipments and customer orders. Creating billing documents is critical for recording sales, sending invoices, and initiating payment collection from customers. The search shortcut streamlines workflow, making it easier to move efficiently from logistics completion to financial processing in the sales cycle.

This SAP S/4HANA Cloud screen is used to create a billing document linked to the outbound delivery process. The user selects the delivery document (80000238) from the list of items to be processed for billing. Status columns indicate the document's progress, such as being fully invoiced. After confirming the details, the user can click "Save" to generate the corresponding billing document and complete the sales process flow.

This SAP S/4HANA Cloud screen displays the creation of a sales invoice after goods are delivered and PGI is completed. The invoice is generated for material BOG-1001 with details like quantity, net value, and tax amount shown. The system uses these values to bill the customer, based on the delivery and sales order. After verifying the details, the user clicks "Save" to finalize and post the invoice, completing the sales and billing process.

This SAP S/4HANA Cloud screen confirms that a billing document has been successfully created and saved. The message at the bottom indicates "Document 90000213 has been saved," signaling the completion of the invoice generation process. This step finalizes the billing for the delivery and records the transaction for accounting and customer invoicing. It marks the end of the order-to-cash process in the SAP sales cycle.