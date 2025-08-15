# Resume-Analyzer
# 📄 AI Resume Analyzer

An AI-powered **Resume Analyzer** built with **Streamlit** that parses resumes, analyzes skills, recommends courses, and provides resume writing & interview tips.  
Includes an **Admin Dashboard** for visualizing user data.

---

## 🚀 Features
- **Resume Parsing**: Extracts details (name, email, phone, skills, etc.) from uploaded PDFs using `pyresparser`.
- **Skill-based Recommendations**: Suggests additional skills and relevant courses.
- **Candidate Level Detection**: Categorizes into Fresher, Intermediate, or Experienced based on resume pages.
- **Resume Score**: Evaluates resumes for important sections (Objective, Declaration, Projects, etc.).
- **Bonus Videos**: Displays random resume writing and interview tips from YouTube.
- **Dark Mode Toggle** 🌙
- **Admin Dashboard**:
  - View aggregated user analytics
  - Pie charts for predicted fields & experience levels
  - Downloadable CSV data

---

## 🛠️ Tech Stack
- **Frontend/UI**: [Streamlit](https://streamlit.io/)
- **Backend/Database**: MySQL (`pymysql`)
- **Resume Parsing**: [pyresparser](https://pypi.org/project/pyresparser/)
- **NLP**: NLTK, spaCy
- **Visualization**: Plotly
- **PDF Handling**: pdfminer3
- **Video Info**: yt_dlp
- **Image Handling**: Pillow

---

## 📂 Project Structure
├── App.py # Main Streamlit app
├── Courses.py # Contains course lists & video links
├── Uploaded_Resumes/ # Folder for uploaded resumes
├── Logo/ # App logo
└── requirements.txt # Python dependencies

