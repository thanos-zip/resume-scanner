> ⚠️ This repo is a starting point, not a solution. 
> You will get stuck. That's the point. Google is your best friend.

# Resume Scanner

> Upload a CV and a job description and get instant AI powered feedback on how well they match.

## What You Will Learn
- How to integrate the OpenAI API into a real product
- How to handle file uploads in a FastAPI backend
- How to build a React frontend that communicates with a Python API

## Tech Stack
- Python
- FastAPI
- OpenAI API
- React
- TailwindCSS
- Vercel (frontend deployment)
- Render (backend deployment)

## Getting Started

### Prerequisites
- Python 3.9+ installed
- Node.js 18+ installed
- An OpenAI API key — platform.openai.com
- Free accounts on Vercel and Render

### Installation
```bash
# Backend
git clone https://github.com/thanos.zip/resume-scanner
cd resume-scanner/backend
pip install -r requirements.txt
cp .env.example .env
# Add your OpenAI API key to .env
uvicorn main:app --reload

# Frontend
cd ../frontend
npm install
npm run dev
```

## Project Structure
```
resume-scanner/
├── backend/
│   ├── main.py              # API routes live here
│   ├── parser.py            # PDF text extraction logic here
│   ├── analyzer.py          # OpenAI API calls live here
│   ├── .env.example         # Environment variable template
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── App.jsx          # Main app component
│   │   ├── components/
│   │   │   ├── Upload.jsx   # File upload UI here
│   │   │   └── Results.jsx  # Display feedback here
│   └── package.json
└── README.md
```

## What To Build
- Extract text from an uploaded PDF resume using PyPDF2
- Accept a job description as plain text input
- Send both to OpenAI and prompt it to return match score and missing keywords
- Display the feedback clearly in the React frontend
- Add a loading state while the API processes
- Deploy backend on Render, frontend on Vercel

## Stretch Goals
- Add keyword highlighting — show exactly what's missing
- Support DOCX resume uploads
- Save past scans with a simple database

## Resources
- https://platform.openai.com/docs/api-reference
- https://fastapi.tiangolo.com/tutorial/request-files/
- https://pypdf2.readthedocs.io

---
Built for [@thanos.zip](https://instagram.com/thanos.zip) followers.
