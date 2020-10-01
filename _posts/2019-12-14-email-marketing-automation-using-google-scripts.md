---
layout: post
title:  "Email Marketing Automation - Using Google Scripts"
author: Pahul Preet Singh Kohli
categories: [Email Marketing, Automation, Google Scripts, Digital Marketing, Digital Strategy, Branding] 
image: assets/images/email.jpeg
description: "Email marketing is the process of delivering a promotional letter, primarily by using email to a customer or group of customers."
comments: false
---

## What is Email Marketing Automation?
Email marketing is the process of delivering a promotional letter, primarily by using email to a customer or group of customers.

## What are the advantages of Email Marketing Automation?

1.	**Scalable Marketing Strategy** : through email marketing automation, the marketing strategy for the company can be scaled, by increased reach to customers.

3.	**Personalization of Customer Experience**: can be achieved by creating a template taking into account customers need. Through automatic personalized email, these clients can be targeted, thereby enhancing the relationship between your client and business.

4. **Improved Productivity**: less time will be spent on emailing customers manually with the automation, thus improving productivity.		

## Email Automation : Using Google Script Code and Sheet 

 1. Create a Google Spread Sheet, with the following [format](https://github.com/Pahulpreet86/Email-Marketing-Automation-Using-Google-Scripts/blob/master/Email%20Automation_%20Using%20Google%20Scripts.xlsx).            
	
 
	 ![image]({{ site.baseurl }}/assets/images/google_spread_sheet.png)

 3. In Google Sheet, go to Tool -> Script Editor.    
![image]({{ site.baseurl }}/assets/images/go_to_script_editor-min.png)

 3. Add the following [code](https://github.com/Pahulpreet86/Email-Marketing-Automation-Using-Google-Scripts/blob/master/Code.gs) in the google script.       
	 
	![image]({{ site.baseurl }}/assets/images/google_script_code-min.png)

 4. Go to File -> New -> HTML File       

	![image]({{ site.baseurl }}/assets/images/create_html_template-min.png)

 5. Copy the following html template [code](https://github.com/Pahulpreet86/Email-Marketing-Automation-Using-Google-Scripts/blob/master/email_template.html), and paste it in the html file created.         

	![image]({{ site.baseurl }}/assets/images/html_file-min.png)

 6. Save the HTML file, with name as email_template.html.  

 7. Once this is done, select function onOpen from toolbar and click on Run.       

	![image]({{ site.baseurl }}/assets/images/select_openup_function-min.png)

 8. Allow permission for email, read, write and edit google sheets.     

	![image]({{ site.baseurl }}/assets/images/allow_permission-min.png)

 9. Now the system with interface has been setup, which can be verified by the addition of Send Email menu option on google sheets.         

 10. Select the cell corresponding to customer email, to whom  you need to send email, then click on Send Email -> Send -> OK. The Sent column in sheet gets updated and the email is sent to the client.       
	![image]({{ site.baseurl }}/assets/images/select_client-min.png)
	![image]({{ site.baseurl }}/assets/images/click_ok-min.png)
	![image]({{ site.baseurl }}/assets/images/sent-min.png)
	![image]({{ site.baseurl }}/assets/images/update_sheet-min.png)


### References

 - [https://mailchimp.com/marketing-glossary/email-automation/](https://mailchimp.com/marketing-glossary/email-automation/)

 - [https://developers.google.com/apps-script/reference/spreadsheet/](https://developers.google.com/apps-script/reference/spreadsheet/)

