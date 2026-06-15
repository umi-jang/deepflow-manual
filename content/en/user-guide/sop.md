# S&OP

*Align team-level sales and production plans into a single company-wide master plan*

## [1] S&OP overview

Turning demand forecasts into operational action depends on how you build and align downstream sales and production plans. In practice, teams often interpret the same forecast differently based on their role — so multiple plans can coexist inside the company.

DeepFlow's S&OP feature stitches those team-level judgments into a single flow. It rolls up sales and production plans across the organization and helps you converge on one executable plan. Each user's edits and approvals are recorded, so the decision context and history travel with the plan.

Use demand forecasts as the baseline, coordinate sales and production plans across teams, and finalize an efficient master plan.

## [2] Authoring and managing sales plans

![Sales plan screen](/images/sop/01.png)

The Sales Plan tab is where planners adjust and finalize sales plans on top of DeepFlow's demand forecast. When the forecast diverges from a planner's judgement — because of promotions, channel issues, or internal strategy — the planner can edit the target sales volume and record the reasoning.

Sales plans are managed per team. The monthly confirmation status tells adjacent teams whether each team's plan is complete.

### [2.1] Entering and editing the sales plan

![Edit sales plan](/images/sop/02.png)

Edit your team's sales plan directly inside DeepFlow.

- Click **Edit target volume** to enter table-edit mode. Editable columns are highlighted in blue.

> **Warning:** To prevent save conflicts and data loss, **only one user can edit a given sheet at a time** (no concurrent editing).
>
> Other users cannot edit the sheet until the active editor either saves or cancels.

Use the supporting data and chart as historical reference, factor in upcoming promotions or end-of-life decisions, and save the target volume along with the reason for adjustment.

- Selecting an item's checkbox displays its chart below.
- The yellow line on the chart represents the target volume you entered. The green line — **Sales (final)** — is the value entered on the Dashboard tab.

### [2.2] Uploading sales plans via Excel

![Bulk Excel upload](/images/sop/03.png)

Use **Upload sales plan** to batch-enter target volumes and adjustment reasons for many items at once.

- The downloaded template lists every item that is in scope for this month's forecast.
- Fill in the target volume and adjustment reason for items you want to plan, and delete the rows for items that don't apply.

> **Warning:** **Required fields**: item code, target volume, adjustment reason.
>
> Make sure no cells in those columns are blank.

### [2.3] Per-team sheets

![Per-team sheet management](/images/sop/04.png)

When multiple teams contribute to the sales plan, use per-team sheets. Users with manager permissions can create, rename, and delete team sheets.

- **Click [+]**: Adds a new sheet (named by department) to the rightmost position.
- **Right-click a sheet tab**: Rename or delete the sheet.

### [2.4] Sales plan approvals

![Approval flow](/images/sop/05.png)

Managers approve or reject each line item in a team sheet.

### Select items

Tick the items, then click **Approve / Reject selection**.

### Approve or reject

Confirm by clicking **Approve** or **Reject**.

### Verify the result

Once approved, the final approver's name and timestamp appear on the row.

> **Tip:** **Quick-approval tip**: Filter the **Status** column to **Review pending** or **AI prediction**, click the header checkbox to select all visible items, and approve in one go.

Only items in **Review pending** or **AI prediction** states are eligible for approval.

- **AI prediction**: DeepFlow has produced a forecast for the item. You can approve it as the sales plan with no adjustment.
- **Review pending**: The planner has reviewed the forecast and entered a target volume and adjustment reason.

### [2.5] Confirming the monthly plan

![Confirm monthly plan](/images/sop/06.png)

Once every item in the sheet is approved, click **Confirm sales plan**.

- This indicates that your team's plan is complete.
- Confirmed plans appear in the S&OP > Dashboard view, where each team's sales and production volumes — and their confirmation state — are visible.

### [2.6] Reviewing the adjustment history

![Adjustment history](/images/sop/07.png)

Click **View adjustment history** to see the edits made to target volumes along with the approval trail.

## [3] Authoring and managing production plans

![Production plan screen](/images/sop/08.png)

Production plans follow the same flow as sales plans:

`Author or upload` → `Approve / reject` → `Confirm monthly plan`

Adjustment-history review and per-team sheet management are also available. See **[2] Authoring and managing sales plans** sections [2.1]–[2.6] for the full reference.

> **Tip:** **Entering and editing the production plan**
>
> - **Edit in DeepFlow**: Click **Edit recommended production** → enter the production quantity and reason in the **Production qty (confirmed)** and **Adjustment reason** cells → click **Save**.
> - **Upload via Excel**: Click **Upload** → download the template → fill in the production quantities and reasons → click **Upload sales plan** → choose the file.
>
> ※ To prevent save conflicts and data loss, only one user can edit a sheet at a time.

## [4] Confirming the S&OP plan (dashboard)

![S&OP dashboard](/images/sop/09.png)

The Dashboard is where you finalize the S&OP plan based on each team's sales and production plans. The highlighted **Sales (final)** and **Production (final)** cells are what you enter on the dashboard.

After teams have built their plans for the month, the dashboard shows their submitted volumes, while **Sales (final)** and **Production (final)** start out blank. Once you fill those cells, the chart below reflects the final plan.

![Auto-fill](/images/sop/10.png)

The **Auto-fill sales & production** action populates the Sales (final) and Production (final) cells for you using either a specific team's plan or DeepFlow's AI forecast.

> **Tip:** The final plan also shows up on the Sales Plan tab's chart, so planners can compare their team plan against the finalized version.
