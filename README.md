# Oracle Pluggable Database Management Assignment II

## Student Information

Name: IGIRANEZA JEAN PAUL   
Student ID: 20251SEN292  
Course: Database Development with PL/SQL  
Database: Oracle Database 21c  

## Overview

This assignment was about working with Oracle Pluggable Databases.

I created a new PDB, created a user inside the PDB, created and deleted another temporary PDB, and checked my database using Oracle Enterprise Manager.

The main PDB I created is:

`IG_PDB_20251SEN292`

The user created inside the PDB is:

`IGIRANEZA_PLSQLAUCA_20251SEN292`

## Oracle Environment

I used the following tools:

- Oracle Database 21c Enterprise Edition
- Oracle SQL Developer
- Oracle Enterprise Manager Database Express
- Windows 64-bit

My Oracle database SID is:

`ORCL`

I connected to the database using SQL Developer with the SYS account and SYSDBA role.

## Task 1: Create a New Pluggable Database

In Task 1, I created a new Pluggable Database named:

`IG_PDB_20251SEN292`

First, I checked that I was connected to `CDB$ROOT`.

I then created the PDB using the `PDB$SEED` files as the source.

After creating the PDB, I checked the available PDBs and confirmed that my new PDB was created.

At first, the status of the new PDB was:

`MOUNTED`

This meant that the PDB existed but was not yet open for normal use.

I then opened the PDB and checked the status again.

The status changed to:

`READ WRITE`

This confirmed that the PDB was open and ready to use.

After that, I changed my current container from `CDB$ROOT` to:

`IG_PDB_20251SEN292`

I checked the current container and confirmed that I was working inside my new PDB.

I also checked that the required user existed inside the PDB.

The username is:

`IGIRANEZA_PLSQLAUCA_20251SEN292`


## Task 2: Create and Delete a Temporary PDB

In Task 2, I created a temporary PDB named:

`IG_TO_DELETE_PDB_20251SEN292`

After creating it, I used the PDB list to confirm that it existed.

The temporary PDB was shown with the status:

`MOUNTED`

After confirming that the PDB existed, I deleted it including its data files.

I checked the PDB list again and confirmed that:

`IG_TO_DELETE_PDB_20251SEN292`

was no longer available.

This confirmed that the temporary PDB was deleted successfully.

## Task 3: Oracle Enterprise Manager

For Task 3, I opened Oracle Enterprise Manager Database Express in my browser.

I connected to my Oracle database and opened the Database Home dashboard.

The dashboard showed my Oracle 21c environment.

It also showed that the database is a CDB with two PDBs.

The Containers section showed:

- `CDB$ROOT`
- `ORCLPDB`
- `IG_PDB_20251SEN292`

The username `SYS` was also visible on the dashboard.

This confirmed that Oracle Enterprise Manager was working correctly and that my PDB was available in the Oracle environment.

## Challenges Faced

I faced some challenges while doing the assignment.

### SQL Developer Setup

At first, I had difficulty finding the SQL Developer application after extracting the files.

I later found the correct SQL Developer package and opened the application successfully.

### Database Connection

I had to find my Oracle SID before connecting SQL Developer to the database.

I checked the Oracle services on Windows and found:

`OracleServiceORCL`

This helped me know that my SID was:

`ORCL`

I then connected successfully using the SYS account with the SYSDBA role.

### PDB File Location

I had to understand how `FILE_NAME_CONVERT` works.

I found that my Oracle data files were stored inside:

`C:\App\oradata\ORCL`

I used the `pdbseed` folder as the source and created a separate folder for my new PDB.

### Oracle Enterprise Manager

When I opened Oracle Enterprise Manager, the browser showed a privacy warning because the connection used a local security certificate.

Since the website was running on `localhost`, I continued to the Oracle Enterprise Manager page and accessed the dashboard successfully.

### Command Errors

While creating the temporary PDB, I had some command errors because of how the SQL statements were executed.

I corrected the command and successfully created the temporary PDB.

I then confirmed that it existed before deleting it.

## Screenshots

The screenshots for the assignment are stored in the following folders:

### PDB Creation

`screenshots/pdb_creation/`

This folder contains evidence for:

- PDB creation
- PDB open state
- User verification

### PDB Deletion

`screenshots/pdb_deletion/`

This folder contains evidence for:

- Temporary PDB creation
- Temporary PDB verification
- Temporary PDB deletion

### Oracle Enterprise Manager

`screenshots/oem_dashboard/`

This folder contains the Oracle Enterprise Manager dashboard screenshot.

## Integrity Statement

I performed the Oracle practical steps and captured the screenshots from my own Oracle environment. I used learning support to understand some errors and assignment requirements, but I personally carried out the database operations shown in the screenshots.

## Submission Details

Repository Link: https://github.com/igiranezajeanpaul/oracle_pdb_ass_II_20251sen292_igiraneza.git

PDB Name Created: IG_PDB_20251SEN292

Issues Encountered: Yes
