# ⚡ Quick Reference Card

**Created by:** Vaibhav Gupta (Roll No: 102316130)

## 🚀 ONE-PAGE GUIDE TO GET STARTED

---

## 📥 What You Need

1. **Python 3.8+** - [python.org](https://python.org)
2. **Node.js 16+** - [nodejs.org](https://nodejs.org)
3. **ffmpeg** - Audio processing library

   ```bash
   # Mac
   brew install ffmpeg

   # Ubuntu
   sudo apt install ffmpeg
   ```

---

## ⚙️ Setup (5 Minutes)

### Automated (Recommended)

```bash
# Linux/Mac
chmod +x setup.sh
./setup.sh

# Windows
setup.bat
```

### Manual

```bash
# Backend
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt

# Frontend (new terminal)
cd frontend
npm install
```

---

## 🔐 Configure Email (CRITICAL!)

Edit `backend/app.py` lines 24-27:

```python
class EmailConfig:
    SMTP_SERVER = "smtp.gmail.com"
    SMTP_PORT = 587
    SENDER_EMAIL = "your-email@gmail.com"      # ← Change
    SENDER_PASSWORD = "your-16-char-password"  # ← Change
```

**Get Gmail App Password:**

1. Google Account → Security → 2-Step Verification
2. App Passwords → Generate
3. Copy 16-character password

---

## ▶️ Run Locally

### Terminal 1 - Backend

```bash
cd backend
source venv/bin/activate  # Windows: venv\Scripts\activate
python app.py
```

Backend → `http://localhost:5000`

### Terminal 2 - Frontend

```bash
cd frontend
npm start
```

Frontend → `http://localhost:3000`

---

## 🌐 Deploy to Production

### Frontend (Vercel)

```bash
cd frontend
npm install -g vercel
vercel
```

### Backend (Render.com - FREE)

1. Push to GitHub
2. Go to [render.com](https://render.com)
3. New Web Service
4. Connect repo
5. Set:
   - Build: `pip install -r requirements.txt`
   - Start: `gunicorn app:app`
6. Add environment variables (email config)

---

## 📝 Command Line Usage

```bash
cd backend
python 102303845.py "Artist Name" 20 30 output.mp3
```

**Syntax:**

```
python <file>.py <Singer> <Videos> <Duration> <Output>
```

**Example:**

```bash
python 102303845.py "Arijit Singh" 20 30 mashup.mp3
```

---

## 🎯 Web Interface Usage

1. Open `http://localhost:3000`
2. Enter:
   - Singer name: "Arijit Singh"
   - Videos: 20 (slider)
   - Duration: 30 seconds (slider)
   - Email: your@email.com
   - AI Extraction: ON (recommended)
3. Click "Create My Mashup"
4. Wait ~10 minutes
5. Check email for ZIP file

---

## 📂 File Structure

```
mashup-service/
├── backend/           # Python Flask API
├── frontend/          # React Web UI
├── README.md          # Full documentation
├── QUICKSTART.md      # Setup guide
├── DEPLOYMENT.md      # Deploy guide
├── FEATURES.md        # Resume highlights
├── PROJECT_SUMMARY.md # This overview
└── setup.sh/bat       # Auto setup
```

---

## 🎨 Features

✅ **AI Chorus Detection** - Finds best parts, not just start
✅ **Beautiful UI** - Modern gradient design
✅ **Email Delivery** - Automatic ZIP sending
✅ **High Quality** - 192kbps MP3
✅ **Real-time Updates** - Live progress
✅ **Smart Processing** - Normalized audio, smooth transitions

---

## 🔧 Tech Stack

**Backend:** Python, Flask, librosa, yt-dlp, pydub
**Frontend:** React, Tailwind CSS
**Infrastructure:** ffmpeg, SMTP

---

## 📊 Configuration

### Backend URL (for production)

Edit `frontend/.env`:

```
REACT_APP_API_URL=https://your-backend-url.com
```

---

## 🐛 Quick Fixes

**Email fails?**
→ Check Gmail app password

**Downloads fail?**
→ `pip install --upgrade yt-dlp`

**ffmpeg error?**
→ Install ffmpeg (see top)

**Port in use?**
→ Change port in `app.py`

**CORS error?**
→ Check `REACT_APP_API_URL`

---

## 📚 Full Docs

- **README.md** - Complete documentation
- **QUICKSTART.md** - Detailed setup
- **DEPLOYMENT.md** - Production deploy
- **FEATURES.md** - Resume highlights

---

## 🎓 For Resume

**Key Points:**

- Built AI-powered mashup service
- Intelligent chorus detection with librosa
- Full-stack React + Flask deployment
- Async processing with email delivery
- Modern UI with Tailwind CSS

**Technologies:**
Python • Flask • React • Tailwind • librosa • yt-dlp • pydub • ffmpeg • Vercel • SMTP

---

## ⚡ Speed Run

```bash
# Install ffmpeg first!

# Setup
./setup.sh

# Configure email in backend/app.py

# Terminal 1
cd backend && source venv/bin/activate && python app.py

# Terminal 2
cd frontend && npm start

# Open http://localhost:3000
```

---

## 🎯 Next Steps

1. ✅ Set up locally (5 min)
2. ✅ Test with sample mashup
3. ✅ Deploy to production
4. ✅ Add to portfolio/resume
5. ✅ Customize & extend

---

**You're all set! Happy coding! 🎵**

---

**Questions?** Check the full documentation files included.
