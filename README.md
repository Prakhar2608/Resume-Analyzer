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

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/ai-resume-analyzer.git
cd ai-resume-analyzer
2️⃣ Create a virtual environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows
3️⃣ Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
4️⃣ Install NLP models
bash
Copy
Edit
python -m nltk.downloader all
python -m spacy download en_core_web_sm
5️⃣ Set up MySQL database
sql
Copy
Edit
CREATE DATABASE cv;
USE cv;
CREATE TABLE user_data (
    ID INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(500) NOT NULL,
    Email_ID VARCHAR(500) NOT NULL,
    resume_score VARCHAR(8) NOT NULL,
    Timestamp VARCHAR(50) NOT NULL,
    Page_no VARCHAR(5) NOT NULL,
    Predicted_Field VARCHAR(100) NOT NULL,
    User_level VARCHAR(100) NOT NULL,
    Actual_skills TEXT NOT NULL,
    Recommended_skills TEXT NOT NULL,
    Recommended_courses TEXT NOT NULL
);
Update DB credentials in App.py:

python
Copy
Edit
connection = pymysql.connect(
    host='localhost',
    user='root',
    password='YOUR_PASSWORD',
    db='cv'
)
6️⃣ Run the app
bash
Copy
Edit
streamlit run App.py
🔑 Admin Login
Username: rahul

Password: rahulgupta

📌 Notes
Ensure Courses.py contains your course & video lists.

Store your logo in Logo/logo2.png.

The app supports dark mode.

📜 License
This project is licensed under the MIT License.

👨‍💻 Developed by Prakhar Sharma

vbnet
Copy
Edit
