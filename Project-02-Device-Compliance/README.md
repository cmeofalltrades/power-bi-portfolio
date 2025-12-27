# Project 02 — Device Compliance Dashboard (MD-102 Aligned)

## Goal
Build an endpoint compliance + patching dashboard that answers:
- How many devices are compliant right now?
- Which OS/device types have the most non-compliance?
- What are the top non-compliance issues?
- Are patches being installed within 7 days?

## Data
Stored in `/data`:
- `Users.csv` — user dimension (location/department)
- `Devices.csv` — device dimension (OS, type, assigned user)
- `ComplianceChecks.csv` — weekly compliance check events (trend)
- `PatchEvents.csv` — monthly patch status per device (patch timeliness)

## Model (Star-ish)
- `Devices[AssignedUserID]` → `Users[UserID]` (many-to-one)
- `ComplianceChecks[DeviceID]` → `Devices[DeviceID]` (many-to-one)
- `PatchEvents[DeviceID]` → `Devices[DeviceID]` (many-to-one)
- Create a `Date` table and relate:
  - `Date[Date]` → `ComplianceChecks[CheckDate]`

## Suggested pages
### Page 1 — Compliance Overview
- Cards: Total Devices, Compliant Devices, Compliance %, Non-Compliant Devices
- Trend line: Compliance % over time (by CheckDate)
- Bar: Non-compliant devices by OS
- Bar: Non-compliant devices by Location
- Treemap/Bar: TopIssue count

### Page 2 — Patch Health
- KPI: % Installed within 7 days
- Bar: PatchStatus counts (Installed/Pending/Failed)
- Table: Devices with Pending/Failed patches + DaysToInstall

## Deliverables to commit
- `/pbix/Device-Compliance.pbix`
- `/images/dashboard-page-1.png`, `/images/dashboard-page-2.png`
- README updates with insights
