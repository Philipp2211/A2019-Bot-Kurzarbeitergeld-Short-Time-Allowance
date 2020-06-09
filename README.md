# A2019 Bot Kurzarbeitergeld/Short-Time Allowance

A detailed instructions file including prerequestits can be found here: [LINK](https://botcenter.automationanywhere.com/Kurzarbeitergeld+Automation+Anywhere+-+readme.pdf?_ga=2.180671847.1358190244.1591715223-560923315.1591715223)

## Purpose of this Bot

### Process Overview
The overall process is shown below.
![Process Overview](/Images/Process_Overview.png)

The reduced hours compensation process consists of several steps that must be performed in this order. After an initial internal review of the prerequisites for reduced hours compensation (hereafter Kug), an agreement must be reached between the company and the works council (if none exists with each affected employee). Then the necessary documents to register short-time work are submitted to the employment agency (notification of loss of work, agreement, etc.). 

The Agentur für Arbeit will then examine the application and either approve or reject it. The employer calculates the Kug independently for each employee concerned and pays it in advance. After payment, the employer submits the benefit application and the Kug payroll list to the  Agentur für Arbeit (this is done monthly). The Employment Agency checks the eligibility requirements and pays the calculated Kug to the employer. After the Kug payment has been made, a final check is performed and the final decision is made by the Agentur für Arbeit.

The payroll list (form 108) must be completed and submitted each month. Completing this list is a repetitive process that follows a strict calculation logic. When carried out manually, this sub-process is both very time-consuming and error-prone. This is at the expense of the employer, as the payment process is delayed if the reimbursement application is incorrect. The free Automation Anywhere solution is designed to meet precisely this automation potential and thus reduce both time and errors.


### Use Case

As described above, Automation Anywhere automates the sub-process of filling the Kug billing list (Form 108). For this purpose, an Excel file filled by the employer with all necessary employee data is processed by the bot. Using this file and the table for calculating the short-time work allowance from the Employment Agency, the short-time work allowance and SV Beitragserstattung are calculated and the Kug payroll list is created.

![Use Case](/Images/Use_Case.png)

If you need to correct a Kug payroll list that has already been submitted, you must correct this manually in the existing payroll list. If employees use the factor procedure, these employees should also be listed in the Excel file, and columns 7-10 should be added manually to the saved PDF after the bot has finished.
Please note that employees who are registered under a different company number in the DEUEV notification must be entered manually in column 2. Please do not enter them in the Excel template.


## Registration for A2019 Community Edition 

## Import the Bot

## Execute the Bot

