SAP S4 HANA PUBLIC CLOUD

END USER MANUAL

Customer Master and Account Group

Submitted to

Galana Energies Limited

Prepared by

Yatendra Pratap Singh

Objective

The objective of this document is to provide users with a clear understanding of how to manage and use the Customer Master in SAP Public Cloud. It aims to help users create, maintain, and utilize customer data effectively to support sales, billing, and reporting processes across the organization.

Customer Master and Account Groups

ThThe Customer Master in SAP Public Cloud is a central repository that stores all key information about a customer required for processing transactions in Sales and Distribution (SD), Financial Accounting (FI), and other related modules. This ensures consistent and accurate customer data across the system.

The Customer Master is structured into three main views:

General Data: Common information such as customer name, address, communication details, and tax information shared across company codes and sales areas.

Company Code Data: Accounting-related details like reconciliation accounts, payment terms, and dunning procedures specific to a company code.

Sales Area Data: Sales-specific information such as sales office, shipping conditions, pricing procedure, and delivery details.

Customer Account Groups

Account Groups in SAP Public Cloud are used to classify customers based on their business relationship and control how customer master data is maintained. They define:

The number range assigned for customer codes.

Which fields are required, optional, or hidden during master data creation.

The partner functions that can be assigned (e.g., Sold-to Party, Ship-to Party, Bill-to Party, Payer).

Creating New Customer Master

1. We use App Maintain Customer Master

2. Click on person, organization or group as per customer classification to create customer master.

3. First we create the customer in general role, account group is the most important key that determines number range and fields status. (Once selected and saved it cannot be changed)

4. Fill in all the address related and communication details.

5. Under the identification tab fill the oracle customer number and pin number for customer.

Extending customer to Finance role

Go to change mode in business partner and click on roles to extend customer to FLCU01 financial customer master role. Go to “company code” tab in the menu. After that fill in company code for which customer needs to be extended. Fill in the details recon account and payment term and click on save to generate customer in FI.

Extending customer to Sales role

Objective

This section explains how to extend an existing Business Partner to the FLCU00 (Customer – Sales Area) role in SAP S/4HANA Public Cloud. This role maintains customer data relevant to Sales, Shipping, Billing, and Partner Functions.

Step 1 – Access the FLCU00 Role

Go to Change Mode for the respective Business Partner.

From the Roles dropdown, select or add FLCU00 – Customer (Sales Area).

Under the Sales Area Data section, fill in all relevant details as per the business requirements.

Step 2 – Maintain Sales Area Details

📸 Refer to Screenshot 1: Sales Area

Sales Organization (GEKE) – Defines the legal and administrative sales entity (e.g., Galana Energies Ltd.).

Distribution Channel (80) – Indicates the route through which goods reach the customer (e.g., Retail).

Division (10) – Classifies the product line or business segment (e.g., White Fuels).

Step 3 – Orders Tab

📸 Refer to Screenshot 2: Orders Tab

Customer Group (30) – Groups customers with similar traits for reporting or pricing (e.g., Tourism & Hospitality).

Sales Office (HL01) – Represents the sales location handling customer orders (e.g., Lake Oil Terminal).

Sales Group (NR0) – Identifies the sales team or depot managing the customer (e.g., Nairobi Depot).

Currency (KES) – Default currency for transactions (e.g., Kenyan Shilling).

Customer Pricing Procedure (Z1) – Defines the pricing method assigned to the customer (e.g., Local Fuels).

Price List (Z1) – Indicates the applicable price list category (e.g., Local Fuels).

Step 4 – Shipping Tab

📸 Refer to Screenshot 3: Shipping Tab

Shipping Condition (01) – Standard shipping process used for deliveries.

Partial Delivery Controls – Used to define how deliveries are split or restricted:

Complete Delivery – Forces full order delivery in one shipment.

Partial Delivery per Item – Allows item-based delivery splitting.

Under-/Over-Delivery Tolerance – Defines permissible percentage deviation in delivered quantity.

💡 Tip: If you need to assign multiple Ship-To Parties for one Sold-To Party, they can be maintained under the Partner Functions tab along with corresponding Bill-To and Payer details.

Step 5 – Billing Tab

📸 Refer to Screenshot 4: Billing Tab

Incoterms (DAF) – Specifies delivery terms (e.g., Delivered at Frontier).

Incoterms Location 1 (Nairobi) – Indicates the delivery location under Incoterms (e.g., Nairobi).

Terms of Payment (0001) – Defines the payment timeline (e.g., Pay Immediately without Deduction).

Account Assignment Group for Customer (01) – Used to determine G/L account postings (e.g., Local).

📸 Refer to Screenshot 5: Output Tax Section

Country/Region (KE) – Specifies customer’s tax country (e.g., Kenya).

Tax Code (TTX1) – Defines applicable tax classification (e.g., Output Tax).

Tax Classification (1) – Indicates the customer’s tax liability (e.g., Liable for Taxes).

Step 6 – Status Tab

📸 Refer to Screenshot 6: Status Tab

Sales Blocks – Control order processing restrictions:

Sales Order Block – Prevents order creation.

Delivery Block – Stops delivery creation.

Billing Block – Prevents invoice generation.

Deletion Blocks – Restricts the deletion of the sales area assignment until cleared.

🔖 Note: You can use the Services for Object → Create Attachment option to upload supporting customer documents (e.g., tax certificate, registration proof).

Step 7 – Save the Customer

After maintaining all mandatory data, click Save to complete the customer extension under FLCU00.
The customer is now ready for Sales Order, Delivery, and Billing processing in the defined Sales Area.

Customer Reports

After extending the Business Partner to FLCU00 (Sales Area) and FLCU01 (Financial Accounting) roles, users can verify customer data through standard SAP Public Cloud applications.

Manage Business Partner

Fiori App ID: F3163
Navigation Path: SAP Fiori Launchpad → Manage Business Partner

📸 Refer to Screenshot: Manage Business Partner

This app is used to display, search, and verify Business Partners created in the system. It allows filtering and reviewing of general, company code, and sales area data.

Key Filters:

Business Partner Number

Name / City / Country / Region

Role (e.g., FLCU00 or FLCU01)

Editing Status (All / Active / Blocked / Marked for Deletion)

Purpose:

To confirm that a Business Partner has been successfully created.

To check assigned roles and address details.

To ensure completeness before extending to other roles.

Display Customer List

Fiori App ID: F1905
Navigation Path: SAP Fiori Launchpad → Display Customer List

📸 Refer to Screenshot: Display Customer List

This report provides a Sales Organization–wise overview of all customers extended under the Sales Area (FLCU00).

Available Filters:

Company Code / Sales Organization

Customer Number

City

Clerk Abbreviation

Dunning Procedure

Financial Payment Terms

Displayed Data:

Company Code – Customer’s legal entity.

Customer Number – Auto-generated BP/Customer number.

Name of Customer – Business or trade name.

City / Phone / E-mail – Contact and communication details.

Purpose:

To validate that customer extensions are correctly linked to the company code or sales area.

To confirm financial and contact data accuracy.

To provide a consolidated customer view for reporting or audit.

✅ Summary:

These reports are essential checkpoints to confirm customer master completeness before starting Order-to-Cash transactions.

-----------------------------------------------End of Document ---------------------------------------------------------