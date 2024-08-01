---
title: Odoo
lang: en
direction: ltr
date: 2024-07-29 15:04:16
cover: /odoo/odoo_customizations_cover.jpg
---

This page is allocated to writing my exprience with Odoo customizations while I worked with companies or as a freelancer, started from 2017. 

> All data presented here are demo/fake data

# Ultra Tendency International GmbH: April 2022 - July 2024


{% img /odoo/customizations/ultratendency/ut-home-menu.png Ultra Tendency Odoo Home Menu for Odoo 16 %}



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


# Freelancing: April 2020 - February 2022

This period of my life was kinda new to me, since it was my first time trying to contact clients to see if they need solutions for their company. However, my first client Infinity Technlogies got referred through a friend of mine, while the other one, sic-express, while I was showing then AI-chatbot for their Messenger, but they wanted accounting system instead! XD

## Infinity Technologies


{% img /odoo/customizations/infinity/odoo-infinity-tech-home-menu.png Odoo home menu for Infinity Technologies %}

[This client](https://infinitytechiq.com) (friends by now) have gained me more exprience than all of other companies/customers combined. With this, I learned how accounting, sales, purchase, inventory works (especially accounting!). Luckily, I have tracked all of the customizations in a file. It is a LONG list.


```markdown
* [REQIREMENTS] Company currency
	- USD and IQD
	- Buying products with USD, and selling them with IQD
* [Done] Product customization
	- product spare parts
* [Cancelled] Invoice customization
	- Show detailed products items/spare parts
* [Done] Purchase order customization
	- Show detailed products items/spare parts
* [Done] Changing 'Inventory' to 'Warehouse'
* [Done] FIFO product costing method should consider when buying next
	- Example: purchasing 100 items with $5 and then buying 100 items with $7. Now when selling the whole 100 items with $5, the product cost is not $5. But it should be $7, and not $5.
* [Done] Sales margin should updated to reflect the actual number products prices in the inventory
* [Done] Automatically set product type to Storable Product when creating a new product
* [Done] Deleting purchase order document
	[STEPS]: Cancel the PO first, then delete it
* [Cancelled] Building report for الحسابات العامة ١
	- Can be replaced with the dynamic reports module
* [Done] Service/Maintenance products forms and scheduling maintenance notifications
* [Done] Product form Saleable/Purchase checkboxes should be aligned with their lables
* [Done] Hiding product cost and margin for non-authorized employees
* [NOTE] Product internal reference should be replaced with part number
	- You can use reference number instead of product part number
* [Done] showing a colum of product internal reference when making a purchase/sale order
* [Done] Tasks (reports) for each employee
* Adding product manufacturer colum	when
	- [DONE] creating a purchase/sales order
	- viewing products canban view
* [Done] Employee expenses
	The processing of crediting employees to be used for project expenses.
* [Done] Petty Cash (السلف) for employees
* [Done] Payroll for employees
* [NOTE] Clear auto-filling last product unit price and make it $0
	- You can edit the prduct purchase prices from the product Purchase tab
* [Done] Only authorized employees can create analytic accounts
* [Done] Sales Orders Approval
* [Done] Deploying Odoo as a training system (existing) and as a production one
* [Done] Documents app for products or projects
	- can be accessed by all users
	- Attaching documents to projects (PO)
* [Done] Can be sold, and Can be purchased, and can be expensed product properties should be checked by default and removed
	from the product details. Can be shown by admins
* [Done] Product logs for all transactions
* [Done] Hiding product Sales tab for non-authorized users
* [Done] Changing product Internal Reference name to Part Number/SN
* [Done] Hiding Produt Purchase unit of measure
* [Done] Separating employee tasks
	- each employee should not see other employee's tasks
* [Done] Bundle quantity should be computed based on the available bundle items quantities
	- Example: Outlet O2 has 1 cover, 1 bush and 1 basement. If there are 20 covers, 20 bushes and 20 basements, it means there are
	20 Outlets avaiable.
* [Done] Product bundle items should be reduced with inventory out, and increased with inventory in
* [Done] Employees براءة الذملة لتسليم الأجهزة
	- [Note] it is named as "employees checklist"
* [Done] Showing a status dashboard for products that don't have values for sales price or cost
	- Rebaz wants to see what products that don't have their prices updated/inserted
		- [Note] You can sort products by their sales price to see the intended products
* [Done] Warining message for duplicate part number/sn
* [Needs Credit] SMS for due payments of customers
	- SMS button for sending due paymens
	- automatically and perdiodically send SMS before a week to notify about due payments
* [Done] Sales order quotation design
* [Note] Project cost estimation
	- Show products costs and how much does the project costs for each of them
	- You can use 
* [Done] Chainging Projects menu to Projects Reports
* [Note] Tasks messages notifications are not working
	= It needs email configuration
* [Done] Checking why the FIFO margin is not working
	- Make sure that product category inventory valuation is set to FIFO and automatic
* [Done] IQD Currency
	- [Done] correct currency for IQD in the Accounting dashboard
	- [Done] General Ledger report shows USD for the IQD currency
* [Done] Uploading all (active) products from the training Odoo to a new Odoo for production
	- Invoicing policy should be on ordered quantites
* [Done] Automatically creating a journal entry for when the invoice/bill is billed
	- Details: When creating a new invoice and is paid, a journal entry will be created to move from accounts payable account (credit) to the journal's account (debit), and vice versa for the bill, from the jouranl's account (credit) to the accounts payable account (debit)
* [Done] Setting a default analytic account to invoice and bill products
* [Done] FIFO and automated is the defaul option for product category
* [Done] Allow the employee to create an invoice from the sale order
	- [Note] It was working this way by default
* [DONE] PO
	- Bundle products are not passed when creating vendor bill products
		- [Note] Makre sure to create a new PO and that the bundle (product) has the ordered policty setup
* [Done] Sales order options: 
	- [Done] Show product bundle item description
	- [Done] Show product part number/SN
	- [NOTE] Hiding product bundle items when creating an SO
		 - e.g.: Hussein want to not show Atlan 300, but shows only Atlan 300 Bundle
	- [To be discussed] Delivery date
* [PAUSED] WH/IN and WH/OUT: Making product quantity done defaluts to demand
* [DONE] Removing IQD 000 from its amount
	- [FIX] The accounting dashboard has trailing currency 0s
		- [Solved] The issue is solved by setting the currency Rounding Factor to 1, and this option must be set at system initialization
* [Done] Expenses
	* [Done] Typically, petty cash can only be set by an accountant and should be recorded by him/her self 
	and not with the regular employee
		- Needs to be resolved for employees without accouting permissions
	- [Done] Showing balance/remaining petty cash amount for the current employee
	- [Done] Petty cash for employee should be selected by default
	- [ISSUE][Solved] Employee is unable to see its balance due to accounting permission restrictions
	- [ISSUE][Solved] Petty cash for IQD is not working
* [Done] Expenses
	- showing total expenses sheet amount according to the selected sheet currency
* [ISSUE][RESOLVED]: auotmatic payment registartion with reset to draft does not takes effect on the journal account
* [Done] Register payment: showing a warning when there is not enough balance for the journal account
* Alpha testing
	- [Done] Purchases
	- [Done] Sales
	- Analytic Accounts
	- [Done] Inventory
	- [Done] Expenses
	- Documents
	- Accounting
		- Petty Cash
	- Project
		- Tasks [Done]
	- Product Maintenance [Done]
	- [Done] CRM
	- [Done] HR
		- Employees check list [Done][
* [Done] Sales order re-design
	- [Done] Sale Order Line: a checkbox to show/hide order line in the quotation print
	- [Done] Allowing to sell with $0
	- [Done] Optional: Show bundle image
	- [Done] Show/Hide company signature
	- [Done] Making company signature bigger
	- Optional: Show part number/SN
	- [Done] Page number should be at the bottom
	- [Done] Product description should be below product name
	- [Done] A checkbox to show/hide product descriptioin in the sales order quotation
	- [Done] Adding Manufacturer (brand) column for the product
	- [Cancelled] Bundle quantity and price should be at the botton of its table cell
* [Done] Warehouse order design
	- changing the header and footer to be the same as the sales order quotation
	- adding "Received From" text above the footer
* [Done] Adding foreign currency IQD
	- [Done] Employee expense (hr.expense)
	- [Done] Main accounting dashboard
* [Done] Accounting dashboard: Showing the total amount for IQDs and USDs
* [Done] PO: Showing inventory status (e.g., the status of the inventory transfer should be like the billing status)
* [Done] Low stock notification reminers
* [Done] Register payment
	- a condition to warn the user when he/she choses a wrong currency (e.g., when the selected journal currency is not the same as the register payment dialog)
* [Done] Payment terms and conditions should be removed from invoice/bill
* [Done] Sale.report: showing/hiding products serial/part number
* [ISSUE][Resolved] Expense reports (hr.expense.sheet) total amount is calculated on the USD only
	- It was caused by calculating a currency rate of 1:1 between the USD and the IQD and was solved by setting the IQD currency rate to a date older thant the expenese sheet dates, e.g., setting it at the begining of the year (Dec 31) 
* User docs
	- Don't allow the uploader to delete the document
* [Done][Under Test] Backup on Google Drive, VPS
* [Done] Accounting reports: separating IQD and USD in the General Ledger
	- General Ledger
	- Partner Ledger
	- Partner Ageing
	- Proft and Loss
	- Balance Sheet
* [Done] showing total amount (without total sum) in the respected currency
	- [Done] Invoices list tree
	- [Done] Sales list tree
	- [Done] Purchases list tree
* Email and activity notifications
	- [Needs Testing] When a new task is created for another employee
	- [Needs Testing] When a sales order is confirmed
	- [Done] Low stock notifications
* Shortcuts menu for commonly used actions
	- Projects
		- Analytic Accounts
		- Down payments
		- Expenses
		- Inventory IN/OUT
	- [Done] Petty cash
	- [Done] Products
	- [Done] Warehouse shortcuts
		- Showing on-hand products
		- Out-of-stock products
		- stock returns
		- Delivered transfers
		- Waiting transfers
	- [Done] Accounting
		- Partner Ageing report
		- Account payable
		- Account receivable
		- Accounts payable dues
* Telegram Notifications
	- Backup
### Tue 8, Feb 2022
* Documents: showing only main categories
* [Done] Odoo sub-domain: erp.infinitytechiq.net
* [Done] petty.cash view: Petty Cash balance shoud show USD currency symbol
* [Done] petty cash balance with IQD shows USD currency conversion
* [Done] Odoo functionality documentation (including the customized parts)
* [Cancelled] Projects: Product SN search to show its tasks
* [Done] invoice/bill amount in IQD should be removed
* [Cancelled]showing payment dialog before posting journal entries
### Thu 10, Feb 2022
* [Done] removing payment terms for invoice
* [Done] removing IQD currency from invoices
* [Done] adding a button for sales orders to reset the web.base.url

```


## SIC-Express

{% img /odoo/customizations/sic-express/sic-express-odoo-home-menu.png Odoo home menu for SIC-Express %}

[This client](https://sic-express.com/) strenthened my accounting exprience further. The great thing is that it is my first time working with an accountant who understands what they needs, and how to do them (clear requirements). I've done also many customizations for them. They're listed below.


```markdown
* Customer
	* [Done] Links for each item
	* [Done] Pictures (screenshots) for all items
		- Thumbnails
		- List view
* Accounting
	- [Done] Bill reference to invoice
	- [Done] Automatically create a bill from the invoice for the existing products
	- [Done] USD and IQD
	- [Done] Adding short description for invoices/bills
	- [Done] Showing foreign amount for partial payments
* Invoicing
	- [Done] Multi-currency (USD + IQD)
	- [Done] show product cost
	- Accounts (as bank and cash)
- [Done] Expenses
	- Salaries
	- Rent
	- Electricity
	- Internet
	- Hospitality
	- Expenses
	- Credit cards expenses and fees
- Accounting
	- [Done] currency exchange between accounts from USD to IQD should reduce the USD account with the amount that is equal to its IQD amount in USD
- Customer ID
- Bill
	- Bill reference should reference invoice 
- General Ledger Report
- [Done] Track changes (cost and public price) for invoice/bills products
- Product category to include shipping type (Economy and Fast)
- [Done] Product template: adding product weight
- [Done] Invoice product lines: showing product weight
- شركة توصيل [Done]
- [Done] Accounting dashboard: Adding currency exchange rate shortcut
- [Done] Product weight kg and pound should be added
- [Done] Contact creation: Individual is set by default instead for Company
- [Done] Contact image (avatar) zoomed when the mouse hovers
- [Done] AmazonSwift: Delivery Invoices before Screenshots menu
- [Done] Product URL: Adding open a new tab button
- [Done] Bills: Bill date should be set by default to current date
- [Done] Delivery invoices number comas should be removed
- [Done] Delivery invoices
	- adding payment state: 'تم الإستلام' + 'إلغاء' + معلق
- [Done] Invoice lines should update the product line info (cost and price) when a new product is created
	- By using "Create and Edit" option when a new product line is inserted in the invoice
- [Done] Invoice: Adding total cost as Order Total
- [Done] Invoice: Adding total weight as Order Weight
	- Total weight in pounds
	- Total weight in kgs
* [Done] Inventory information (item quantity, forecasting, etc...)
* [Cancelled] Preventing WH/OUT when there are not product quantities
* [Cancelled] Multiple warehouse locations (India, and Baghdad)
* [Cancelled] البيع بالآجل 
* [Fixed] Balance sheet is not updating its values
* [Fixed] Balance sheet view report is not the same as the pdf report
* [Done] 133.33 USD to 199,95 IQD (it should be 200,000 IQD
* [Fixed] partial payment caused issues with outstanding payments
* [Unresolved] إستلام 200 دولار عن طريق debit ، بعدها قبض الـ 200 دولار تطلع بالـ outstanding payments
* [Note] draft bill title in Journal entries is created by defaul
* [Done] كشف حساب لأي شخص ، حتى إن كان مصفر
* [Fixed] bug: when an invoice is reset to draft, a new bill (paired bill) is re-created again
* [Done] don't allow the same name when creating a new contact
* [Done] a video on how to create a new user with a limited accounting permissions
- [Done] homepage logo change and package name change
- [already existing for accounting billing permission only] accounting
	- showing dashboard and Overview pages to chief accountants only (regular users only have access to Customers page and onwards)
- [working as expected] automatic logout
	- logs out after 1 minute instead of 10 minutes (600 seconds)
- [Done] adding shipment type (sea, land and air) freights to be showin in the ivnoices tree view as a column (colored like payment status)
- [Done] General Ledger report: adding a button or a checkbox to indicate a matching state (e.g., coloring the line) and the button should ask when to deactivate it.

```



# Raban Al-Safina (Al-Tameer):  October 2017 – April 2020

{% img /odoo/customizations/al-tameer/al-tameer-odoo-home-menu.png Odoo home menu for Al-Tameer %}



My Odoo journy started in Al-Tameer (a sub-branch from Raban Al-Safina), using Odoo 10, where I customized the HR system for this sub-company, and other 7 sub-companies.

At the beginning, Odoo customization, was not easy. Some tasks might took days, even weeks, to finish, due to the bizarre nature of how to develop a plug-in for Odoo and the existence of poor or no documentation. It is awkward and cumbersome; pain with tears to see the results.

My main work was in HR, and the whole idea was to build an HR system + mobile app. I've used Flutter to build the mobile app, because it was cross-platform, and faster to develop.

The Odoo HR customizations was mainly about exporting some xlsx report sheet about employees attendance and if there are any missing checks or delays, or unpaid leaves, then this file is sent to the financial department to cacluate employees salary. It was crucial, because the results will decide how much to pay for each employee. Here is a screenshot of the final xlsx result:

<br>

{% img /odoo/customizations/al-tameer/hr-attendance-summary-xlsx.png xlsx file exported from HR module in Odoo for Al-Tameer %}

<br><br>

Others were about Payroll module, and it was caculating the same xlsx result, but inside Odoo:

<br>

{% img /odoo/customizations/al-tameer/salary-caclculaton-sheet-odoo.png salary calculations sheet in Odoo for Al-Tameer %}

<br>

There were automatic emails that are sent, according to some criteria (e.g., end of the week or when the employee attendance is scoring low).

<br>


{% img /odoo/customizations/al-tameer/my-altameer-hr-attendance-and-leaves-summary-mail-1.png Attendance and leaves summary email using Odoo for Al-Tameer %}

<br>

I also developed a mobile app for this system, using Flutter, and below is the relationship between the app, Odoo and the attendance device/server.

{% img /odoo/customizations/al-tameer/altameerhr-odoo-flutter-diagram.png AlTameer HR + Flutter diagrom %}

<img src="/odoo/customizations/al-tameer/altameer-hr-flutter-english-ui-2.png" width="48%" alt="AlTameerHR flutter app - Checks page" loading="lazy" />

<img src="/odoo/customizations/al-tameer/altameer-hr-flutter-english-ui-3.png" width="48%" alt="AlTameerHR flutter app - Summary page" loading="lazy" />

