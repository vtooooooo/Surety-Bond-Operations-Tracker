# Surety Bond Operations Tracker

**Tools:** Microsoft Excel (Advanced) | Formulas & Functions | Data Validation | Conditional Formatting | Dashboard Design

---

## Project Overview

This project simulates the real-world bond processing workflow used by a Surety Underwriting Technical Assistant. It demonstrates proficiency in Excel-based queue management, operational reporting, data accuracy checking, and shared inbox tracking — core responsibilities of surety operations roles at firms like Chubb.

The workbook was built entirely from scratch using synthetic data representing 20 active bond requests across multiple bond types, processors, principals, and obligees.

---

## Business Problem

Surety underwriting teams process high volumes of bond requests daily — bid bonds, final bonds, riders, consents, cancellations, and premium adjustments — while managing strict deadlines, renewal billing accuracy, and shared email queues. Without a structured tracking system, items can be missed, SLAs breached, and billing errors go undetected.

This tracker addresses those operational challenges through a centralized, formula-driven Excel workbook.

---

## Workbook Structure

### 1. Bond Queue Tracker (Main Log)
- Tracks 20 active bonds across the full lifecycle: New → In Progress → Pending Info → Completed
- Bond types covered: Bid Bond, Final Bond, Rider, Consent, Release, Cancellation, Premium Adjustment
- Dropdown data validation for Bond Type, Status, and Priority fields
- Auto-calculated **Days Remaining** using `TODAY()` — updates in real time
- Auto-calculated **SLA Met** flag (✔ Yes / ✘ No) triggered upon entering a Completion Date
- Color-coded rows by status using conditional formatting (green = completed, red = overdue, yellow = pending)

### 2. Summary Dashboard
- Live KPI cards: Total Bonds in Queue, Open/Active, and Completed — all formula-driven
- **Status Breakdown Table:** Count, percentage of queue, average days remaining, and total premium by status
- **Processor Workload Table:** Total assigned, open, completed, overdue, and completion rate per processor
- **Bond Type Volume Table:** Count, total bond amount, average premium, and portfolio percentage by bond type
- **High-Priority Alert Table:** Auto-flags Overdue and High-priority bonds requiring immediate attention

### 3. Renewal Bill Checker
- Simulates the renewal billing QA process — a direct responsibility from the Technical Assistant role
- Enter bill figures in yellow input cells; system instantly compares to master policy data
- Green = Match, Red = Discrepancy requiring review
- Intentional discrepancies included to demonstrate the QA workflow (e.g., premium overbilling, bond amount errors)
- Summary row tallies total master premium vs. billed premium and counts discrepancies

### 4. Email Inbox Log
- Tracks 15 incoming emails to the shared mailbox with full assignment and response logging
- Fields: Date Received, Sender, Subject/Request Type, Bond ID Reference, Assigned Processor, Priority, Date Responded, Auto-calculated Response Time, Action Taken, Status, Follow-Up Flag
- Conditional formatting highlights escalated items in red and completed items in green

### 5. Instructions / User Guide
- Documents every sheet, formula logic, color code system, and step-by-step usage instructions
- Enables any team member to adopt the tracker without additional training

---

## Key Excel Techniques Used

- `COUNTIF`, `SUMIF`, `AVERAGEIF`, `COUNTIFS` — cross-sheet live aggregations for the dashboard
- `VLOOKUP` — pulling bond data into the alert table from the main queue
- `IF`, `IFERROR`, `AND` — logical formulas for SLA tracking, match checks, and error handling
- `TODAY()` — dynamic date calculations for real-time deadline monitoring
- **Data Validation** — dropdown lists for Bond Type, Status, and Priority to ensure data integrity
- **Conditional Formatting** — color scales, cell value rules, and text rules across all sheets
- **Cross-sheet references** — all dashboard metrics pull live from the Bond Queue Tracker sheet
- **Named ranges and structured layout** — consistent formatting with freeze panes, merged headers, and professional color scheme

---

## Dataset

- **20 synthetic bond records** across 4 processors (Maria Lopez, James Carter, Sarah Kim, Tom Nguyen)
- Bond amounts ranging from $80,000 to $2,500,000
- Principals span construction, engineering, utilities, and mechanical sectors
- Obligees include state DOTs, municipalities, school districts, federal agencies, and private developers
- Intentional data scenarios: overdue bonds, pending information holds, billing discrepancies, rush submissions, and escalations

---

## Skills Demonstrated

- Surety bond lifecycle understanding (bid bond through close-out)
- Renewal billing accuracy and QA workflows
- Shared email queue management and task assignment
- Deadline tracking and SLA monitoring
- Multi-sheet Excel workbook design with live cross-sheet formulas
- Operational dashboard reporting for team leads and supervisors
- Attention to detail through built-in data validation and error-checking logic

---

## How to Use

1. Open the workbook in Microsoft Excel
2. Start on the **📋 Instructions** tab for a full walkthrough
3. Add or update bonds in the **Bond Queue Tracker** tab using the dropdown menus
4. The **Summary Dashboard** updates automatically — no manual entry required
5. Use the **Renewal Bill Checker** by entering bill figures in the yellow cells
6. Log all incoming emails in the **Email Inbox Log** as they arrive
