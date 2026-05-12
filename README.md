🤖 AI-Powered HR Recruitment & Verification Workflow (n8n)
An advanced, automated recruitment pipeline built on n8n that not only screens resumes against Job Descriptions but also performs Forensic Background Verification using LinkedIn scraping to detect experience fraud or discrepancies.

🌟 Key Features
Multi-Source Data Merge: Combines Candidate Form data, Resume PDF text, and Google Sheets Job Descriptions.

LinkedIn Profile Scraping: Automatically extracts LinkedIn URLs from resumes and scrapes live profile data via Apify.

AI Background Verification: A dedicated AI Agent compares the Resume with LinkedIn data to find mismatches in Job Titles, Companies, and Dates.

Fraud Detection (Authenticity Score): Generates an "Authenticity Score". If a candidate lies about their experience, they are automatically disqualified.

Smart Scoring & Shortlisting: Evaluates technical skills, "Nice to Have" requirements, and cultural fit.

Automated Merit Lists: * Merit List 1: High-score candidates get an instant interview invite.

Merit List 2 (Waitlist): Borderline candidates get a "Keep in Touch" email.

Automated Rejections: Low-score or "Failed Verification" candidates receive a constructive feedback email.

HR Notifications: Sends detailed alerts to Slack with a "Red Flag" warning if fraud is detected.

🛠️ Tech Stack
Automation: n8n

LLM / AI: OpenAI GPT-4o / OpenRouter

Data Extraction: Apify (LinkedIn Profile Scraper)

Storage: Google Sheets

Communication: Slack, Gmail/Postmark

📋 How It Works
Trigger: Candidate submits a form with their Resume.

Parsing: Extract Resume Text node converts PDF to text.

OSINT Step: JavaScript Code node extracts the LinkedIn URL.

Verification: AI compares LinkedIn data vs Resume text.

Final Scoring: Main AI Agent calculates the final match % based on skills + verification status.

Action: The workflow sends emails and logs data to Google Sheets & Slack.

🚀 Deployment
Import the HR_Resume_Screening.json into your n8n instance.

Configure your credentials for:

OpenRouter (AI)

Apify (LinkedIn Scraping)

Google Sheets & Gmail

Slack

Hit Publish.
