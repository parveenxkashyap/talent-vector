README.md
```md
# 📄 TalentVector - AI Resume Ranking Platform

Streamlit app that ranks resumes against job descriptions using TF-IDF cosine similarity. Features user authentication, SQLite database, profile management, and ranking history.

## ✨ Features
- 🔐 Secure user registration/login with password hashing
- 📄 PDF resume text extraction (pypdf)
- 🤖 TF-IDF + cosine similarity resume ranking
- 👤 Complete user profile management
- 📊 Personal ranking history with timestamps
- 💾 SQLite database (Resume.db - auto-created)

## 🚀 Quick Start

1. **Clone & Install**
```bash
git clone <repo-link->
cd talentvector
pip install -r requirements.txt
```

2. **Run App**
```bash
streamlit run app.py
```

3. **Access**
- Open: http://localhost:8501
- Register new account or login
- Upload resumes + paste job description → Rank!

## 📁 Project Structure
```
├── app.py              # Main Streamlit app (all-in-one)
├── requirements.txt    # Python dependencies
├── Resume.db          # SQLite DB (auto-generated)
├── .gitignore         # Ignore local files
└── README.md          # This file
```

## 🛠️ Tech Stack
- **Frontend**: Streamlit
- **Backend**: SQLite3
- **PDF Processing**: pypdf
- **ML Ranking**: scikit-learn (TF-IDF + Cosine Similarity)
- **Security**: SHA256 password hashing with salt

## 🔍 How It Works
1. **Text Extraction**: Reads PDF resumes → extracts text
2. **Vectorization**: TF-IDF converts job desc + resumes to vectors
3. **Ranking**: Cosine similarity scores (0-1) → sorts highest first
4. **Persistence**: Results saved to user history automatically

## 📊 Example Output
```
Resume              | Score
-------------------|-------
john_doe_cv.pdf    | 0.847
jane_smith.pdf     | 0.723
resume_batch_1.pdf | 0.612
```

## ⚙️ Configuration
- **Database**: `Resume.db` (local SQLite)
- **Port**: Default 8501 (Streamlit)
- **Session**: Browser cookies (auto-expires)

## 🐛 Troubleshooting
- **PDF errors**: Ensure valid text-based PDFs (not scanned images)
- **No text extracted**: Try different PDF reader or check file format
- **Import errors**: `pip install -r requirements.txt`
- **DB locked**: Delete `Resume.db` and restart

## 🔒 Security Notes
- Passwords: SHA256 + unique salt per user
- Sessions: Streamlit session_state (client-side)
- No external APIs or network calls

## 🤝 Contributing
1. Fork repo
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'feat: add amazing feature'`)
4. Push (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License
MIT License - feel free to use/modify/deploy anywhere.

## 🙏 Acknowledgments
Built with ❤️ using Streamlit, scikit-learn, and SQLite.
```
