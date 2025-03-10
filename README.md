# 📬 Automated Job Application Tracker

### 📌 **Overview**
Keeping track of job applications can feel like a job in itself. Instead of manually updating spreadsheets every time I apply somewhere, I built a script that **scrapes job-related emails from my inbox using the Gmail API** and compiles key details (company name, job title, application date) into a structured **CSV or Google Sheet**.  

It's still a work in progress—but I wanted to share my approach, challenges, and future improvements.

---

### 🛠 **How It Works**
1. **Authenticates with Gmail** using OAuth (so you can access your own inbox securely).  
2. **Searches for job-related emails** based on subject line keywords (e.g., "Thank you for applying," "We received your application").  
3. **Extracts job details** like company name, job title, and application date using **regex + spaCy NLP**.  
4. **Saves everything** into a structured **CSV file** for easy tracking.  

---

### 🔧 **Setup Instructions**
#### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/job-application-tracker.git
cd job-application-tracker

#### **2️⃣ Set Up a Virtual Environment (Optional, but Recommended)**
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

#### **3️⃣ Set Up Google API Credentials**
Go to the Google Cloud Console
Enable the Gmail API and create OAuth 2.0 credentials
Download credentials.json and place it in the project folder
