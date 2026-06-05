SAP S/4HANA Public Cloud Implementation

END USER MANUAL

Credit Memo Processing

Submitted to
Galana Energies Limited

Prepared by
Yatendra Pratap Singh

Table of Contents

Objective

Credit Memo Overview

Accessing the Application

Creating Credit Memo Request

Reviewing and Releasing Credit Memo

Creating Billing Document for Credit Memo

Posting and Accounting Impact

System Integration and Business Effect

Objective

This document provides end users with a step-by-step guide to process Credit Memos in SAP S/4HANA Public Cloud. It explains how to create Credit Memo Requests, release them for billing, and post the Credit Memo document. The objective is to ensure correct revenue adjustments, proper tax postings, and complete audit traceability.

Credit Memo Overview

A Credit Memo is used when a customer needs to be reimbursed or credited for previously invoiced goods or services. This may occur due to pricing corrections, quantity discrepancies, or product returns. In SAP, the process begins with creating a Credit Memo Request (Order Type CR) and ends with posting the Credit Memo Billing Document (Type G2).

Accessing the Application

1. Navigate to SAP Fiori Launchpad.
2. In the search bar, type ‘VA01’.
3. Select the app ‘Create Sales Orders – VA01’.
📸 Refer to Screenshot 1: App Selection

Creating Credit Memo Request

Step 1 – Define Order Type
• Enter Order Type: CR (Credit Memo Request)
• Click on ‘Create with Reference’ to base the credit on a previous billing document, if applicable.
📸 Refer to Screenshot 2: Order Type Selection

Step 2 – Take reference from the invoice and click on copy

📸 Refer to Screenshot 3: Taking reference

Step 3 – Maintain Item Data and Remove Billing Block
• Material: WF-1001 – PMS
• Quantity as per adjustment requirement for credit
• Billing Block: Y8 – Check Credit Memo (remove billing block)
📸 Refer to Screenshot 4: Credit Memo Item Details

Step 4 – Save the Document
Once all data is entered, click ‘Save’.
System displays: ‘Credit Memo Request 60000037 has been saved.’
📸 Refer to Screenshot 5: Save Confirmation

Reviewing and Releasing Credit Memo

After creation, the Credit Memo Request moves to an approval workflow. The approver validates pricing, quantity, and adjustment justification. Once approved, the system allows billing document creation.

Creating Billing Document for Credit Memo

Step 5 – Access Billing App
• Navigate to ‘Create Billing Documents’ in Fiori Launchpad.
• The system lists all pending Credit Memo Requests.
• Select the Credit Memo Request (e.g., 60000037) and click ‘Create Billing Document’.
📸 Refer to Screenshot 6: Billing Document Selection

Step 6 – Review, Save and Post Billing Document
• Verify Billing Type: G2 – Credit Memo
• Confirm Net Value and Taxes
• First click save then click ‘Post Billing Document’
System confirms: ‘Billing Document 90000111 has been saved.’
📸 Refer to Screenshot 7: Credit Memo Billing Document Posting

Posting and Accounting Impact

When the Credit Memo Billing Document is posted, SAP automatically generates accounting entries to adjust revenue:
   Sales Revenue Account    Dr.
   Customer Account (A/R)   Cr.
   Tax Account (if applicable)   Dr./Cr.
This ensures that financial statements and tax reports reflect accurate corrected values.

System Integration and Business Effect

• Integration with FI: Ensures financial postings align with revenue adjustments.
• Integration with SD: Links Credit Memo with original billing and sales documents.
• Business Effect: Adjusts customer account balance and ensures accurate net sales.
• The entire process is traceable through Document Flow, ensuring transparency and compliance.