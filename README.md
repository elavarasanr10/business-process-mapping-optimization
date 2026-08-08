# Business Process Mapping & Optimization Case Study

**Author:** Elavarasan R  
**Project:** Business Process Mapping & Optimization  

---

## 📊 Dashboard Preview

<img width="1224" height="724" alt="dashboard_summary1" src="https://github.com/user-attachments/assets/a29d41c5-7fa2-46f0-abf7-9e2543231cae" />


## Objective
Analyze the workflows of a mid-size company across five core processes, identify where time, cost, and quality are being lost, and recommend a redesigned ("To-Be") process supported by measurable KPIs.

## Business Problem
The company is losing money and customer trust to slow, error-prone, manually-handled processes: orders that take too long to fulfill, invoices stuck in approval, onboarding that drags past a new hire's start date, support tickets that miss SLA, and vendor payments delayed by manual matching. Leadership needs a clear, data-backed view of where the biggest losses are and what to fix first.

## Case Study Background
The dataset (`data/Process_Data_Raw.xlsx`) covers 110 process-activity records across five processes and five departments — Order-to-Cash (Sales & Fulfillment), Invoice Processing (Finance), Employee Onboarding (HR), Customer Support Ticketing (Customer Service), and Procurement & Vendor Payment (Procurement). Each row captures one activity instance: timing, volume, cost, errors, rework, SLA target vs. actual, and complaints.

## Process Mapping Methodology
- **SIPOC** to frame each process's Suppliers, Inputs, Process, Outputs, and Customers before mapping detail.
- **As-Is mapping** of the current workflow step by step, marking handoffs, approvals, and wait points.
- **To-Be mapping** of the redesigned workflow once bottlenecks are addressed.

## Analysis Performed
- **Bottleneck analysis** — activities with the highest waiting time and approval time relative to their SLA target.
- **Root cause analysis** — grouping repeated errors and rework by activity and resource to find where failure originates, not just where it shows up.
- **Gap analysis** — current KPI values against SLA targets and industry-typical benchmarks.
- **Cost analysis** — process cost per activity and per completed task, to find the most expensive steps.
- **SLA and complaint analysis** — correlating missed SLAs with customer complaint volume.

## Optimization Recommendations
- Automate the highest-volume manual steps (data entry, invoice matching, ticket triage) with RPA or workflow rules.
- Replace single-approver chains with parallel or delegated approval routing to cut approval time.
- Integrate CRM/ERP/HRIS systems so data isn't re-entered across handoffs.
- Add SLA checkpoints mid-process, not just at completion, so delays are caught before they cascade.
- Stand up a self-service option for the highest-volume, lowest-complexity requests (order status, ticket status).

## Dashboard Features
- **KPI cards:** Cycle Time, SLA Achievement %, Process Cost, Error Rate, Productivity %.
- **Process Flow Analysis** — cycle time by process and activity.
- **Bottleneck Analysis** — waiting time and approval time by activity.
- **Cost Analysis** — cost per process and per department.
- **Error & Rework** — error rate and rework rate trends.
- **Before vs. After** — As-Is vs. To-Be KPI comparison once optimizations are modeled.
- **Filters** — by department, process, date range, and resource.

## Key Insights
- Procurement and Invoice Processing carry the longest waiting and approval times relative to their SLA targets — the clearest automation candidates.
- SLA misses correlate closely with higher customer complaint counts, especially in Customer Support and Order-to-Cash.
- A small set of activities (manual data entry, approval steps, matching steps) account for a disproportionate share of errors and rework across every process.

## Conclusion
The data points to a consistent pattern: value is lost less in the "doing" of the work and more in the waiting, handoffs, and manual re-entry around it. Targeted automation and approval redesign on the worst-performing activities would meaningfully cut cycle time and cost without a full process overhaul.

## Repository Structure


```
business-process-mapping-optimization/
├── data/
│   └── Process_Data_Raw.xlsx
├── process-maps/
│   ├── as-is-process-map.png
│   └── to-be-process-map.png
├── analysis/
│   └── kpi-analysis-notes.md
├── dashboard/
│   └── dashboard-screenshot.png
├── report/
│   └── business-recommendation-report.md
└── README.md
```

## Tools Used
Excel/Power BI for KPI analysis and dashboarding, Lucidchart/Draw.io for process mapping, and this repository for version control and portfolio presentation.
