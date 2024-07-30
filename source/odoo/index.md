---
title: Odoo
lang: en
direction: ltr
date: 2024-07-29 15:04:16
cover: /odoo/odoo_customizations_cover.jpg
---

# Ultra Tendency International GmbH: April 2022 - July 2024

Working with UT was the first time I have worked with company over 100 employees using Odoo. It was challenging and more opportunities to explore. I spent a lot of time with PMOs and HRs at most (Timesheets, Planning and Projects). I'll list _major_ customizations I've done in those modules.

## Timesheets

In addition to the following customizations, I've also done minor changes to how Timesheets are recorded. For example, ensuring it is not exceeding target hours limit, or don't record on Sundays unless there are exception projects. 

### Gantt View

The first requirement I remember was the to make it easier for HRs to recognize overtime or undertime timesheet hours. In Odoo 14 or 15, it was hard to perceive how each employee is recording his/her hours without some highlight clues, so I suggested to enhance the existing Gantt view, by adding hints in each cell. Later Odoo 16 (shown in the screenshot) make it better by having overtime/undertime hours besides employee name. It is still useful in Odoo 16, since Gantt cells are highlighted, making the Gantt view better.
<br>

{% img /odoo/customizations/ultratendency/timesheets/timesheets_monthly_heatmap.png Monthly Timesheets customizations for Odoo 15 and Odoo 16 %}

{% img /odoo/customizations/ultratendency/timesheets/timesheets_weekly_heatmap.png Weekly Timesheets customizations for Odoo 15 and Odoo 16 %}


### Quarter (or specified dates range) Report

This requirement is based on the need to watch employees overall quarterly performance, thats beyond what Gantt view provides. This report also displays data based on a specific date range. It was generated using PostgreSQL.
<br> 

{% img /odoo/customizations/ultratendency/timesheets/timesheets_report_dialog.png Timesheets report dialog %}

{% img /odoo/customizations/ultratendency/timesheets/timesheets_report_june-august.png Timesheets report demo from June to August %}


## Planning

There was a need to adjust planning slots according the employee time-offs or public holidays. It was challenging, as there are a couple of cases that needs to be addressed before making this happen. As you can see in the following screenshot, _blueMix_ has a planning slot for 4 days, and there is an empty slot at the middle (Wednesday). This is because, _blueMix_ has a time-off or a public holiday on Wedensday, so plannig for this day is cleared. This applies when the employee has multiple slots in the same date range, and it also applies to half-day time-offs of public holidays spanned over a couple of days.
<br>

{% img /odoo/customizations/ultratendency/planning/automatic-planning-slots-adjustment.png Automatic planning adjustment in Odoo %}

{% img /odoo/customizations/ultratendency/planning/automatic-planning-slots-diagram-middle.png Automatic planning adjustment (middle) in Odoo %}

{% img /odoo/customizations/ultratendency/planning/automatic-planning-slots-diagram-end.png Automatic planning adjustment (end) in Odoo %}

{% img /odoo/customizations/ultratendency/planning/automatic-planning-slots-diagram-beginning.png Automatic planning adjustment (beginning) in Odoo %}



## Projects

### Tasks-Planning Insights
In Odoo 14, there was Projects Dashboard, where you can see insights about how projects' planning is doing well or not. This was a helful feature for PMOs, but they removed it in Odoo 15 and so I have to find the same insights data. The important attributes were:
* Remaining Hours (Planning included)

Remaining Hours (Planning included) was really tricky, because it includes data from other parameters to be calculated (task initial hours, delivered hours, monthly timesheet hours, monthly planned hours, total planned hours). I've did this using PostgreSQL to make execution faster (I've did it using the ORM, but there was noticable delays, which frustrates PMOs). In addition to the above data, I've also included other parameters who were also useful for PMOs in planning insights. They were:

* Remaining Hours to Forecast
* Month Timesheet Hours
* Month Allocated Hours
* Sold Hours
* Total Allocated Hours
* Upcomming Allocated Hours

<br>

{% img /odoo/customizations/ultratendency/projects/project-tasks-planning-analysis.png Projects tasks planning analysis %}

### Projects Cost Report

This report shows whats is the cost generated for each employee's delivered costs and planned costs, according to his/her timesheet hours and planned hours, respectively.
<br>

{% img /odoo/customizations/ultratendency/projects/projects-cost-report.png Project cost report %}


## Sales


### Revenues Report

This report shows generated revenues based on timesheet hours, and forecasted revenues based on planned hours. The hourly rate average is based on the sale order item hourly/daily price. It also calcuates both, fixed-amount and on-demand-based sale order items. This was also generated using PostgreSQL.
<br>

{% img /odoo/customizations/ultratendency/sales/sales-report.png Sales Report in Odoo %}
