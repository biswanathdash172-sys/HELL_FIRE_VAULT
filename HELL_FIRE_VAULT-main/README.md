# ☄️ HELLFIRE VAULT 🎲

```text
    _   _  ____  _      _      ____  _____  ____  _____     
   / \ / \/  __\/ \    / \    /  __\/__ __\/  __\/  __/     
   | |_| ||  \/|| |    | |    |  \/|  / \  |  \/||  \       
   | | | ||    /| |_/\ | |_/\ |    /  | |  |    /|  /_      
   \_/ \_/\_/\_\\____/ \____/ \_/\_\  \_/  \_/\_\\____\     
                                                            
      _   _  ____  _     _     _____   _  __  _  _  ____    
     / \ / \/  _ \/ \ /\/ \   /__ __\ / |/ / / \/ \/  _ \   
     | | | || / \|| | ||| |     / \   |   /  | || || | \|   
     | |/| || |-||| \_/|| |     | |   |   \  | || || |_/|   
     \_/ \_/\_/ \|\____/\_/     \_/   \_|\_\ \_/\_/\____/   
```

## 📜 The Pitch
Welcome to the **Hellfire Vault** — a centralized arcade terminal built for Hawkins High. This application integrates three distinct systems into a single, cohesive experience:

1. **Project 5 (Ledger Resolver):** Upload a chaotic, multi-person debt CSV and the *Resolution Engine* calculates the absolute mathematical minimum number of payments required to settle all debts.
2. **Project 3 (Automated Briefing Generator):** Instantly synthesizes the math into a neat, presentation-ready `.pptx` slide deck detailing who owes whom and exactly what transactions must take place. 
3. **Project 2 (Secure File Exchange):** Built-in LAN sharing so campaign members can instantly download the generated briefing slides directly from the Dungeon Master’s laptop over local Wi-Fi.

Plus, we’ve tapped into dark magic: **Vecna (Gemini AI)** is connected directly to the vault to answer your questions about the ledger in real time.

---

## 🛠️ Tech Stack: Pure Vibe Coding
This project was designed, built, and deployed in **exactly 12 hours** during a hackathon. We didn't use bloated frameworks—we relied on pure "vibe coding" and robust fundamentals:

- **Backend:** `Python 3` + `Flask`
- **Frontend:** Vanilla `HTML`, `CSS`, and `JavaScript` (No React, No Tailwind... just pure, unadulterated DOM manipulation and CSS Grid/Flexbox).
- **Presentation Logic:** `python-pptx`
- **AI Integration:** Google `google-generativeai` (Gemini 1.5 Flash)
- **Database (Optional/Demo):** `Supabase`

---

## 🕹️ How to Boot up the Arcade
You don't need to be an AV Club member to run this. Just follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/biswanathdash172-sys/HELL_FIRE_VAULT.git
   cd HELL_FIRE_VAULT
   ```

2. **Install dependencies:**
   Make sure you have Python installed, then run:
   ```bash
   pip install flask python-pptx python-dotenv google-generativeai supabase
   ```

3. **Set up Environment Variables:**
   Create a `.env` file in the root directory combining your API keys:
   ```env
   # API Keys for intelligence and storage
   GEMINI_API_KEY=your_gemini_key_here
   FLASK_SECRET_KEY=super_secret_hellfire_key_011
   
   # External DB (Optional depending on active branch)
   SUPABASE_URL=your_supabase_url
   SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Ignite the Server:**
   ```bash
   python app.py
   ```
   *The vault is now open on your local machine at `http://localhost:5000`.*

---

## 🎲 LAN Party Instructions (Project 2 Integration)
To share the generated `.pptx` briefings with your campaign members securely without sending them over the internet:

1. Ensure your laptop (the Host) and your friends' devices are connected to the **same Wi-Fi network**.
2. Find your local IPv4 address. 
   - *Windows:* Open Command Prompt and type `ipconfig`.
   - *Mac/Linux:* Open Terminal and type `ifconfig` or `ip a`.
3. Tell your friends to open their browser and navigate to:
   `http://<YOUR-IPv4-ADDRESS>:5000/download/campaign_briefing.pptx`
   *(Example: `http://192.168.1.55:5000/download/campaign_briefing.pptx`)*
4. The file will download instantly over the local network. 

---

## ⚠️ Hackathon Disclaimer
*This project was built under a strict 12-hour time limit.* 
- In order to meet the deadline, the Secure File Exchange is implemented via a direct REST layer over Local Area Network (LAN) routing rather than a complex remote P2P relay. You must be on the same Wi-Fi.
- Security protocols (like the `Gateway Login`) are currently in "Demo Mode" and accept any credentials to allow for rapid presentation and judging.
- The blockchain hash generation seen in the UI is a local testnet-style simulation designed to showcase the intended cryptographic validation flow.

***"Friends don't lie... but they do pay their debts."*** 🚲🔦
