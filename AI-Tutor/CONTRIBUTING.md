# 🤝 Contributing to AI Tutor

Thank you for your interest in contributing to AI Tutor! This guide will help you get started with contributing to the project.

## 🚀 Quick Start for Contributors

### 1. Fork and Clone

```bash
# Fork the repository on GitHub

# Clone your fork
git clone https://github.com/YOUR_USERNAME/AI-Tutor.git
cd AI-Tutor

# Add the original repository as upstream
git remote add upstream https://github.com/KrutikaBorase/AI-Tutor.git
```

### 2. Set Up Development Environment

```bash
# Create virtual environment
python -m venv ai-tutor-dev

# Activate on macOS/Linux
source ai-tutor-dev/bin/activate

# Activate on Windows
ai-tutor-dev\Scripts\activate

# Install project dependencies
pip install -r requirements.txt

# Install development dependencies
pip install -r requirements-dev.txt

# Install pre-commit hooks
pre-commit install
```

### 3. Create a Branch

```bash
# Create a feature branch
git checkout -b feature/your-feature-name

# Or create a bug-fix branch
git checkout -b fix/issue-number
```

## 📋 Types of Contributions

### 🐛 Bug Reports

Found a bug? Help us improve AI Tutor!

Before reporting:

- Check existing issues
- Test with the latest version
- Gather relevant system information

Include in your report:

- Clear description of the bug
- Steps to reproduce
- Expected behavior
- Actual behavior
- Operating system and Python version
- Error messages or logs
- Relevant screenshots, if applicable

### 💡 Feature Requests

Have an idea for improving AI Tutor?

Before requesting a feature:

- Check existing issues and feature requests
- Consider whether the feature fits the project scope
- Describe the use case clearly
- Consider possible implementation requirements

Include in your request:

- Clear description of the proposed feature
- Use cases and expected benefits
- Possible implementation approach
- Mockups or examples, if applicable

### 📖 Documentation

Documentation improvements are always welcome!

Areas to contribute:

- Fix typos and grammar
- Add missing information
- Improve explanations and examples
- Improve installation or usage instructions
- Add tutorials or guides
- Keep documentation consistent with the current project structure

### 🧪 Code Contributions

Code contributions can include:

- Bug fixes
- Performance improvements
- AI model integrations
- UI/UX improvements
- Error-handling improvements
- Test coverage improvements
- Code quality improvements

## 🛠️ Development Guidelines

### Code Style

The project follows Python best practices and PEP 8 style guidelines.

Use:

- Clear and descriptive variable names
- Type hints where appropriate
- Docstrings for important functions
- Small and maintainable functions
- Comments for complex logic

Example:

```python
def format_prompt(education_level: str, subject: str, prompt: str) -> str:
    """
    Format a prompt for the AI model based on education level and subject.

    Args:
        education_level: The student's education level.
        subject: The subject area.
        prompt: The user's input prompt.

    Returns:
        A formatted prompt string.
    """
    return f"""
    You are a {education_level}-level {subject} tutor.
    Explain the following clearly and step by step:

    {prompt}
    """
```

## 📁 Project Structure

The current project structure is:

```text
AI-Tutor/
├── app.py
├── assets/
│   └── README.md
├── config/
│   └── models.yaml
├── docs/
│   ├── installation.md
│   ├── troubleshooting.md
│   └── usage.md
├── tests/
│   └── test_app.py
├── image.png
├── requirements.txt
├── requirements-dev.txt
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

### Main Files and Directories

- `app.py` - Main Streamlit application
- `config/models.yaml` - AI model configuration and recommendations
- `docs/` - Installation, usage, and troubleshooting documentation
- `tests/` - Automated tests
- `assets/` - Documentation assets and asset-related information
- `requirements.txt` - Runtime dependencies
- `requirements-dev.txt` - Development and testing dependencies
- `README.md` - Project overview and getting started guide
- `CONTRIBUTING.md` - Contribution guidelines
- `LICENSE` - Project license

## 🧪 Testing

Before submitting changes, run the available tests.

### Run all tests

```bash
pytest
```

### Run tests with coverage

```bash
pytest --cov=. --cov-report=html
```

### Run the application tests

```bash
pytest tests/test_app.py
```

### Run integration tests

```bash
pytest -m integration
```

Some integration tests require a working Ollama installation and locally available models.

### Testing Guidelines

When adding new functionality:

- Add unit tests where appropriate
- Test normal and edge-case behavior
- Test error handling
- Mock external dependencies when appropriate
- Make sure existing tests continue to pass

## 🔄 Git Workflow

### Commit Messages

Use clear and descriptive commit messages.

Recommended format:

```text
type(scope): description
```

Examples:

```text
feat(models): add support for a new model

fix(ui): improve model selection handling

docs(readme): update installation instructions

test(app): add model detection tests

refactor(app): simplify model ordering logic
```

Common commit types:

- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Code formatting or style changes
- `refactor` - Code restructuring
- `test` - Adding or updating tests
- `chore` - Maintenance tasks

## 🔀 Pull Request Process

### Before submitting a pull request

1. Sync your branch with the upstream repository:

```bash
git fetch upstream
git checkout main
git pull upstream main
```

2. Return to your feature branch:

```bash
git checkout feature/your-feature-name
```

3. Rebase or merge the latest changes if required.

4. Run the tests:

```bash
pytest
```

5. Review your changes:

```bash
git diff
```

6. Update documentation if your changes affect project usage or setup.

### Pull Request Requirements

Please include:

- A clear title
- A concise description of the changes
- The reason for the change
- Related issue number, if applicable
- Tests or validation performed
- Screenshots for UI changes, when useful
- Documentation updates when required

### Pull Request Template

```markdown
## Description

Brief description of the changes.

## Type of Change

- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Refactoring
- [ ] Test improvement

## Testing

- [ ] Tests pass locally
- [ ] Added or updated tests
- [ ] Manual testing completed

## Checklist

- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Documentation updated if needed
- [ ] No unnecessary changes included
```

## 🤖 AI Model Contributions

AI Tutor uses Ollama for local AI model integration.

When adding support for a new model:

1. Verify that the model works with Ollama.
2. Add the model to the appropriate configuration.
3. Update documentation if necessary.
4. Add or update tests where appropriate.
5. Explain the model's intended use case.

The model configuration is maintained in:

```text
config/models.yaml
```

Example configuration:

```yaml
preferred_models:
  - "new-model:latest"

subject_models:
  "Computer Science": "new-model"
```

## 🎨 UI/UX Improvements

AI Tutor uses Streamlit for its user interface.

When making UI changes:

- Keep the interface simple and accessible
- Maintain consistency with the existing design
- Avoid unnecessary complexity
- Test the interface locally
- Consider different screen sizes where applicable

## ⚡ Performance Improvements

When improving performance:

- Identify the actual bottleneck first
- Avoid unnecessary model or API calls
- Use caching where appropriate
- Keep the implementation readable
- Measure the effect of performance changes

Example:

```python
@st.cache_data
def expensive_operation():
    # Cache expensive operations when appropriate
    pass
```

## 📖 Documentation Improvements

Documentation contributions are encouraged.

When updating documentation:

- Keep instructions clear and accurate
- Use examples where helpful
- Keep commands up to date
- Maintain consistent Markdown formatting
- Update related documentation when necessary

Documentation is located in:

```text
docs/
├── installation.md
├── troubleshooting.md
└── usage.md
```

## 🔧 Development Setup

### Required Tools

- Python 3.7+
- Git
- Ollama
- A code editor such as VS Code

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Install Development Dependencies

```bash
pip install -r requirements-dev.txt
```

### Start Ollama

Make sure Ollama is installed and running.

```bash
ollama serve
```

Then install a supported model, for example:

```bash
ollama pull gemma3
```

Other supported models may include:

```bash
ollama pull llama3
ollama pull deepseek-coder
```

## 🖥️ Running the Application

From the project directory:

```bash
streamlit run app.py
```

The application will open in your browser.

## 🔍 Code Review Process

### For Contributors

- Keep pull requests focused
- Respond to review feedback
- Make requested changes clearly
- Keep commit messages descriptive
- Test changes before requesting review

### For Reviewers

- Be respectful and constructive
- Focus on code quality and maintainability
- Check functionality and edge cases
- Verify documentation when relevant
- Test changes when possible

## 🏆 Recognition

Contributors may be recognized through:

- GitHub contributor history
- Project documentation
- Release notes
- Special acknowledgements

## 📞 Getting Help

For questions or problems:

- Check the project documentation
- Review the troubleshooting guide
- Search existing GitHub issues
- Open a new issue when necessary

Useful documentation:

- [Installation Guide](docs/installation.md)
- [Usage Guide](docs/usage.md)
- [Troubleshooting Guide](docs/troubleshooting.md)

## 🎉 Thank You!

Thank you for contributing to AI Tutor!

Whether you report a bug, improve documentation, suggest a feature, add tests, or contribute code, every contribution helps improve the project.

---

**Repository:** https://github.com/KrutikaBorase/AI-Tutor

**Author:** Krutika Borase
