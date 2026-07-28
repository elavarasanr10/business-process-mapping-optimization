# KPI Analysis Notes

These notes summarize the bottleneck, root cause, and gap analysis performed on `data/Process_Data_Raw.xlsx`, using the KPI summary built in Google Sheets and visualized in Power BI.

## 1. Bottleneck Analysis
For each process, Waiting Time and Approval Time were compared against the SLA Target. The two consistent problem areas:
- **Procurement & Vendor Payment** — the longest combined waiting + approval time relative to its SLA target, concentrated in the Invoice Matching and Payment Approval activities.
- **Invoice Processing** — Manager Approval is a single-point holdup; when that step slows down, the whole process misses SLA.

## 2. Root Cause Analysis
Grouping Error Count and Rework Count by Activity Name shows errors cluster in manual, single-person steps rather than being spread evenly:
- Manual data entry and manual invoice matching account for a disproportionate share of errors.
- Rework is highest wherever an activity depends on another team's output arriving in the right format — a handoff problem, not a skills problem.

## 3. Gap Analysis
Comparing SLA Achieved (Yes/No) against SLA Target by process:
- Order-to-Cash and Customer Support Ticketing miss SLA most often, and those misses track closely with higher Customer Complaint Count in the same rows.
- Employee Onboarding is closest to its SLA target on average, but still has isolated delays tied to Background Verification.

## 4. Cost Analysis
Cost per Transaction (Process Cost ÷ Tasks Completed) is highest in Procurement and Invoice Processing — the same two processes flagged in the bottleneck analysis. This is the strongest signal in the dataset: the slowest processes are also the most expensive per transaction, which is what makes them the priority for optimization rather than a nice-to-have.

## Summary
The pattern across all four analyses points the same direction: a small number of manual, single-owner activities (approval steps, manual matching, manual data entry) are driving delay, error, cost, and complaints together. Fixing those specific steps — not a full process overhaul — is where the highest return is.
