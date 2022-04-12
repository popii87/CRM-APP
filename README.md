# CRM-APP

The purpose of CRM:
Input of all leads that are contacted (speakers, delegates, sponsors) which will be kept for annual events.
Advanced analytics for each department and exporting data should be easy
Automation processes for easier management of the leads/contacts


Company structure
Departments
Production
Email sales (Marketing)
Phone sales (Sales)

Job titles (Roles) hierarchy
Production
Production Director (PD)
↘Senior Production Manager (SPM)
    ↘Production Manager (PM)
        ↘Senior Producer (SP)
            ↘Producer (P)
Email Sales
Head of Marketing (HM)
↘Marketing Manager (MM)
    ↘Senior Marketing Executive (SME)
        ↘Junior Marketing Executive (JME)
Senior Research Executive (SRE)
Junior Research Executive (JRE)
Phone Sales
Sales Manager (SM)
↘Assistant Sales Manager (ASM)
     ↘Sales Team Leader (STM)
         ↘Senior Sales Executive (SSE)
             ↘Sales Executive (SE)

Products
Products (conferences) have 3-month cycle.
Product name should be adaptable to changes. 
Choosing a product is mandatory in CRM and all of the Departments must have product assigned.
Product should have option between Active/Disabled, while Active it can be managed. When Disabled should be invisible to all users.


Short explanation of Departments:
 Production
Product is assigned to (P, SP, PM, SPM, PD) by admin and the name of the product should be adaptable to changes while the product is Active. 
After importing leads and converting into Speakers (in Production case the delegates are speakers) those contacts should be available for sales and marketing. Especially if someone becomes a speaker. This should be done with some kind of lock/unlock option. This is valid while the product is Active, and producer should be able to add new leads and potentially convert them into speakers during this active period.

Producer: View only their leads. By request admin sends an export of leads, has no privilege to download or export leads. 
Senior Prodicer: View only their leads. By request admin sends an export of leads, has no privilege to download or export leads. 
Production Manager: View the leads of the Product they are assigned. By request admin sends an export of leads, has no privilege to download or export leads. 
Senior Production Manager: View the leads of the Product/s they are assigned. By request admin sends an export of leads, has no privilege to download or export leads.
Production Director: View the leads of the Product they are assigned. Has privilege to download or export leads.
Dashboard: 
Dashboard in terms of Production roles should contain information about the assigned product, with filter how many emails are sent, how many leads are contacted through email, how many through other source (linkedin, scm etc...) with filters like date, quarter, and some type of gauge with performance meter. 

 Email Sales (Marketing)

Email sales is divided in Research roles – which imports leads and Marketing roles which sends a campaign and afterward communicates with clients.
Junior Research Executive: View only own leads, which needs to have option to import in CSV.
Senior Research Executive: View only own leads, which needs to have option to import in CSV.
Junior Marketing Executive: View only the leads of the Product they are assigned. (Also Researcher’s leads for the assigned product)
Senior Marketing Executive: View only the leads of the Product/s they are assigned. (Also Researcher’s leads for the assigned product)
Marketing Manager: View, only the leads of the Product/s they are assigned. (Also Researcher’s leads for the assigned product/s)
Head of Marketing: View every lead in the CRM (even in past locked Products) except the leads in active products in Sales Department. Has privilege to download or export leads.
Dashboard: The dashboard for Research roles should contain the number of imported leads per week/month or 3 months. A gauge with performance meter if the number leads is hits designated target. Dashboard for Marketing roles should have API Connection with currently Mailwizz and SMTP and fetch all data from campaigns in order to show the data in terms of open rates, bounce stats, replies etc...
Option for admin to lock / unlock previous modules of products – events.

Phone Sales

Phone Sales is divided in teams and to a team is assigned a Product.
Team is usually contained by 3-4 (SE or SSE)
SMTP mailbox connected with CRM software for every user with attachment and templates fields included.
REST API connection with VOIP service (with provided documentation) 
Multiple Dashboard and Performance gauges designated for every role.

Sales Executive: View only the leads that they create. Can export specifically defined CSV or XLSX File which contains the values: Name, Last Name, Job title and Company from the team that they are assigned. – They can download that file whenever needed while the product is Active for that team.
Senior Sales Executive: 
View only the leads that they create. Can export specifically defined CSV or XLSX File which contains the values: Name, Last Name, Job title and Company from the team that they are assigned. – They can download that file whenever needed while the product is Active for that team.
Sales Team Leader:
View the leads from the team and assigned product.
Can export specifically defined CSV or XLSX File which contains the values: Name, Last Name, Job title and Company from the team that they are assigned. 
Dashboard should contain reports of sent emails and call records from all members of the team for assigned product.
Assistant Sales Manager
View the leads from the team and assigned products.
Can export specifically defined CSV or XLSX File which contains the values: Name, Last Name, Job title and Company from the team that they are assigned. 
Dashboard should contain reports of sent emails and call records from all members of the teams for assigned products.
Sales Manager
View the leads from the team and assigned products.
Can export specifically defined CSV or XLSX File which contains the values: Name, Last Name, Job title and Company from the team that they are assigned. 
Dashboard should contain reports of sent emails and call records from all members of the teams for assigned products.


CRM Features
As mentioned the CRM should include following main features.
Departments (Production, Email Sales, Phone Sales)
User Roles (Production: PD, SPM, PM, SP, P), (Email Sales: HM, MM, SME, JME, SRE, JRE), (Phone Sales: SM, ASM, STM, SSE, SE)
User Teams inside Department – Can be arranged by Product (Team1 is working on Product1, Team2 is working Product2, etc...)
User Privileges are set by hierarchy of the Roles.
Product (Conference which is on 3-month basis) 


Unique menu for each department.
SMTP per user.
REST API connections for Yealink VOIP software and Mailwizz email campaign software.
Product renaming and locking/unlocking possibility.
Possibility to define an export of data for specific role.
Dashboard customizability and performance gauges for weekly, monthly and 3-month performance of users.


(CRM Software) 
VTENext 20.04.1 CRM (Self Hosted)
Installed on AWS Lightsail, OS Ubuntu 20.04, LAMP Stack and Hestia panel.
All of the features mentioned above are contained except the EMAIL Sales (Marketing) connection between Mailwizz email marketing software / email delivery system.
Each module is generated per Conference (Product) and it customized by company’s workflow.
The modules are customizable and they can be enabled/disabled.
The Yealink Voip software – gauge meters are set as external widgets which are shown in the CRM as a webpage. 

Yet to manage:
Mailwizz integration in regards of import of lists, segmentation, sending campaigns and reportings from campaigns should be written in the CRM 

(Marketing Software)
Mailwizz 1.9.46 Email Marketing Software (Self Hosted)
Installed on VPS, OS Ubuntu 18.04, LEMP Stack and Hestia panel.
API Documentation
https://api-docs.mailwizz.com/#introduction


