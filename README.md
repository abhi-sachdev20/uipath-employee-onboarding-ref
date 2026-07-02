# UiPath Employee Onboarding REFramework Project

This project is a UiPath REFramework-based automation created for UiPath certification preparation.

## Project Overview

The automation processes employee onboarding records using Orchestrator queues.

## Process Flow

1. Dispatcher reads employee data from Excel.
2. Dispatcher adds employee records to Orchestrator Queue.
3. Performer gets queue items one by one.
4. Performer validates employee details.
5. Valid records generate onboarding checklist files.
6. Invalid records are marked as Business Exceptions.
7. Unexpected failures are handled as System Exceptions.

## Technologies Used

- UiPath Studio
- REFramework
- UiPath Orchestrator Queues
- Excel Activities
- File System Activities
- Exception Handling
- Config.xlsx

## Queue Name

Employee_Onboarding_Queue

## REFramework Components Used

- Init
- Get Transaction Data
- Process Transaction
- Set Transaction Status
- End Process

## Business Rules

A transaction is marked as Business Exception if:

- Employee ID is missing
- First Name is missing
- Email address is invalid

## Output

For each valid employee, the bot creates:

```text
Output\EMP001_Rahul_Sharma\Onboarding_Checklist.txt