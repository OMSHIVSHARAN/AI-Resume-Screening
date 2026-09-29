AI Resume Screening

An AI-powered resume–job description (JD) matcher built with Python, Pydantic, and Groq.

The project accepts a job description as text and evaluates PDF or Word resumes against it. It extracts structured information from the job description and resumes, then uses an LLM to produce a match score, verdict, and reasoning.

Features

Accepts job descriptions as text input.

Parses PDF and Word (.docx) resumes and extracts text.

Uses Pydantic schemas to structure job-description and resume data.

Uses Groq to compare resume information with job requirements.

Returns a match score, verdict, and supporting details.

Tech Stack

Python

Groq API

Pydantic

pypdf

python-docx

python-dotenv

uv

Project Structure

AI-Resume-Screening/
├── resumes/              # Add PDF or DOCX resumes here
├── main.py
├── resume_parser.py
├── pyproject.toml
├── .python-version
├── .env                  # Create locally; do not commit
└── .gitignore

Setup

1. Clone the repository

git clone https://github.com/OMSHIVSHARAN/AI-Resume-Screening.git
cd AI-Resume-Screening

2. Install dependencies

This project uses uv.

uv sync

3. Configure the Groq API key

Create a .env file in the project root:

GROQ_API_KEY=your_groq_api_key

Replace the placeholder with your own API key. Keep the .env file private; it should never be committed.

4. Add resumes

Place PDF or Word (.docx) resumes in the resumes/ directory.

5. Run

uv run python main.py

Resume Bullet

AI-powered resume–JD matcher built with Python, Pydantic, and Groq.

How It Works

Read the job description provided as text.

Extract structured job requirements using a Pydantic schema and an LLM.

Extract text from PDF or DOCX resumes.

Parse resume content into structured data.

Compare the structured resume with the job requirements using an LLM.

Return a match score, verdict, and reasoning for human review.

Notes

The match score is an LLM-generated estimate, not an objective measure of candidate ability.

Review the extracted information and supporting reasoning before making any hiring-related decision.

Scanned PDFs may require OCR; text extraction alone may not read their contents.

Do not upload real candidates' personal information to a public repository.
