📄 PaperSense — AI-Powered Semantic PDF Search Engine

PaperSense is an intelligent, local-first search engine that allows users to upload PDFs and instantly search through them using AI-powered semantic search, TF-IDF ranking, and keyword highlighting.

It is built for students, researchers, and professionals who need Google-like search inside their own documents.

🌟 Key Features
🔍 AI Hybrid Search (Semantic + TF-IDF)

PaperSense combines:

SentenceTransformer embeddings (all-MiniLM-L6-v2)

TF-IDF keyword scoring

Hybrid weighted ranking (0.6 semantic + 0.4 keyword)

This generates highly accurate search results, even for vague queries.

📦 Instant PDF Uploads

Drag & upload PDFs

Auto-indexed on the backend

Available for search immediately

🖼️ Live PDF Thumbnails

Each result shows a thumbnail of the first page using:

PyMuPDF (fitz) page rendering

Fast JPEG stream

Instant preview inside the UI

✨ Modern UI (React + Custom CSS)

Clean dark & light modes

Floating orbits and glass morphism

Smooth interactions

Real-time updates

Search history

Indexed PDF list

Score badges (High / Medium / Low)

💾 Local-First

Everything runs locally:

PDFs never leave your machine

All analysis done on-device

Fully offline capable (except model download)

🧠 Tech Stack
Backend

Python FastAPI

PyPDF2

SentenceTransformers

scikit-learn

PyMuPDF (fitz) — for PDF thumbnails

Uvicorn

Frontend

React (Vite)

Custom CSS (no Tailwind needed)

Fetch API

Responsive layout

🚀 Getting Started (Local Setup)
1. Clone the repo
git clone https://github.com/snorelax08/PaperSense.git
cd PaperSense

📌 Backend Setup
cd papersense-backend
pip install -r requirements.txt
python -m uvicorn api_main:app --reload --port 8000


Backend runs at:

http://127.0.0.1:8000

🖥️ Frontend Setup
cd papersense-frontend
npm install
npm run dev


Frontend runs at:

http://127.0.0.1:5173

🔗 API Endpoints
Route	Method	Description
/search	POST	Run hybrid semantic + keyword search
/upload	POST	Upload and index a new PDF
/files	GET	List all indexed PDFs
/history	GET	Get search history
/thumbnail/{file}	GET	Render & return PDF thumbnail
/reload	POST	Rebuild indexes
/health	GET	API health check
🎨 Screenshots (Add After Recording)

You can add screenshots here like:

![Search UI](assets/screenshot1.png)

🧩 Folder Structure
PaperSense/
│
├── papersense-backend/
│   ├── api_main.py
│   ├── pdfs/
│   ├── requirements.txt
│   └── ...
│
└── papersense-frontend/
    ├── src/
    ├── index.css
    ├── App.jsx
    └── ...

📜 License

MIT License — free to use, modify, and distribute.

🧑‍💻 Developer

Atharwa Vatsyayan (snorelax08)
Created for personal productivity, knowledge management, and document understanding.

If you want, I can also generate:

✅ A clean README banner
✅ A logo for PaperSense
✅ Animated GIF demo section
✅ Deployment instructions for Render/Vercel
✅ A professional “About the Project” section

Just tell me — I can make the README look 10× more premium.
