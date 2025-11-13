# Certificate-Eligibility-Check-Automation
End-to-end certification automation built with n8n. The workflow evaluates students’ marks, tasks, and project completion to determine certificate levels, sending real-time results via Gmail integration.

# 🏅 Certificate Eligibility Automation — n8n Workflow

This repository contains an **n8n workflow** built for **Innomatics Research Labs** to automate certificate eligibility generation.  
The workflow reads student performance data, applies logical conditions, and sends personalized emails indicating whether a student qualifies for a **Gold, Silver, Bronze, or Not Eligible** certificate.

## 🎯 Objective

To create a fully automated system that:
- Collects student performance data from Google Forms  
- Reads and processes data using Google Sheets  
- Applies predefined eligibility criteria  
- Sends personalized certificate emails automatically  


## 🧠 Real-Time Project Context

Innomatics Research Labs wanted to reduce manual work in evaluating students for monthly performance-based certificates.  
This n8n workflow ensures that:
- Every student gets evaluated consistently  
- Results are delivered instantly via email  
- The certification process is transparent and data-driven  


## ⚙️ Workflow Logic Overview

| Node Name | Purpose |
|------------|----------|
| **Students Mail Data** | Contains student email addresses to send the Google Form link. |
| **Link to Fill Google Form** | Sends each student an email with a link to submit their details. |
| **Collected Responses** | Reads all submitted responses from Google Sheets. |
| **Checking Certificate Criteria** | Evaluates performance data against eligibility rules. |
| **Switch Node** | Routes students into categories: Gold, Silver, Bronze, or Not Eligible. |
| **Gold / Silver / Bronze / Not Eligible Mail** | Sends personalized emails with the result. |


## 🧮 Certificate Eligibility Conditions

| Certificate | Criteria |
|--------------|-----------|
| 🥇 **Gold** | Marks > 80, Tasks = 10, Assignments = 10, Quiz > 80, Presentation = Yes |
| 🥈 **Silver** | Marks 60-80, Tasks = 10, Assignments = 10, Quiz 60-80, Presentation = Yes |
| 🥉 **Bronze** | Marks 40-60, Tasks = 10, Assignments = 10, Quiz 40-60, Presentation = Yes |
| ❌ **Not Eligible** | Fails to meet any of the above conditions |


## ✉️ Email Templates Used

### 🥇 Gold Certificate
**Subject:** 🎉 Congratulations! You’re Eligible for the Gold Certificate  
**Body:** Hello {{Name}},  
Congratulations! Based on your outstanding performance,  
you are eligible for the **Gold Certificate**.  
Keep up the great work and continue shining! ✨


### 🥈 Silver Certificate
**Subject:** Good Job! You’ve Earned the Silver Certificate  
**Body:** Hello {{Name}},  
Great effort! Based on your results,  
you are eligible for the **Silver Certificate**.  
Keep pushing forward — Gold is just one step away! 🏅  


### 🥉 Bronze Certificate
**Subject:** You’re Eligible for the Bronze Certificate  
**Body:** Hello {{Name}},  
Well done! You’ve qualified for the **Bronze Certificate**.  
Keep practicing and improving to reach Silver or Gold levels next time! 💪 


### ❌ Not Eligible
**Subject:** Update on Your Certificate Eligibility  
**Body:** Hello {{Name}},  
Thank you for your participation.  
Currently, you are **not eligible** for a certificate.  
To qualify, complete all tasks, assignments, and quizzes,  
and improve your marks based on the given criteria.  
You’ve got this — keep trying! 💫 


### 1. Clone the Repository
```bash
git clone https://github.com/<yourusername>/n8n-certificate-eligibility.git
cd n8n-certificate-eligibility
```
### 2. Import Workflow into n8n

Open n8n dashboard.

Go to Workflows → Import from File.

Choose certificate-eligibility-automation.json.

Configure Google and Gmail credentials.

### 3. Test the Workflow

Run manually or set a trigger.

Observe personalized emails being sent.


# 🪪 Author

Ruchita Patil
Email: pruchita565@gmail.com

LinkedIn Profile: www.linkedin.com/in/patil-ruchita
