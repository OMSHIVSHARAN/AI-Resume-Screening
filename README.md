# AI Resume Screening

An AI-powered resume–job description (JD) matcher built with Python, Pydantic, and Groq.

This project analyzes resumes against job descriptions using Large Language Models (LLMs). It extracts structured information from resumes and job descriptions, compares them, and generates a match score with supporting reasoning.

## Features

- **PDF and DOCX Parsing:** Automatically extracts text from PDF and Word resumes.
- **Job Description Analysis:** Uses an LLM to extract job requirements, skills, responsibilities, and education requirements.
- **Structured Data Extraction:** Uses Pydantic schemas to convert unstructured text into structured data.
- **AI-Powered Matching:** Compares candidate skills, experience, and qualifications against job requirements.
- **Match Score:** Generates a match percentage based on the resume and job description.
- **Detailed Reasoning:** Identifies matching skills, missing skills, and relevant experience.
- **Candidate Evaluation:** Provides a match verdict and supporting details for human review.

## Tech Stack

- **Language:** Python
- **LLM:** Groq API
- **Model:** OpenAI GPT-OSS 120B
- **Data Validation:** Pydantic
- **PDF Processing:** pypdf
- **Word Document Processing:** python-docx
- **Environment Management:** python-dotenv, uv

## Project Structure

```text
AI-Resume-Screening/
│
├── resumes/
│   └── resume.pdf
│
├── main.py
├── resume_parser.py
├── pyproject.toml
├── .python-version
├── .gitignore
├── .env
└── README.md
