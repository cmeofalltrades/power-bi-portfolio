# Project 02 — Device Compliance & Patch Health Dashboard

## Overview
This project simulates an endpoint compliance and patch management reporting solution aligned with **Microsoft MD-102 / Endpoint Administrator** responsibilities. The dashboard provides visibility into device compliance posture, non-compliance drivers, and patch installation health across multiple locations, operating systems, and device types.

The goal is to demonstrate real-world Power BI modeling, DAX, and dashboard design skills applied to IT operations and endpoint management use cases.

---

## Tools & Technologies
- Power BI Desktop
- Power Query
- DAX
- CSV-based relational dataset
- GitHub (documentation & version control)

---

## Data Model
**Tables Used:**
- `Users` — user location and department
- `Devices` — device type, OS, assigned user
- `ComplianceChecks` — weekly compliance status checks
- `PatchEvents` — monthly patch release and installation tracking
- `Date` — centralized date table

**Relationships:**
- Users (1) → Devices (*)
- Devices (1) → ComplianceChecks (*)
- Devices (1) → PatchEvents (*)
- Date (1) → ComplianceChecks (*)
- Date (1) → PatchEvents (*) via Patch Release Date

---

## Dashboard Pages

### Page 1 — Compliance Overview
Provides an executive-level view of endpoint compliance health.

**Key Metrics:**
- Total Devices
- Compliant Devices
- Non-Compliant Devices
- Compliance Percentage

**Visuals Include:**
- Compliance % trend over time
- Non-compliant devices by OS
- Non-compliant devices by device type
- Top non-compliance issues (encryption, antivirus, updates, policy)

**Purpose:**
Identify compliance trends and prioritize remediation efforts by platform and device category.

---

### Page 2 — Patch Health
Focuses on patch deployment effectiveness and operational risk.

**Key Metrics:**
- Total Patch Events
- Installed Patches
- Pending or Failed Patches
- % Installed Within 7 Days (SLA metric)

**Visuals Include:**
- Patch status distribution
- Patch installation timeliness
- Action table highlighting devices with pending or failed patches
- Days since patch release to prioritize overdue remediation

**Purpose:**
Monitor patch backlog, identify at-risk devices, and measure patching SLA performance.

---

## Key Skills Demonstrated
- Star-schema style data modeling
- Date table implementation and time-based filtering
- DAX measures for KPIs and SLA metrics
- Slicer-driven, interactive dashboards
- Operational dashboard design for IT and endpoint management
- GitHub documentation and portfolio presentation

---

## Screenshots
Screenshots of both dashboard pages are included in the [screenshots](./screenshots) folder.

---

## Notes
This project uses synthetic data to simulate realistic enterprise endpoint environments and patch management scenarios.
