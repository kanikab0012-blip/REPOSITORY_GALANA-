SAP S/4HANA Public Cloud Implementation

END USER MANUAL

Debit Memo Request Processing

Submitted to
Galana Energies Limited

Prepared by
Yatendra Pratap Singh

Table of Contents

Objective

Debit Memo Overview

Accessing the Application

Creating Debit Memo Request

Entering Organizational and Reference Data

Maintaining Item and Pricing Details

Billing Document Creation

Posting and Accounting Impact

System Integration and Business Effect

Objective

This document provides step-by-step guidance on creating and processing Debit Memo Requests in SAP S/4HANA Public Cloud. It details the process for creating debit memos referencing existing billing documents, updating item details, and posting the billing document. The aim is to ensure accuracy in revenue adjustments and customer account management.

Debit Memo Overview

A Debit Memo is used to charge a customer for an additional amount after the original invoice has been issued. Common reasons include price differences, unbilled quantities, or additional service charges. In SAP, the process starts with a Debit Memo Request (Order Type DR) and concludes with posting a Debit Memo Billing Document (Type L2).

Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. In the search bar, type ‘VA01’.
3. Select the app ‘Create Sales Orders – VA01’.
📸 Refer to Screenshot 1: App Selection

Creating Debit Memo Request

Step 1 – Select Order Type
• Enter Order Type: DR (Debit Memo Request)
• Click on ‘Create with Reference’ to copy data from an existing billing document.
📸 Refer to Screenshot 2: Order Type Selection

Step 2 – Create with Reference
• Select the ‘BillDoc’ tab.
• Enter Billing Document number (e.g., 900000097).
• Click ‘Copy’ to bring forward details from the reference invoice.
📸 Refer to Screenshot 3: Create with Reference

Verifying Organizational and Remove billing block

Step 3 – Organizational Data copied from reference billing
• Sales Organization: GEKE – Galana Energies Ltd.
• Distribution Channel: 10 – B2B Local
• Division: 20 – Lubricants
• Sold-to Party: 1100000000 – GE Athi River
• Ship-to Party: 1100000000 – GE Athi River

• Billing Block: Y9 – Check Debit Memo (remove)
📸 Refer to Screenshot 4

Maintaining Item and Pricing Details

Step 4 – Update Item and Pricing Details
• Material: E200024-204 – ENOC Vulcan 770X 15W/140-4x5 Lit
• Target Quantity: 10 PAC
• Order Reason: 001 – Sales Call (mandatory for audit tracking)(select a it is mandatory)
📸 Refer to Screenshot 5 and 6: Item Overview and Order Reason

Step 5 – Save the Document
Click ‘Save’ to create the Debit Memo Request.
System displays confirmation: ‘Debit Memo Request 70000028 has been saved.’
📸 Refer to Screenshot 7: Save Confirmation

Billing Document Creation

Step 6 – Create Billing Document
• Navigate to ‘Create Billing Documents’ app.
• Select the Debit Memo Request (e.g., 70000028) from the list.
• Click ‘Create Billing Document’.
📸 Refer to Screenshot 8: Billing Due List Selection

Step 7 – Review and Post Billing Document
• Billing Type: L2 – Debit Memo
• Billing Date: 11.11.2025
• Review details under General Information and Pricing Data.
• Click ‘Post Billing Document’ to complete posting.
📸 Refer to Screenshot 9: Post Billing Document Confirmation

Posting and Accounting Impact

Upon posting the Debit Memo Billing Document, the system automatically generates accounting entries to increase revenue:
   Customer Account (A/R)     Dr.
   Sales Revenue Account      Cr.
   Tax Payable (if applicable)   Cr.
This ensures financial accuracy and compliance with accounting standards.

System Integration and Business Effect

• FI Integration: Updates customer balances and revenue accounts.
• SD Integration: Maintains full linkage between the original billing and debit memo.
• Business Impact: Increases customer receivable and corrects revenue based on additional charges.
• The process is traceable through document flow for complete transparency.