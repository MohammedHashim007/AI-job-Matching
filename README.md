# AI Job Match Agent

A beginner-friendly AI application that compares a candidate resume with a job description and provides a structured job-match analysis.

This project is part of the **AI Projects Series** from **Karthik's Show**.

## Features

- Upload a resume in PDF format
- Extract resume text using `pypdf`
- Convert the resume into a structured candidate profile
- Analyse a pasted job description
- Extract structured job requirements
- Calculate an AI-assisted job match score
- Identify matching skills
- Identify missing skills
- Separate skills that are not clearly evidenced in the resume
- Provide an experience-match summary
- Generate practical improvement recommendations
- Generate 5 role-specific interview questions
- Validate structured AI output using Pydantic

## Tech Stack

- Python
- Streamlit
- pypdf
- Pydantic
- Groq
- python-dotenv

## How It Works

```text
Resume PDF
    ↓
Extract Resume Text
    ↓
Candidate Profile
    ↓
Job Description
    ↓
Job Requirements
    ↓
Compare Candidate vs Job
    ↓
Match Score
    ↓
Matching Skills
    ↓
Missing / Not Evidenced Skills
    ↓
Recommendations
    ↓
Interview Questions
```

## Project Structure

```text
ai-job-search-agent/
├── app.py
├── requirements.txt
├── .env.example
└── .gitignore
```

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/KarthiksShow/ai-job-search-agent.git
cd ai-job-search-agent
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the virtual environment

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_actual_groq_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

You can use `.env.example` as a reference.

> Never commit your real `.env` file or API key to GitHub.

## Run the Application

```bash
streamlit run app.py
```

Then open the local Streamlit URL shown in the terminal.

## How to Use

1. Upload a text-based resume PDF.
2. Paste a job description.
3. Click **Analyse Job Match**.
4. Review the extracted candidate profile.
5. Review the structured job requirements.
6. Check the match score.
7. Review matching skills and missing skills.
8. Review skills that are not clearly evidenced in the resume.
9. Read the improvement recommendations.
10. Use the generated interview questions for preparation.

## Output

The application provides:

- Candidate summary
- Years of experience
- Skills
- Job title
- Required skills
- Preferred skills
- Experience requirement
- Match score
- Matching skills
- Missing skills
- Not-evidenced skills
- Experience-match explanation
- 3 practical recommendations
- 5 interview questions

## Structured Output Validation

Pydantic is used to validate AI-generated JSON.

The project uses structured models such as:

```text
CandidateProfile
JobRequirements
JobMatchResult
```

This helps keep the AI output predictable and easier to use in the application.

## Important Notes

- The match score is AI-assisted and should not be treated as a hiring decision.
- The application should be used as a decision-support tool.
- It does not automatically search LinkedIn, Indeed, or other job portals.
- The current version compares one resume with one pasted job description.
- The AI is instructed not to invent candidate experience or skills.
- Scanned or image-only PDFs may require OCR, which is not included in this version.
- Model output may vary slightly between runs.

## Learning Outcomes

By building this project, you can learn:

- How to process PDF resumes
- How to extract structured information using an LLM
- How to validate LLM output using Pydantic
- How to compare two structured profiles
- How to design AI-assisted scoring workflows
- How to handle missing vs not-evidenced information
- How to generate grounded recommendations
- How to build a practical AI application with Streamlit

## YouTube Tutorial

This project is explained step by step in Tamil on **Karthik's Show**.

The tutorial covers:

- Project setup
- Resume upload
- PDF text extraction
- Candidate profile extraction
- Job description analysis
- Job-match scoring
- Skill-gap analysis
- Recommendations
- Interview-question generation

## Channel

**Karthik's Show**

Learn. Build. Grow.

## Disclaimer

This project is for learning and demonstration purposes.

The AI-generated match score and recommendations should not replace human judgment in job applications or hiring decisions.
