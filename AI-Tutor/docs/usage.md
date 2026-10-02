# 📚 Usage Guide

Learn how to effectively use AI Tutor and explore its available learning features.

## Getting Started

### 1. Launch the Application

```bash
cd AI-Tutor
streamlit run app.py
```

Open your browser and visit:

`http://localhost:8501`

### 2. Configure Your Preferences

Use the sidebar to configure your learning preferences.

#### Education Level

- **School**: Simple explanations and basic vocabulary
- **High School**: Moderate complexity and exam-oriented explanations
- **Graduate**: Advanced concepts and technical explanations
- **PG/PhD**: Expert-level and advanced explanations

#### Subject Selection

Available subjects include:

- **Math**: Algebra, calculus, statistics, geometry
- **History**: World history, regional studies, historical analysis
- **Computer Science**: Programming, algorithms, data structures
- **Physics**: Mechanics, thermodynamics, quantum physics
- **Biology**: Cell biology, genetics, ecology, anatomy
- **Chemistry**: Organic, inorganic, physical chemistry

#### Learning Mode

- **Explain a Topic**: Get explanations for concepts and questions
- **Generate a Quiz**: Generate practice questions for a selected topic

## Feature Guide

### 🎯 Explanation Mode

Use Explanation Mode to learn a new concept or understand a difficult topic.

#### Example

```text
Input:
"Explain quadratic equations"

The response can cover:
- Definition and standard form
- Methods of solving
- Examples
- Applications
```

Another example:

```text
Input:
"Explain machine learning algorithms"

The response can cover:
- Different algorithm types
- Core concepts
- Implementation considerations
- Use cases
- Limitations
```

### Best Practices

- **Be specific**: Ask "Explain photosynthesis in plants" instead of "Tell me about plants".
- **Ask follow-up questions** to explore a concept further.
- **Request examples** when a concept is difficult.
- **Ask for clarification** on specific parts of an explanation.

## 🧩 Quiz Mode

Use Quiz Mode to test your understanding and practice a topic.

### Example

```text
Input:
"World War 2"

The generated quiz may include:
- A clear question
- Multiple-choice options
- A correct answer
- An explanation
```

### Quiz Tips

- Be specific about the topic.
- Adjust the education level for the desired difficulty.
- Generate multiple quizzes for additional practice.
- Ask for explanations of incorrect answers.

## Advanced Usage Patterns

### 1. Progressive Learning

Start with a broad topic and gradually explore more specific concepts:

```text
Session 1: "Explain machine learning"
Session 2: "Tell me more about neural networks"
Session 3: "How do convolutional neural networks work?"
Session 4: "Quiz me on CNN architecture"
```

### 2. Exam Preparation

Combine explanation and quiz modes:

```text
Week 1: Learn concepts using Explanation Mode
Week 2: Practice weak areas using Quiz Mode
Week 3: Review topics using both modes
```

### 3. Project-Based Learning

Use AI Tutor to understand concepts related to real-world projects:

```text
"Explain how to build a simple web application"
"What are the steps in data analysis?"
"How do I design a science experiment?"
```

## Model Selection Guide

### 🧠 Gemma3

- **Best for**: General learning and explanations
- **Strengths**: General-purpose educational responses
- **Use when**: You want a general learning assistant

### 💻 DeepSeek Coder

- **Best for**: Programming and computer science
- **Strengths**: Code-focused responses
- **Use when**: Learning programming or technical concepts

### 🚀 Llama3

- **Best for**: General-purpose use
- **Strengths**: Alternative general model
- **Use when**: Another general-purpose option is preferred

## Learning Strategies

### 📖 For Students

#### Daily Study Routine

1. **Review**
   - Quiz yourself on previous topics.
   - Identify areas that need improvement.

2. **Learning Session**
   - Use Explanation Mode for new concepts.
   - Take notes on important points.

3. **Practice**
   - Use Quiz Mode.
   - Review incorrect answers.

### Exam Preparation

1. **Topic Mapping**
   - List the subjects and topics you need to study.
   - Use AI Tutor to understand each topic.

2. **Practice**
   - Generate quizzes regularly.
   - Focus on difficult areas.

3. **Final Review**
   - Use mixed questions.
   - Ask for quick explanations of key concepts.

### 🎓 For Educators

AI Tutor can be used to:

- Generate practice questions.
- Explore different explanation styles.
- Create learning material ideas.
- Provide alternative explanations for students.

## Tips for Effective Learning

### 📝 Note Taking

- Save important explanations in your notes.
- Keep useful quiz questions for revision.
- Create summaries of difficult concepts.

### 🔄 Iterative Learning

- Ask follow-up questions.
- Request alternative explanations.
- Connect related concepts together.

### 🎯 Goal-Oriented Sessions

- Define what you want to learn before starting.
- Focus questions on a specific topic.
- Review difficult concepts before moving on.

## Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Focus browser address bar | `Ctrl + L` |
| Submit message | `Enter` |
| New line in input | `Shift + Enter` |
| Clear chat | Refresh page |

## Privacy and Data

AI Tutor is designed to run locally with Ollama.

### Local Application Data

The application is intended to keep your learning interactions local to your device when using local models.

This includes:

- Questions
- Conversation content
- Model responses
- Learning preferences
- Generated explanations and quizzes

Actual behavior can depend on the configuration and software components you use.

## Common Use Cases

### 📚 Homework Help

```text
"Explain how to solve this physics problem: [paste problem]"
"What are the key themes in Romeo and Juliet?"
"How do I write a good research paper?"
```

### 🧪 Research Projects

```text
"Explain the methodology for statistical analysis"
"How do I design an experiment for [topic]?"
"Explain the background of [topic]"
```

### 📊 Test Preparation

```text
"Generate math practice questions"
"Quiz me on biology topics"
"Create verbal reasoning practice problems"
```

### 💼 Professional Development

```text
"Explain modern software development practices"
"What are the principles of project management?"
"How does financial analysis work?"
```

## Troubleshooting Usage Issues

### AI Responses Are Too Simple or Too Complex

- Adjust the education level.
- Ask the model to simplify or increase the technical depth.

Example:

```text
"Explain this concept at a graduate level."
```

### Quiz Questions Are Too Easy or Too Difficult

- Change the education level.
- Make the topic more specific.

Example:

```text
"Generate a graduate-level organic chemistry quiz."
```

### Explanations Lack Detail

Ask a follow-up question:

```text
"Can you explain that in more detail?"
```

### Model Responses Are Slow

- Try a smaller Ollama model.
- Close unnecessary applications.
- Check available RAM and system resources.

---

Ready to start learning? 🚀
