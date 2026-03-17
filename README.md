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
