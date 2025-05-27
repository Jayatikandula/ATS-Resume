An intelligent, GenAI-powered application that functions as an Applicant Tracking System (ATS). It analyzes resumes, extracts relevant information, and ranks candidates based on job descriptions using Gemini Flash 1.5.

Built with Streamlit, LangChain, and Gemini Flash 1.5, this project brings smart resume filtering and semantic matching into a lightweight and interactive interface.

🚀 Features
📄 Resume Upload – Accepts resumes in PDF format for analysis.

🔍 Job Description Matching – Compares resume content with a given job description.

🧠 LLM-Powered Evaluation – Uses Gemini Flash 1.5 for context-aware matching.

🧩 Ranking & Feedback – Provides match scores and suggests improvements.

🎛️ Streamlit UI – User-friendly interface for uploading and reviewing results.

🛠️ Tech Stack
Frontend: Streamlit

LLM: Gemini Flash 1.5 via LangChain

PDF Parsing: PyMuPDF (fitz) or pdfplumber

Python Libraries: LangChain, pandas, dotenv, fitz, etc.

📁 Project Structure
bash
Copy
Edit
.
├── app.py                    # Main Streamlit app
├── requirements.txt          # Required Python packages
├── utils/
│   ├── resume_parser.py      # Extracts text and sections from PDF resumes
│   ├── job_matcher.py        # Gemini-based matching logic
├── .env                      # Stores API key (not pushed to GitHub)
└── README.md                 # Project documentation
⚙️ Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/ai-resume-ats.git
cd ai-resume-ats
2. Create Virtual Environment
bash
Copy
Edit
python -m venv venv
# Activate it
source venv/bin/activate         # macOS/Linux
venv\Scripts\activate            # Windows
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
🔧 Configuration
Create a .env file in your root directory with the following:

ini
Copy
Edit
GEMINI_API_KEY=your_gemini_flash_key
▶️ Run the App
bash
Copy
Edit
streamlit run app.py
🧠 How It Works
Resume Parsing: The app extracts text from PDF resumes and breaks it into logical sections (e.g., education, experience, skills).

Job Description Input: The user provides a job description or role requirement.

Gemini Flash 1.5 Matching: LangChain routes the resume content and job description to Gemini Flash 1.5, which evaluates and returns a relevance score.

Feedback: The app shows how well the resume matches the role and suggests areas for improvement.

📌 Use Cases
HR teams or startups screening applicants automatically

Students testing their resumes against job descriptions

Resume optimization using AI-based feedback

ATS simulation for interview preparation

🔒 Security Tips
Keep your API keys secure and never commit .env files.

Add authentication if deploying publicly.

Sanitize inputs when handling large-scale deployments.

🤝 Contributing
Want to improve the resume parser or add support for DOCX? PRs are welcome! Please open an issue before making major changes.

