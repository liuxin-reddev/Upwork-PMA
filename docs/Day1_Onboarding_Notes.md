# PMA Consultants: Day 1 Onboarding Notes

**Role:** Project Billings Specialist (Upwork contract). I report to **Samantha (Sam) Zeisler, Billing Lead**.
**Sources:** *Billing 101: Team Reference* PDF (`6_Billing_101_Team_Reference_Danny_and_Dax.pdf`) and the Day 1 meeting transcript (onboarding session, then the daily NetSuite issue triage).

> **The review rule:** nothing goes to a PM or client until Sam has reviewed it. Questions go in the **NetSuite (Contracts) chat**. Blockers go on the **Contracts Team Task Tracker** (Smartsheet).

---

## 1. Who's who

| Person | Role / context | Notes |
|---|---|---|
| **Samantha (Sam) Zeisler** | Billing Lead, my manager | About 10 years at PMA. Reviews every invoice. Ran the onboarding. |
| **Dax** | CEO (since 2024) | 20+ years at PMA, civil engineering and project controls background. Being onboarded alongside me ("Danny and Dax"). Closely involved in the NetSuite transition. |
| **Elie ("Ellie") Blumen** | Chief Financial Analyst | Chicago office, about 25 years at PMA. Explained the billing cycle and regions. |
| **Kirsten Sell** | Chief Administrative Officer | Was in my interview, not in Day 1 calls. |
| **Janet Shirley** | Hiring / Upwork contact | |
| **Nazima** | Outside consultant (CLA) helping with billing | 3 weeks in, about 3.5 years of NetSuite experience. |
| **Pam Hersik** | Payroll Manager | Supporting Billings and bridging accounting, payroll and billing. My contact for timesheet and payroll questions. |
| **Takia Long** | Billing team | About 3 years at PMA. |
| **Sonia** | Billing team | About 8 months at PMA. |
| **Daphne** | Billing team, part-time | About 10 years at PMA. **Off on Thursdays.** |
| **Neda** | Joining the billing team | Moving over from operations. |
| **Eric** | Role and approval troubleshooting | Sam: "loop in Eric" for permission or approval-button problems. Fixes roles with **Andrew**. |
| **Steven** | NetSuite developer/consultant (probably) | Moved the invoice-line override fields. |
| **Alicia** | Biller, New England region | Piloting the Percent Complete subproject setup. Ask her about that. |
| **Scott** | PM on the GLWA example project | Works out of SharePoint. |

**The team:** six people dedicated to billing. Each one owns a portfolio of invoices by **region** and bills the same invoices every month. When a region wins a new project, that region's billers handle its invoicing and contract management.

---

## 2. Big picture

- About **150 active clients** and roughly **220–250 invoices a month** (Ellie said about 225).
- **NetSuite went live in July** (moved from **Deltek Vision**). The team is **behind schedule**: at the start of November they were still finishing **September** and should already be billing **October**.
- **Billing types:**
  - Time & Materials: the majority.
  - Lump sum / Fixed fee: about 15–20%.
  - Percent Complete: about 2%. Only a handful of projects, and "maybe one" is truly percent complete.
- **Revenue recognition:** revenue is recognized **as charged/invoiced**. Every Project Rule needs a matching **Project Revenue Rule (As Charged)**. On Percent Complete projects the **PM supplies the cumulative %** and it is entered manually. The input/cost-based method is not used.
- **Subsidiaries:** PMA Consultants (almost all my work), PMA Technologies, PMA Canada, and one **Joint Venture** set up for a single project. PMA invoices the JV, and the JV invoices the client together with the other firms' work. Puerto Rico and similar work bills from PMA Consultants (Puerto Rico needs **tax**).

---

## 3. Monthly billing cycle

The month's work is billed the following month. In November we bill October hours.

| Source | Start | Close |
|---|---|---|
| Ellie (meeting) | Around the **1st**. Some clients need an invoice by the 1st. | Historically by the **20th**. Goal is **mid-month** once NetSuite settles. |
| PDF | Open billing on the **4th or 5th** | By about the **25th** |

> ⚠️ The two sources disagree on the dates. **Ask Sam which target applies to my portfolio.**

Client timing varies. Some bill on the 1st, some have cut-off dates, some bill at milestones (hours carried until a milestone is met), and some bill off-month.

Each biller keeps the **Contracts Billing Tracker** current: In progress → Out for approval → Approved → Billed.

---

## 4. Project lifecycle and who owns what

```
P-Sale → Awarded → New billable project → Setup with PM → Time / expenses / subs → Charges → Invoice → Client pays → Closeout
```

| Owner | Responsibilities |
|---|---|
| **Marketing** (with the PM) | P-Sale (promotional project). Captures budget, NTP, delivery system, referral or new client, industry, services, project segmentation. |
| **Contracts (us)** with the PM | Project setup, task structure, resource assignments |
| **Contracts only** | Billing rules, charges, labor transfers (moving hours), preparing, reviewing and sending invoices, corrections and Credit Rebills |
| **PM** | Timesheet review and approval, invoice approval, budgets, starting closeout (Contracts completes it) |
| **Accounting** (about 5–8 people) | Payroll, sub-consultant bills (AP), expense reports, receiving and posting payments (AR), revenue recognition postings |

In NetSuite our role is **Contract Administrator**. Other names for the team are "Contracts" and "Billers".

---

## 5. New project setup (P-Sale → billable)

1. On the **P-Sales Awarded** dashboard portlet, find P-Sales flipped to *Awarded*. They are on the **P-Sales form**, carry a **"P"** in the project number, and have the **P-Sales checkbox** checked.
2. **Check the Customer first.** It cannot be changed once transactions exist.
   - Parent or child? A child shows a parent field on the customer record. The **Relationships** subtab lists sub-customers, and an empty one means the customer is a parent.
   - Check the address and contacts, and which other projects use this customer.
   - Look at how previous projects for the same client were set up (e.g., GLWA has three customer records). If unsure, confirm with the PM.
3. **Make a copy** of the P-Sale and change the form to **PMA Project Billing**. That unlocks the contract-admin fields, and NetSuite assigns the next project number automatically.
   - Legacy (Deltek) numbering is `0XXXX.00` (e.g., `04749.00`). **New NetSuite projects use 4 digits with no `.00`** (e.g., `5003`).
4. Uncheck **P-Sales**, set **Status = Active**, and tick **Allow Expenses** on the Preferences tab.
5. Before billing, these must be complete: PM, Invoicing PM, Resources, the **Resource Details tab with two Project Managers**, project budget, task budgets, start and end dates.
6. Put the contract documents (usually received by email) in the **SharePoint folder** or the project/task **Communication** tab.
7. Hold a **kickoff call with the PM** to go through setup together.

### Key fields explained in the meeting
- **Project Manager** handles **time entry approvals**. They must **also** be listed as a PM on the **Resource Details** tab, or timesheets will error. Aim for **two PMs** there as backup for approvals.
- **Invoicing Project Manager** handles **invoice approvals**. It can be a different person from the PM (Scott runs the project, Bob approves the invoice).
- **Invoicing Project** (custom field, built for Percent Complete subprojects). In about 95% of cases it equals the top-level parent project. Example: `4812` uses a subproject to carry the percent complete.
- **Resources** control which **tasks appear on an employee's timesheet**, which limits errors. Planned work is often a placeholder of **1 hour**. Only **actuals** are tracked; forecasting may come later.
- **Project Biller**: my name needs to be on my employee record as a biller (Sam is checking).
- **Send Invoices from PM**: checkbox exists but is probably not used yet.
- **Project SharePoint Folder**: link to the PM's files. Contract files are currently kept in two places, and Deltek files did not migrate.
- **Project Invoice Note**: free text that **prints on the invoice** (e.g., "added $1,500 for…", or a PO when there is no PO field).
- **Fee/budget fields**: Original PMA Fee (set once), PMA Current Fee (with change orders or amendments), PMA Billing Limit (Project Task Sum) = sum of the task budgets, and **Total Project Billing Limit Override** for when the sum of task budgets is not the approved project budget. Fields marked "(source from task)" are **landing fields for scripts and workflows**. Some have field-level help ("includes DJC historical").
- **Contract Type**: CPFF, Fixed Fee, Percent Complete, T&M/Fixed Fee combo. **Only Percent Complete changes any functionality.**
- **Pay When Paid Subcontractors**: subs are paid when PMA is paid. It affects the vendor bill.
- **Terms** drive the AR due date printed on the invoice.
- **Billing Contact** can be set at the customer or project level. A project-level contact is not added to the customer.
- **Retainage**: Calculate Customer Retainage and/or Calculate Vendor Retainage, Retainage %, which item types to retain on (consulting, expenses, etc.), and **Prior Retainage Amount**, entered from Deltek history for projects that were already running retainage.
- **Project Dates**: many Estimated End Dates are out of date. Cleanup comes later.
- **Classification / Department = region.** This **must be right on new projects**.
- **Financial tab**: Billing Type is always **Charge-Based**.

---

## 6. Invoice printing checkboxes (project level and invoice level)

**Project level (Invoice Printing Defaults):** Withholding (2% or 5%), Signed Timesheets, Billing Summary, Expense Attachments (almost always on), Billing Back-Up (the detail behind the hours; often off for fixed fee).

**More checkboxes exist on the invoice form**, added later by NetSuite (e.g., **Billing Summary by Task**). If the project-level settings don't produce the layout you need, check the invoice form. Sam would prefer all of them at the project level.

**Billing summary tables:** a project-level table shows current, prior, limit and remaining. **Task-level tracking became available in September.** August invoices only show the project-level total (e.g., GLWA's $8M override).

The PDF comes from **NS WIP Print Invoice**: task by task, employee hours × rate, then subs and expenses.

---

## 7. How an invoice works (from the PDF)

1. Review **charges** and set their status at the project level: **Ready / Hold / Processed / Non-Billable**.
2. Raise the draft from **Invoice Billable Customers** using the correct date range.
3. Review the settings: Invoice #, **Posting Period (Override)**, start and end dates (re-enter them after the invoice loads), checkboxes, PM and Invoicing PM. **Save once** so NetSuite pulls in the invoicing project fields.
4. Review every charge (time, subs, expenses, additional fees, tax, retainage, ceiling and task budgets).
5. Run **NS WIP Print** and read it as the client will.
6. **Submit for Approval.** ⚠️ *Pending Approval* only means the draft has been opened. The PM **does not have it** until you click Submit for Approval.
7. Deliver to the client and record how. Use **Submitted Outside of NetSuite** for email-with-backup, portals (e-Builder, PMWeb, Coupa, Trimble: **select PMA in the dropdown**) or the client's own format.

**The three keys** when something looks wrong: **project configuration**, **invoice configuration**, **charge review**.

**Project Rules vs. Revenue Rules:** every new or changed Time-Based, Fixed Fee, Purchase or Expense rule must be added to a matching **Revenue Rule**. Fixed Fee projects need new rule(s) **every month**. Saved search: **Projects Missing Rev Rules**.

### Sample invoices to study
| Project | What it teaches |
|---|---|
| 04797.00 | Fixed fee, two tasks |
| 04886.00 (Oct) | Split-period expenses held for the October invoice |
| 04749 GLWA | Sub invoices (METCO, Stantec, NTH) and the PM's write-up |
| 04903.00 PI Consultants | Manual Excel template. The client rejects penny differences, and there are early due dates and cut-offs. |
| 04547.00 United | Task-by-task billing (invoices A, B and C), Hold/Ready by task, Coupa submission |
| **4821 Penn Station** | **Backlog project assigned to me** in the Drive-with-review stage |
| P5418 West Farms Bus Depot CNG | Francisco's new project, used as the setup walkthrough |

### Saved searches
Saved Time Search - SZ, Actual Time Charges Samantha Results, Projects Missing Rev Rules.

---

## 8. Daily NetSuite issue triage (open items from Day 1)

The meeting runs daily, right after the onboarding block. It covers NetSuite invoicing blockers, which are logged on the **NetSuite issue log** and sent on to the NetSuite team.

| # | Raised by | Issue | My notes and ideas to offer once I've shadowed more |
|---|---|---|---|
| 1 | Nazima | Error on saving an invoice. The lines were there after reload, and cancelling and re-running worked. Possibly retainage. Fee lines land in the wrong section unless the **Parent Task / Child Task override** columns are filled. A **third override column on the far right** is still there. | The override fields exist because the standard task list shows tasks from **every project with the same task name**. The custom fields filter to this project. Ask Steven why the third column was kept. Nazima asked about **subtotal rows** on the invoice; Sam is open to testing it. |
| 2 | Sonia | PM on **5008 Beth Israel** can't see the **Approve** button. The status stays "Pending Approval". | Check first that the draft was actually **Submitted for Approval** (Pending Approval alone doesn't route it). Then check that the **Invoicing Project Manager** on the invoice matches the PM trying to approve, that the PM's **role** has approval permission, and that no approve/reject/re-approve loop has stalled the workflow (the "Rainy" case). Sam: **loop in Eric**. |
| 3 | Takia | **Leslie Succalit** (not the other Leslie) on **4899.00**, September. Takia made a labor transfer, then Leslie and Ken also edited, resubmitted and re-approved her timesheet. Result: **two lines for the same hours**. | Risk of **double billing** and a payroll mismatch. Check Manage Pending Charges for duplicate charges, and put the duplicate on Hold or Non-Billable until Pam confirms which time entry is correct. Pam asked whether Leslie has been terminated. The September period may be locked, so ask how locked-period time changes are handled. |

**Lesson:** labor transfers belong to Contracts. Employees and PMs editing approved timesheets afterwards creates duplicates.

---

## 9. My action items

- [ ] Reply to Sam and confirm I have the Billing 101 PDF. Ask for access: NetSuite role (Contract Administrator), the NetSuite (Contracts) chat, the Contracts Billing Tracker, the Smartsheet Task Tracker, the SharePoint Project Folder Structure and the EUB Unbilled Data Details file.
- [ ] Ask Sam to add me as **Project Biller** on my employee record.
- [ ] Join the afternoon shadowing session at 12:00 (project cleanup).
- [ ] Attend the daily issue triage.
- [ ] Read the Monthly Invoicing Checklist (PDF section 7) closely. To leave the Shadow stage I need to be able to **explain the invoice steps and the charge statuses**.
- [ ] Study the sample invoices, then **4821 Penn Station** (my first backlog project).
- [ ] Keep a running question log and post questions in the Contracts chat.
- [ ] Keep Sam posted on my health (COVID) and let her know if the schedule needs to move.

## 10. Questions to ask

1. Billing calendar: is the target open on the 1st or the 4th/5th, and close on the 20th, the 25th, or mid-month? Is it different for the backlog?
2. Which region or portfolio will I own, and when does the defined project list start?
3. Time approval routing: are approvals routed to the **project's PM** or to the employee's **Time Approver** (employee record)? What limitation stopped us from using the employee record?
4. Is there an example project where **Invoicing Project ≠ Top-Level Parent** that I can study (ask Alicia)?
5. When should I use **Total Project Billing Limit Override**, and who approves using it?
6. How are corrections to **closed or locked-period** time handled? The PDF says that process is "coming".
7. Credit Rebill vs. Credit Memo: when is each used?
8. Retainage on JV / West… sub invoices: should Calculate Vendor Retainage be on?
9. Is there a list of each client's invoice requirements (templates, portals, backup), or does it live only in the SharePoint folders?
10. Which NetSuite improvements are wanted that I could help with (saved searches, dashboards, forecasting with planned hours, moving the invoice-level checkboxes to the project level)?

---

## 11. Quick glossary

**P-Sale** promotional project · **NTP** notice to proceed · **Charge** billable transaction from approved activity · **Ready / Hold / Processed / Non-Billable** charge statuses · **Billing Limit** maximum billable amount (project, task or subtask) · **Credit Rebill** reversing and replacement charges, used once the invoice is delivered and the period is closed · **Write-Off** charges removed that won't be invoiced · **Home / Field** resource designation used in rules · **WIP Print** client-facing draft PDF · **Submitted Outside of NetSuite** delivery flag · **GLWA** Great Lakes Water Authority · **SFPUC** San Francisco Public Utilities · **CPFF** cost plus fixed fee · **DJC** direct job cost.
