# Recruit AI

## Overview
Recruit AI is an AI-powered resume screening platform that helps recruiters evaluate candidates faster and more consistently. It compares resumes with job descriptions and generates ATS score, strengths and gaps.

## Problem
Recruiters manually review hundreds of resumes, which is time-consuming, inconsistent, and inefficient. Important candidates may be missed due to manual screening.

## Solution
Recruit AI automates resume evaluation using AI by:
- Comparing resumes with job descriptions  
- Generating ATS score 
- Highlighting strengths and skill gaps  
- Providing consistent, data-driven insights  

## Tech Stack
- Frontend: Lovable  
- Backend: n8n  
- AI: Prompt-based evaluation (Gemini)
- Architecture: API-driven workflow

## Backend Architecture (n8n Workflows)

The backend is designed as a modular system with multiple n8n workflows, each exposed as an API and integrated with the frontend (Lovable). Each workflow handles a specific function to ensure scalability, clarity, and maintainability.

### 🔐 Authentication Layer

#### Send Login Code
<img width="1321" height="337" alt="Send login code to recruiter email" src="https://github.com/user-attachments/assets/b806217a-4cbe-4fa1-af6b-a98d10429d88" />

- Generates a one-time login code  
- Sends the code to the recruiter via email  
- Stores email and code for verification  

#### Verify Login Code
<img width="1186" height="480" alt="Verify login code entered by recruiter" src="https://github.com/user-attachments/assets/b4ed553b-3e2f-4fc7-b3d6-07758897e8ec" />

- Validates the login code entered by the recruiter
- Authenticates user access to the platform  
- Returns success or error response to frontend  

### 📄 Job Management Layer

#### Create Job Role
<img width="1130" height="292" alt="Create and Store job description" src="https://github.com/user-attachments/assets/f8d5f238-8dc6-49a3-9c10-064d4b0d2a37" />

- Accepts job title and job description  
- Generates unique Job ID  
- Stores job details mapped to user  

#### List Job Roles
<img width="1064" height="311" alt="Fetch job roles to display to recruiter" src="https://github.com/user-attachments/assets/fb265f08-2df3-4b25-9fa4-a91a9b20ec50" />

- Fetches all job roles for the logged-in user  
- Displays job title and descriptions on dashboard  

### 🤖 AI Evaluation Layer

#### Resume Analysis (ATS)
<img width="1715" height="516" alt="Compare JD and Resume and provide output" src="https://github.com/user-attachments/assets/9c27081a-af10-4d46-a2c4-108d8e50d9c8" />

- Accepts resume (PDF/Text) and job description  
- Extracts text from PDF if required  
- Uses AI model to evaluate resume against JD  
- Generates ATS score, strengths, gaps, and recommendation for interview  

### 📊 Candidate Management Layer

#### Save Candidate Result
<img width="842" height="273" alt="Save cadidate decision Accept or reject" src="https://github.com/user-attachments/assets/da0dd6fa-e7c8-443a-867d-874b7c9c95a4" />

- Stores candidate evaluation results  
- Saves ATS score, decision, and job mapping  

#### Candidate Result Notification
<img width="1128" height="428" alt="Send email to candidate for Accept or Reject" src="https://github.com/user-attachments/assets/ff35b1a6-f234-4db6-9b4d-d64e5af76728" />

- Sends evaluation result to candidate via email  
- Confirms successful communication  

#### List Candidates
<img width="1095" height="290" alt="Fetch and display candidate results to recruiter" src="https://github.com/user-attachments/assets/c9287df4-cad1-4893-be75-89e25d4786c5" />

- Fetches all candidates for a job role  
- Displays email, score, and selection status  

## How It Works
### Recruiter Flow
1. Recruiter logs in using email  
2. Accesses dashboard with job descriptions  
3. Views list of candidates and their screening status  

### Resume Screening Flow
1. Recruiter selects or inputs a Job Description  
2. Enters candidate email ID for sending updates and uploads resume (PDF) or pastes resume text  
3. Backend (n8n) processes and extracts data  
4. AI evaluates resume against JD  
5. Generates structured match score and insights
6. Recruiter can click on 'Reject' or 'Accept' for proceeding with interview
7. On clicking 'Accept' or 'Reject', respective email will be sent to the candidate email ID

### 📊 Output
- ATS Score (0–100)  
- Strengths  
- Gaps  
- Recommendation for interview ('Accept' or 'Reject')  

## 🧩 Key Features
- AI-based resume to JD matching  
- Structured scoring logic  
- Resume upload + text input support  
- Dashboard view for candidates and status tracking  
- API-driven workflow using n8n  

## Impact
- Reduces manual screening effort  
- Improves consistency in evaluation  
- Speeds up hiring decision-making  

## Future Improvements
- Bulk resume upload    
- Advanced analytics dashboard  
