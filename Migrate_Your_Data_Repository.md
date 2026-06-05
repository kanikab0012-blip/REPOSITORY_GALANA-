---
client: Galana
solution: SAP S/4HANA Public Cloud
module: Data Migration
document_type: User_Manual
repository_type: AI_RAG_Knowledge_Repository
process_name: Migrate Your Data
---

# Migrate Your Data

## Objective
Load master data into SAP S/4HANA Public Cloud using Migration Cockpit.

## SAP App
Migration Cockpit

## Create Migration Project

### Step 1
Search:
Migrate Your Data

### Step 2
Create New Project

Example:
Customer Test

Migration Approach:
Migrate Data Using Staging Tables

### Step 3
Select Migration Object

Example:
Customer

### Step 4
Download Template

Prepare migration sheet offline.

### Step 5
Upload File

Use Upload File action.

### Step 6
Prepare Mapping Tasks

Execute mapping tasks for all required fields.

Example:
- Company Code
- Country
- Customer Group
- Sales Organization
- Distribution Channel

### Step 7
Maintain Values

Example shown:
Digital Payment Token = VISA

### Step 8
Validate

Run validation and resolve errors.

### Step 9
Migrate

Select Start Migration.

## Migration Lifecycle

Create Project → Select Object → Download Template → Upload File → Mapping → Validation → Migration

## Business Rules
- All mandatory mappings must be completed.
- Validation must be successful before migration.
- Errors must be resolved before migration execution.
