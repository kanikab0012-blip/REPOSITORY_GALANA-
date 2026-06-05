Table of Contents

1	Purpose	2

2	Prerequisites	3

2.1	System Access	3

2.2	Roles	3

2.3	Preliminary Steps	3

2.4	Required Organizational Units	4

2.5	Main Parameters for Data Creation	5

2.5.1	Business Partner Grouping and Number Ranges	5

2.5.2	Business Partner ID	5

2.5.3	Business Partner Function	6

2.5.4	Account Group	6

3	Overview Table	7

4	Test Procedures	8

4.1	Creating Customer Master Data - General Data	8

4.2	Creating Customer Master Data - Company Code Data	15

4.3	Creating Customer Master Data - Sales Area Data	20

Purpose

A customer is a business partner to which goods and services are sold and delivered. A business partner can be a customer and a supplier at the same time if, for example, your customer also supplies goods to you.

A customer master holds information about the customer such as their name, address, bank details, tax details and delivery and billing preferences. This customer information is used and stored in transactions such as sales orders, deliveries and invoices.

Some customer information is specific to a particular company (known as company code) or sales unit (known as sales area) within your organization.

Prerequisites

This section summarizes all the prerequisites for conducting the test in terms of systems, users, master data, organizational data, other test data and business conditions.

System Access

Roles

Create business roles using the following business role templates delivered by SAP and assign them to your individual test users.

Alternatively, if available, you can use the following spaces delivered by SAP. You create a space with pages containing predefined essential apps and assign it to the business role. You then assign this business role to your individual users.

For more information, refer to How to Create a Business Role from a Template in the product assistance for SAP S/4HANA Cloud Public Edition.

Preliminary Steps

Context

In this step, you assign the roles of chapter Roles to the test user that are necessary for data replication. Prior to executing this step ensure you have created and added the necessary roles for the specific object for data replication.

Required Organizational Units

Some segments of customer master data are dependent on the organizational units of the company, General (Central) Data does not depend on an organizational unit or the company code. The following table gives an overview of these different data segments and their relevant organizational units:

Main Parameters for Data Creation

In this section, we describe some basic parameters that influence the behavior of a master record and are always required to create a customer master data record:

Business Partner Grouping and Number Ranges

Business Partner Groupings determine the number ranges for the Business Partner IDs. You cannot change the assignment or IDs afterwards. If a Business Partner Grouping is assigned to an internal number range, you cannot enter the Business Partner ID manually. In this case, leave the field blank as the system automatically chooses a number from the assigned numeric number range.

The following business partner groupings and corresponding number ranges are defined for business partners (customers):

Business Partner Function

Business Partner Function

The business partner function determines the rights and responsibilities of each partner in a business transaction.

Examples for partner functions in Sales and Distribution are: Sold-to party, Ship-to party, and so on.

Account Group

Account Groups are leading control parameters for creating the ERP data segments of a customer master record. Currently, the supported account groups are

Overview Table

This scope item consists of several process steps that are listed in the following table:

Test Procedures

This section describes test procedures for each process step that belongs to this scope item.

Creating Customer Master Data - General Data

Test Administration

Customer project: Fill in the project-specific parts.

Purpose

The following procedure provides instructions for creating customer master data. Apps available to you are dependent upon your assigned role. Therefore, two options are provided.

Procedure: Option 1 - Maintain Business Partner

Follow this procedure when your user access presents you with the Maintain Business Partner (BP) app.

Procedure: Option 2 - Manage Customer Master Data

Follow this procedure when your user access presents you with the Manage Customer Master Data (F0850A) app.

Creating Customer Master Data - Company Code Data

Test Administration

Customer project: Fill in the project-specific parts.

Purpose

The following procedure provides instructions for creating customer master data. Apps available to you are dependent upon your assigned role. Therefore, two options are provided.

Prerequisite

You must complete the previous chapter, Creating Customer Master Data - General Data  [page ] , before you proceed with this chapter.

Follow the procedure after you have saved the General Data entries, as described in the previous chapter.

Procedure: Option 1 - Maintain Business Partner

Follow this procedure when your user access presents you with the Maintain Business Partner (BP) app.

Procedure: Option 2 - Manage Customer Master Data

Follow this procedure when your user access presents you with the Manage Customer Master Data (F0850A) app.

Creating Customer Master Data - Sales Area Data

Test Administration

Customer project: Fill in the project-specific parts.

Purpose

The following procedure provides instructions for creating customer master data. Apps available to you are dependent upon your assigned role. Therefore, two options are provided.

Prerequisite

You must complete the previous chapter, Creating Customer Master Data - General Data  [page ] , before you proceed with this chapter.

Follow the procedure after you have saved the General Data entries, as described in the previous chapter, on the Display Organization: Customer Name screen.

Procedure: Option 1 - Maintain Business Partner

Follow this procedure when your user access presents you with the Maintain Business Partner (BP) app.

Procedure: Option 2 - Manage Customer Master Data

Follow this procedure when your user access presents you with the Manage Customer Master Data (F0850A) app.

Typographic Conventions