# A2019 Bot Kurzarbeitergeld/Short-Time Allowance

A detailed instructions file including prerequestits can be found here: [LINK](https://botcenter.automationanywhere.com/Kurzarbeitergeld+Automation+Anywhere+-+readme.pdf?_ga=2.180671847.1358190244.1591715223-560923315.1591715223)

## Purpose of this Bot

### Process Overview
The overall process is shown below.
![Process Overview](/Images/Process_Overview.png)

The reduced hours compensation process consists of several steps that must be performed in this order. After an initial internal review of the prerequisites for reduced hours compensation (hereafter Kug), an agreement must be reached between the company and the works council (if none exists with each affected employee). Then the necessary documents to register short-time work are submitted to the employment agency (notification of loss of work, agreement, etc.). 

The Agentur für Arbeit will then examine the application and either approve or reject it. The employer calculates the Kug independently for each employee concerned and pays it in advance. After payment, the employer submits the benefit application and the Kug payroll list to the  Agentur für Arbeit (this is done monthly). The Employment Agency checks the eligibility requirements and pays the calculated Kug to the employer. After the Kug payment has been made, a final check is performed and the final decision is made by the Agentur für Arbeit.

The payroll list (form 108) must be completed and submitted each month. Completing this list is a repetitive process that follows a strict calculation logic. When carried out manually, this sub-process is both very time-consuming and error-prone. This is at the expense of the employer, as the payment process is delayed if the reimbursement application is incorrect. The free Automation Anywhere A2019 Bot solution is designed to meet precisely this automation potential and thus reduce both time and errors.

### Use Case
As described above, the Bot automates the sub-process of filling the Kug billing list (Form 108). For this purpose, an Excel file filled by the employer with all necessary employee data is processed by the bot. Using this file and the table for calculating the short-time work allowance from the Employment Agency, the short-time work allowance and SV Beitragserstattung are calculated and the Kug payroll list is created.

![Use Case](/Images/Use_Case.png)

If you need to correct a Kug payroll list that has already been submitted, you must correct this manually in the existing payroll list. If employees use the factor procedure, these employees should also be listed in the Excel file, and columns 7-10 should be added manually to the saved PDF after the bot has finished.
Please note that employees who are registered under a different company number in the DEUEV notification must be entered manually in column 2. Please do not enter them in the Excel template.

## Registration for A2019 Community Edition 
There are two options to leverage the Bot:
* Use a private A2019 Instance
* Use the A2019 Community Edition

If you decide to use the A2019 Community Edition you need to register on the following page: [REGISTRATION A2019 COMMUNITY EDITION](https://www.automationanywhere.com/products/enterprise/community-edition/bots)

## Install the Bot Agent/Register your Device
After registration you can login to the A2019 Community Edition ([LINK](https://community.cloud.automationanywhere.digital/#/login?next=/index)).
To enable A2019 to execute Bots on your local device you need to click on the Laptop symbol in the top right corner and then on "Connect devise". 
Then you need to follow the instructions to download and install the Bot Agend and connect you local devise.
![Register Devise](/Images/Register_Devise.png)

## Import the Bot
To import the Bot you need to execute the following steps:
1. Launch the Community Edition Control Room by logging into your Community Edition account. 
1. Navigate to My Bots by clicking Bots in the left panel and then select My Bots ![My Bots](/Images/My_Bots.png)


## Execute the Bot

