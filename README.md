# 🔥 HellFire Vault

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-1.5_Flash-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)](LICENSE)

> **Multi-tool web platform built in 12 hours at a hackathon.**  
> Combines a debt-settlement calculator, AI-powered briefing generator, and LAN file sharing — all in one Flask app.

---

## 🎯 What It Does

HellFire Vault is a single Flask web app that bundles **three tools** into one interface:

**1. 💸 Ledger Resolver (Debt Settlement Engine)**  
Upload a CSV of shared expenses between multiple people. The algorithm calculates the *mathematically minimum* number of transactions needed to settle all debts — no more "who owes who" confusion.

**2. 📊 Auto Briefing Generator**  
Converts the settlement results into a clean, ready-to-present `.pptx` slide deck automatically. No manual editing needed.

**3. 📡 LAN File Sharing**  
Hosts the generated slides on a local network so anyone on the same Wi-Fi can download them instantly — no cloud upload, no email needed.

**Bonus: Vecna AI 🤖**  
Google Gemini 1.5 Flash is integrated as an AI assistant to answer questions about the ledger in real time.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3 + Flask |
| Frontend | HTML, CSS, Vanilla JS (no frameworks) |
| Presentation | `python-pptx` |
| AI Assistant | Google Gemini 1.5 Flash (`google-generativeai`) |
| Optional Storage | Supabase |

---

## 📁 Project Structure

```
HELL_FIRE_VAULT/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── .env.example            # Template for environment variables
├── templates/              # HTML templates (Jinja2)
├── static/                 # CSS, JS, images
├── uploads/                # Uploaded CSV files (temp)
└── outputs/                # Generated .pptx files
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- pip

### 1. Clone the repo
```bash
git clone https://github.com/biswanathdash172-sys/HELL_FIRE_VAULT.git
cd HELL_FIRE_VAULT
```

### 2. Install dependencies
```bash
pip install flask python-pptx python-dotenv google-generativeai supabase
```

### 3. Set up environment variables
```bash
# Copy the example file
cp .env.example .env

# Then open .env and fill in your keys
```

Your `.env` should look like:
```
GEMINI_API_KEY=your_gemini_api_key_here
FLASK_SECRET_KEY=your_secret_key_here

# Optional — only if using Supabase storage
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
```

> 💡 Get a free Gemini API key at [ai.google.dev](https://ai.google.dev)

### 4. Run the app
```bash
python app.py
```

Open your browser at: `http://localhost:5000`

---

## 📤 LAN File Sharing (Share with Others on Same Wi-Fi)

1. Find your local IP address:
   - **Windows:** Run `ipconfig` in Command Prompt
   - **Mac/Linux:** Run `ifconfig` or `ip a` in Terminal

2. Share this URL with anyone on the same Wi-Fi:
   ```
   http://<YOUR-LOCAL-IP>:5000/download/campaign_briefing.pptx
   ```
   *Example: `http://192.168.1.55:5000/download/campaign_briefing.pptx`*

> ⚠️ Both devices must be on the **same Wi-Fi network**. This does not work over the internet.

---

## 📸 Screenshots

> *(Add screenshots of your app here — one of the debt upload page, one of the generated PPTX, one of the AI chat)*

---

## 🗺️ What's Next

- [ ] Edit and delete individual debt entries
- [ ] Export settlement summary as PDF
- [ ] Add user authentication
- [ ] Deploy to cloud (Render / Railway)
- [ ] Mobile-responsive UI

---

## ⚡ Built At

This project was designed and shipped in **12 hours** at a hackathon.  
Stack kept intentionally minimal — no React, no Tailwind, just Python + Flask fundamentals.

---

## 📄 License

Open source under the [MIT License](LICENSE).
