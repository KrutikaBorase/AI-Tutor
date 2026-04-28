# 🤖 AI Tutor – Local AI Study Buddy

AI Tutor is a **privacy-focused, LLM-powered learning assistant** that runs entirely on your local machine. It helps users understand concepts, generate quizzes, and learn interactively without sending any data to external servers.

---

## ✨ Features

### 🎯 Personalized Learning
- Supports multiple education levels (School → PG/PhD)
- Covers subjects like Math, Physics, Computer Science, Biology, History
- Adapts explanations based on user level

### 🤖 Dual Learning Modes
- **Explain Mode:** Step-by-step concept explanations
- **Quiz Mode:** Generate MCQs with answers and explanations

### 🔒 100% Privacy
- Runs completely locally using Ollama
- No data sent to external APIs
- Works offline after setup

### 🧠 Multiple LLM Support
- Gemma3 (best for education)
- DeepSeek Coder (for programming)
- Llama3 (general-purpose)

---

## 🛠️ Tech Stack

- Python  
- Streamlit  
- Ollama (Local LLMs)  
- Prompt Engineering  

---

## 🚀 How It Works

User Input → Prompt → LLM (Ollama) → Response → UI (Streamlit)

---

## ⚡ Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/KrutikaBorase/AI-Tutor.git
cd AI-Tutor
2. Install Dependencies
pip install -r requirements.txt
3. Install LLM Model
ollama pull gemma3
4. Start Ollama
ollama serve
5. Run Application
streamlit run app.py

Then open your browser and go to:

http://localhost:8501
🎮 Usage
Select your education level & subject
Choose mode:
Explain a topic
Generate quiz
Enter queries like:
"Explain neural networks"
"Create a quiz on calculus"
📁 Project Structure
AI-Tutor/
├── app.py
├── requirements.txt
├── README.md
├── assets/
├── docs/
├── config/
└── tests/
🧠 Key Highlights
Built a local LLM-based AI system
Implemented prompt engineering for adaptive learning
Designed an interactive UI for real-time responses
Supports multiple LLMs via Ollama
🗺️ Future Improvements
RAG (PDF-based learning)
Voice interaction
Progress tracking dashboard
Multi-language support
🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

📌 Author

Krutika Borase
Data Science Engineering Student

⭐ Support

If you like this project, consider giving it a ⭐ 
