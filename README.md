
🤖 AI Tutor – Local AI Study Buddy
AI Tutor is a privacy-focused, locally running AI learning assistant built with Python, Streamlit, and Ollama.
It helps users understand concepts, generate quizzes, and learn interactively through a simple AI-powered interface.

✨ Features
🎯 Personalized Learning
AI Tutor supports multiple education levels and adapts explanations based on the selected learning level.
- School
- High School
- Graduate
- PG/PhD
  
📚 Multiple Subjects
AI Tutor can be used for different subjects, including:
- Mathematics
- History
- Computer Science
- Physics
- Biology
- Chemistry
  
🤖 Dual Learning Modes
Explain Mode
Provides detailed explanations for learning new concepts or understanding difficult topics.
Example:
Explain neural networks

Quiz Mode
Generates practice questions with answers and explanations.
Example:
Create a quiz on calculus

🔒 Local & Privacy-Focused
AI Tutor is designed to run locally using Ollama.
- AI models run locally on the user's machine.
- No external LLM API is required.
- User conversations can be processed locally.
- The application can continue working offline after the required models and dependencies are installed.

🛠️ Tech Stack
- Python
- Streamlit
- Ollama
- Local LLMs
- Prompt Engineering
  
🧠 Supported AI Models
AI Tutor supports local models through Ollama.
Currently supported model options include:
Gemma3
Suitable for general educational explanations and learning.
DeepSeek Coder
Suitable for programming and Computer Science topics.
Llama3
Suitable for general-purpose educational conversations.

The models available in the application depend on the models installed through Ollama.

🚀 How It Works
User Input
    ↓
Education Level + Subject
    ↓
Prompt Construction
    ↓
Ollama Local LLM
    ↓
Generated Response
    ↓
Streamlit Interface

⚡ Quick Start
1. Clone the Repository
git clone https://github.com/KrutikaBorase/AI-Tutor.git
cd AI-Tutor

2. Install Dependencies
pip install -r requirements.txt

3. Install an AI Model
For example:
ollama pull gemma3

4. Start Ollama
ollama serve

5. Start AI Tutor
streamlit run app.py

Then open:
 http://localhost:8501

🎮 Usage
After launching the application:
1. Select your education level.
2. Select a subject.
3. Choose a learning mode.
4. Enter your question.
5. Submit the question.
6. Review the generated explanation or quiz.
Example Queries
Explain neural networks

Create a quiz on calculus

Explain machine learning algorithms

Explain how gravity works

📸 Application Preview
 
📁 Project Structure
AI-Tutor/
├── app.py
├── requirements.txt
├── requirements-dev.txt
├── CONTRIBUTING.md
├── LICENSE
├── assets/
├── config/
├── docs/
└── tests/

📚 Documentation
Detailed documentation is available in the docs directory.
- [Installation Guide](docs/installation.md)
- [Usage Guide](docs/usage.md)
- [Troubleshooting Guide](docs/troubleshooting.md)
- [Contributing Guide](CONTRIBUTING.md)

🧪 Testing
Development dependencies can be installed using:
pip install -r requirements-dev.txt

Run the test suite:
pytest

Run tests with coverage:
pytest --cov=. --cov-report=html

🗺️ Future Improvements
Potential future improvements include:
- PDF-based learning
- Retrieval-Augmented Generation (RAG)
- Voice interaction
- Progress tracking dashboard
- Multi-language support
- Additional AI model integrations
- Improved learning analytics


🤝 Contributing
Contributions are welcome.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.


👩‍💻 Author
Krutika Borase

B.Tech Data Science Engineering Graduate
GitHub
 https://github.com/KrutikaBorase
LinkedIn
https://www.linkedin.com/in/krutika-borase/

⭐ Support
If you find AI Tutor useful, consider giving the repository a ⭐ on GitHub.
Happy learning! 📚🤖
