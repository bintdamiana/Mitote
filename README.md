Mitote: Nahuatl Aware Pronunciation Explorer 🎶

A language preservation project teaching AI to pronounce and explain Nahuatl-rooted words in Mexican Spanish.

What’s a Mitote? (mee-TOH-te)

The word mitote comes from the Nahuatl mitotiqui, meaning “dancer.” Today, it refers to more than just a party—it’s a lively, sometimes chaotic gathering. A mitote might be a backyard full of friends, a noisy family dinner, or a gossip session with neighbors. It’s the sound of joy, culture, and connection.

Why Mitote?

Mitote is a demo tool designed to address a key gap in text-to-speech (TTS) systems: the consistent mispronunciation of Nahuatl origin words in Mexican Spanish. Despite their everyday usage, these words are often mangled or flattened by generic TTS engines.

By integrating curated linguistic data with AI powered synthesis, Mitote delivers accurate, culturally informed pronunciations while preserving the integrity of indigenous language in modern speech technology.

🌟 About the Project

Mitote brings together language preservation and machine learning to tackle a specific linguistic challenge. It offers:

Origin Stories — Explore how Nahuatl words entered and evolved in Mexican Spanish.

Pronunciation Guides — Learn to say each word correctly, with clear phonetic breakdowns.

Accurate Audio — Compare generic TTS output with Nahuatl-aware pronunciation using SSML customization.

This project is built for linguists, developers, educators, and anyone invested in cultural preservation through technology. By giving AI the tools to listen better and speak more truthfully, Mitote helps ensure that the voices of the past are not lost in the language of the future.

🛠️ Tech Stack

Frontend: React (Create React App)

Backend: FastAPI (Python)

AI Model: Microsoft Phi-3-mini-4k-instruct

Vector DB & RAG: ChromaDB

Text-to-Speech: Rime TTS API

Embeddings: sentence-transformers (all-MiniLM-L6-v2)

Additional Libraries: gTTS, uvicorn

📁 Project Structure
mitote/
├── backend/                 
│   ├── app.py              # FastAPI server and logic
│   ├── words.json          # Curated dataset
│   ├── requirements.txt    
│   └── README.md
├── frontend/               
│   ├── public/
│   ├── src/
│   │   ├── App.js
│   │   ├── App.css
│   │   └── ...
│   ├── package.json
│   └── README.md
└── LICENSE

Quick Start
Prerequisites

Node.js (v16+) for the React frontend

Python 3.9+ for the FastAPI backend

A free API key from Rime TTS

1. Clone the Repository
git clone https://github.com/bitdamiana/mitote.git
cd mitote

2. Set Up the Backend
cd backend
python -m venv venv
# On Windows: venv\Scripts\activate
source venv/bin/activate
pip install -r requirements.txt


Edit app.py and insert your Rime API key:

rime_client = RimeClient(api_key="YOUR_KEY_HERE")


Run the backend server:

uvicorn app:app --reload --port 8000


API will be available at http://localhost:8000

3. Set Up the Frontend

In a new terminal:

cd frontend
npm install
npm start


App will launch at http://localhost:3000

💬 Using the Demo

Type a word like "chocolate" or "aguacate" into the input field.

Click "Explore Word"

See the origin story, pronunciation guide, and compare two audio samples:

Generic TTS

Nahuatl-informed pronunciation

📊 The Word Dataset

At the heart of the app is words.json, a curated set of entries. Each word contains structured data for linguistic retrieval and synthesis.

Example Entry:

{
  "word": "mitote",
  "language": "es-MX",
  "origin": "Nahuatl",
  "original_word": "mitotiqui",
  "pronunciation_breakdown": "mee-TOH-te",
  "corrected_ssml": "mi.'to.te",
  "origin_story": "From Nahuatl 'mitotiqui' (dancer), referring to festive ceremonies. Evolved to mean a lively, chaotic, and joyful party or gossip session.",
  "embedding_context": "Word: mitote. Origin: Nahuatl 'mitotiqui'. Meaning: A noisy fuss or lively party. Pronunciation: mi.'to.te"
}

🔧 How It Works: Architecture

Retrieve — The React frontend sends a query to the FastAPI backend.

Augment — The backend uses ChromaDB to find matching data.

Generate — The Phi-3 LLM generates a natural-language explanation.

Synthesize — The backend calls two TTS services:

gTTS: Baseline audio

Rime TTS: Enhanced audio using corrected_ssml

Display — The frontend shows both audio clips side-by-side, with pronunciation and story.

Future Enhancements
🌍 Expanded Language Support: Add Quechua, Guarani, and other indigenous roots
Voice Input: Speak the word via Web Speech API
User Contributions: Suggest new words + etymologies (moderated)
Educational Modules: Quizzes, lessons, and student resources
Advanced TTS Fine-Tuning: Build a custom model for Nahuatl-origin words
Mobile App: React Native frontend for iOS & Android
Historical Audio: Include recordings from native Nahuatl speakers

🙏 Acknowledgments

Rime TTS for their expressive, developer-friendly API

Hugging Face for providing powerful models like Phi-3

The enduring cultural legacy of Nahuatl—its rhythms, meanings, and influence on modern Spanish

🤝 Join the Mitote
This is an open source project, and contributions are welcome. 
Please feel free to open an issue or submit a pull request.
Explore the stories words tell. Preserve linguistic heritage.
Build with us. Speak with us. Celebrate with us.

📄 License This project is licensed under the MIT License. See the LICENSE file for details.

📧 Contact Sahara Al-Madi - Thecyberlingo@gmail.com Project Link: https://github.com/bintdamiana/Mitote
