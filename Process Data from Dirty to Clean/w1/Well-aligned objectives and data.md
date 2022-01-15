Well-aligned objectives and data
================================

You can gain powerful insights and make accurate conclusions when data is well-aligned to business objectives. As a data analyst, alignment is something you will need to judge. Good alignment means that the data is relevant and can help you solve a business problem or determine a course of action to achieve a given business objective.

In this reading, you will review the business objectives associated with three scenarios. You will explore how clean data and well-aligned business objectives can help you come up with accurate conclusions. On top of that, you will learn how new variables discovered during data analysis can cause you to set up data constraints so you can keep the data aligned to a business objective.  

Clean data + alignment to business objective = accurate conclusions
-------------------------------------------------------------------

### Business objective

Account managers at Impress Me, an online content subscription service, want to know how soon users view content after their subscriptions are activated. 

![Image of a web video player and image of an analog clock set to 3:03 ](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uGU6wRn8SXClOsEZ_NlwUQ_1f46ab637fc641acafae6f862c23fc46_Screen-Shot-2021-01-25-at-12.38.21-PM.png?expiry=1642377600000&hmac=HLpk-24dlVI9G1liVKKaXaIVfXPc8XnfUY_PObmYsbo)

To start off, the data analyst verifies that the data exported to spreadsheets is clean and confirms that the data needed (when users access content) is available. Knowing this, the analyst decides there is good alignment of the data to the business objective. All that is missing is figuring out exactly how long it takes each user to view content after their subscription has been activated.

Here are the data processing steps the analyst takes for a user from an account called V&L Consulting. (These steps would be repeated for each subscribing account, and for each user associated with that account.)

### Step 1

|Data-processing step |Source of data |
| --- | --- |
|Look up the activation date for V&L Consulting |Account spreadsheet |

Relevant data in spreadsheet:

![Screenshot of two columns of a spreadsheet for Account Name and Activation Date. The date 10/21/2019 is highlighted](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GnNRQZl4QkSzUUGZeBJEzg_90d6857f15ac4d24ae9df6e5c5b4e0fa_Screen-Shot-2021-01-18-at-6.29.11-PM.png?expiry=1642377600000&hmac=_ZLlHi3S1_r3Yboa1sJpSnO1MGJfi79BqV35lWv-SHE)

Result: October 21, 2019

### Step 2

|Data-processing step|Source of data |
| --- | --- |
|Look up the name of a user belonging to the V&L Consulting account |Account spreadsheet (users tab) |

Relevant data in spreadsheet:

![Screenshot of two columns of a spreadsheet for Account Name and Users. The name Maria Ballantyne is highlighted](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/R-nkA9w1Riep5APcNSYnRA_7480900c4f204ffb9421199fd8bf32c8_Screen-Shot-2021-01-18-at-6.27.24-PM.png?expiry=1642377600000&hmac=tBUPzI_OsayIasQdfgygI69xodSknKFShAbki_JOtk4)

Result: Maria Ballantyne

### Step 3

| Data-processing step                            | Source of data                  |
| ----------------------------------------------- | ------------------------------- |
| Find the first content access date for Maria B. | Content usage spreadsheet


Relevant data in spreadsheet:

![Screenshot of two columns of a spreadsheet for Users and Access Dates. The date 10/31/2019 is highlighted](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_Mn53wNpR0aJ-d8DaedG4w_ecc7521519ea4b4c810dd80bc0f54b9d_Screen-Shot-2021-01-18-at-6.35.48-PM.png?expiry=1642377600000&hmac=C0KW5W5AhBx6OhXBTB389TXwxmHA4ehAsL6U9zgONd4)

Result: October 31, 2019

### Step 4

| Data-processing step                                                       | Source of data              |
| -------------------------------------------------------------------------- | --------------------------- |
| Calculate the time between activation and first content usage for Maria B. | New spreadsheet calculation |

Relevant data in spreadsheet:

![Screenshot of spreadsheet with Account, Users, Activation Date, 1st Access Date, and Number of Days. Number 10 is highlighted](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jV8hcatCTq2fIXGrQr6ttw_b4f3452496b543bd9e46716485d5175e_Screen-Shot-2021-01-18-at-6.41.56-PM.png?expiry=1642377600000&hmac=YYtBZHVNjkz7hdm3op_mvfZFVLeMzwgFHyRy0WVjz38)

Result: 10 days

### Pro tip 1

In the above process, the analyst could use VLOOKUP to look up the data in Steps 1, 2, and 3 to populate the values in the spreadsheet in Step 4. [VLOOKUP](https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1 "This link takes you to the Microsoft Support page for the VLOOKUP function.") is a spreadsheet function that searches for a certain value in a column to return a related piece of information. Using VLOOKUP can save a lot of time; without it, you have to look up dates and names manually.

R​efer to the [VLOOKUP](https://support.google.com/docs/answer/3093318?hl=en "This link takes you to the VLOOKUP help page for Google Sheets.") page in the Google Help Center for how to use the function in Google Sheets.

### Pro tip 2

In Step 4 of the above process, the analyst could use  the DATEDIF function to automatically calculate the difference between the dates in column C and column D. The function can calculate the number of days between two dates. 

Refer to the Microsoft Support [DATEDIF](https://support.microsoft.com/en-us/office/datedif-function-25dba1a4-2812-480b-84dd-8b32a451b35c "DATEDIF") page for how to use the function in Excel. The [DAYS360](https://support.microsoft.com/en-us/office/days360-function-b9a509fd-49ef-407e-94df-0cbda5718c2a "DAYS360") function does the same thing in accounting spreadsheets that use a 360-day year (twelve 30-day months).

R​efer to the [DATEDIF](https://support.google.com/docs/answer/6055612?hl=en "This link takes you to the Google Help Center page for the DATEIF function.") page in the Google Help Center for how to use the function in Google Sheets.

Alignment to business objective + additional data cleaning = accurate conclusions 
----------------------------------------------------------------------------------

### Business objective

Cloud Gate, a software company, recently hosted a series of public webinars as free product introductions. The data analyst and webinar program manager want to identify companies that had five or more people attend these sessions. They want to give this list of companies to sales managers who can follow up for potential sales.  

![An image of a group of people chatting and an image of an online page](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kfJtDm53S4iybQ5ud9uIaQ_c2812e7377fe4f48bc044561996b3d92_Screen-Shot-2021-01-25-at-12.46.54-PM.png?expiry=1642377600000&hmac=u6jYXX-hmWmPN4T-mJcKXwJDsc8nDaBLgXr13R2gT0I)

The webinar attendance data includes the fields and data shown below.

||||
| ------------- | ------------------------------ | ----------------------------------------------------- |
| Name          | <_First name_\> <_Last name_\> | This was required information attendees had to submit |
| Email Address | xxxxx@_company_.com            | This was required information attendees had to submit |
| Company       | <_Company name_\>              | This was optional information attendees could provide |

### D​ata cleaning

The webinar attendance data seems to align with the business objective. But the data analyst and program manager decide that some data cleaning is needed before the analysis. They think data cleaning is required because:

-   The company name wasn't a mandatory field. If the company name is blank, it might be found from the email address. For example, if the email address is username@google.com, the company field could be filled in with Google for the data analysis. This data cleaning step assumes that people with company-assigned email addresses attended a webinar for business purposes.

-   Attendees could enter any name. Since attendance across a series of webinars is being looked at, they need to validate names against unique email addresses. For example, if Joe Cox attended two webinars but signed in as Joe Cox for one and Joseph Cox for the other, he would be counted as two different people. To prevent this, they need to check his unique email address to determine that he was the same person. After the validation, Joseph Cox could be changed to Joe Cox to match the other instance.

Alignment to business objective + newly discovered variables + constraints = accurate conclusions 
--------------------------------------------------------------------------------------------------

### Business objective

An after-school tutoring company, A+ Education,  wants to know if there is a minimum number of tutoring hours needed before students have at least a 10% improvement in their assessment scores.

![An image of a person writing on a pad and an image of a gauge meter](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XIgx4gCvR5-IMeIAr2efDA_a28452c4b7874cd68547049e163f0c2b_Screen-Shot-2021-01-25-at-12.52.43-PM.png?expiry=1642377600000&hmac=Ve1EDtQ9o-rH3O5Ju_bCDc1aTSeDw_sGsR2-QxQ0vbM)

The data analyst thinks there is good alignment between the data available and the business objective because:

-   Students log in and out of a system for each tutoring session, and the number of hours is tracked

-   Assessment scores are regularly recorded  

### D​ata constraints for new variables

After looking at the data, the data analyst discovers that there are other variables to consider. Some students had consistent weekly sessions while other students had scheduled sessions more randomly even though their total number of tutoring hours was the same. The data doesn't align as well with the original business objective as first thought, so the analyst adds a data constraint to focus only on the students with consistent weekly sessions. This modification helps to get a more accurate picture about the enrollment time needed to achieve a 10% improvement in assessment scores. 

Key takeaways
-------------

Hopefully these examples give you a sense of what to look for to know if your data aligns with your business objective. 

-   When there is clean data and good alignment, you can get accurate insights and make conclusions the data supports.

-   If there is good alignment but the data needs to be cleaned, clean the data before you perform your analysis. 

-   If the data only partially aligns with an objective, think about how you could modify the objective, or use data constraints to make sure that the subset of data better aligns with the business objective.

Mark as completed

Like

Dislike

Report an issue