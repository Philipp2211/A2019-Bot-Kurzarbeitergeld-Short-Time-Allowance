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
To enable A2019 to execute Bots on your local device you need to click on the Laptop symbol in the top right corner and then on "Connect device". 
Then you need to follow the instructions to download and install the Bot Agent and connect you local device.
![Register Device](/Images/Register_Device.png)

## Import the Bot
To import the Bot you need to execute the following steps:
1. Launch the Community Edition Control Room by logging into your Community Edition account. 
1. Navigate to My Bots by clicking Bots in the left panel and then select My Bots. ![My Bots](/Images/My_Bots.png)
1. Click Import Bots in the top right corner. ![Import Bots](/Images/Import_Bots.png)
1. Click Browse and select the Bot (The whole Zip file: "A2019_Bot_Export_Kurzarbeitergeld.zip")  you would like to import. ![Browse Files](/Images/Browse_Files.png)

## Input Data
Required input file:
Excel file filled with all required employee data

If you need to correct a Kug payroll list that has already been submitted, you must correct this manually in the existing payroll list. If employees use the factor procedure, these employees should also be listed in the Excel file, and columns 7-10 should be added manually to the saved PDF after the bot has finished.
Please note that employees who are registered under a different company number in the DEUEV notification must be entered manually in column 2. Please do not enter them in the Excel template.


The following fields in the Excel template are mandatory fields and must be filled in:
* First name 
* Last name
* Insurance number
* Kug downtime 
* Sick pay hours
* Target remuneration (unrounded)
* Actual remuneration (not rounded)
* Income tax class 1-6 (Arabic spelling)
* Power set (1 or 2)
* Region: East or West

The following data are optional and only need to be filled in if the employee is affected, so please leave these fields blank
* Factor (format: 0.xxx)(if employee has chosen factor method, otherwise empty)
* Has the worker been in quarantine during the reference period (yes or empty)


## Execute the Bot
* An Excel template is provided by us. Please save it on your local computer. 
* Enter the required personnel data from your HR systems into the Excel template. 
* One line is entered in Excel for each employee (mandatory data must not remain empty). 
* As an example, the Excel template already contains a data set from Max Mustermann, which you should replace with your real employees.
* Finally, please save the Excel file and close Excel. 
* Open the bot "KUG 108 calculation".
* To run the bot, click on "Run" in the upper right corner.
* In the first dialog, select the completed Excel file on your local computer as the source of the data entry.
* In the next dialog you choose an output directory for the completed KUG 108 forms. 
* Enter the 8-digit "root number" of your company, then your 4-digit department ID.
* Finally, enter the accounting month in the following German notation: "April 2020" ...
* Now the bot automatically fills the PDF forms within seconds with all calculated values for all employees in your Excel file (except column 7-10 for employees with factor methods).
* If you have applied for KUG for employees with factor methods, you will see a note that columns 7-10 have to be added manually to the PDF forms. The relevant employees are automatically highlighted in red in Excel. 
* As soon as the bot is ready, the PDF files will appear in your output directory. After a visual check, send these PDF files to the Federal Employment Agency.

