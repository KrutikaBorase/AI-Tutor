# 🛠️ Installation Guide

This guide provides detailed installation instructions for the AI Tutor application across different operating systems.

## System Requirements

### Minimum Requirements

- **OS**: Windows 10+, macOS 10.15+, or Linux
- **RAM**: 8GB (16GB recommended for optimal performance)
- **Storage**: 10GB free space for models and dependencies
- **Python**: 3.7 or higher

### Recommended Requirements

- **RAM**: 16GB or higher
- **Storage**: 20GB+ SSD for faster model loading
- **GPU**: Optional, but can improve performance with compatible models

## Installation Steps

### 1. Install Python

#### Windows

1. Download Python from [python.org](https://www.python.org/downloads/)
2. Run the installer and check **"Add Python to PATH"**
3. Verify the installation:

```bash
python --version
```

#### macOS

```bash
# Using Homebrew
brew install python

# Or download from python.org
```

#### Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

### 2. Install Ollama

#### Windows

1. Download Ollama from [ollama.com](https://ollama.com/download)
2. Run the installer
3. Launch Ollama

#### macOS

```bash
# Using Homebrew
brew install ollama

# Or download from ollama.com
```

#### Linux

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### 3. Clone and Set Up AI Tutor

```bash
# Clone the repository
git clone https://github.com/KrutikaBorase/AI-Tutor.git
cd AI-Tutor

# Create a virtual environment
python -m venv ai-tutor-env

# Activate the virtual environment

# Windows:
ai-tutor-env\Scripts\activate

# macOS/Linux:
source ai-tutor-env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 4. Install an AI Model

#### Quick Setup

```bash
# Install Gemma3
ollama pull gemma3

# Start Ollama if it is not already running
ollama serve
```

#### Alternative Models

```bash
# Programming and computer science
ollama pull deepseek-coder

# General-purpose alternative
ollama pull llama3

# Lightweight option
ollama pull gemma2:2b
```

### 5. Verify the Installation

```bash
# Check installed Ollama models
ollama list

# Start the application
streamlit run app.py
```

Open your browser and navigate to:

`http://localhost:8501`

## Platform-Specific Notes

### Windows

- Use PowerShell or Command Prompt for terminal commands.
- Make sure Python and pip are added to your PATH.
- Windows Defender or firewall settings may require Ollama to be allowed.

### macOS

- Ollama supports Apple Silicon Macs.
- Command Line Tools may be required:

```bash
xcode-select --install
```

### Linux

Install required build tools when necessary:

```bash
sudo apt update
sudo apt install build-essential
```

For GPU acceleration, compatible NVIDIA drivers and CUDA configuration may be required.

## Docker Installation

Docker can be used as an alternative setup method.

### Prerequisites

- Docker installed and running
- Docker Compose installed if using Docker Compose

### Example Docker Compose Configuration

Create a `docker-compose.yml` file:

```yaml
version: '3.8'

services:
  ollama:
    image: ollama/ollama:latest
    ports:
      - "11434:11434"
    volumes:
      - ollama_data:/root/.ollama

  ai-tutor:
    build: .
    ports:
      - "8501:8501"
    depends_on:
      - ollama
    environment:
      - OLLAMA_HOST=ollama:11434

volumes:
  ollama_data:
```

### Example Dockerfile

Create a `Dockerfile`:

```dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8501

CMD ["streamlit", "run", "app.py", "--server.address", "0.0.0.0"]
```

Run the application:

```bash
docker-compose up -d
```

## Troubleshooting Installation

### "Python not found"

- **Windows**: Reinstall Python with **Add Python to PATH** enabled.
- **macOS/Linux**: Try `python3` instead of `python`.

### "pip not found"

Try:

```bash
python -m ensurepip --upgrade
```

or:

```bash
python -m pip
```

### "Ollama connection failed"

Check whether Ollama is running:

```bash
ollama list
```

Start Ollama if required:

```bash
ollama serve
```

### "Model not found"

Check installed models:

```bash
ollama list
```

Install a model:

```bash
ollama pull gemma3
```

### Memory Issues

Try a smaller model:

```bash
ollama pull gemma2:2b
```

You can also close other applications to free system memory.

## Performance Optimization

### For Better Speed

1. Use SSD storage for model files.
2. Use smaller models.
3. Close unnecessary applications.
4. Use GPU acceleration when available.

### For Better Quality

1. Use larger models when your system can handle them.
2. Use sufficient RAM.
3. Use GPU acceleration when available.

## Next Steps

After successful installation:

1. Read the [Usage Guide](usage.md).
2. Try a simple question.
3. Explore the available learning modes.
4. Experiment with different models and education levels.

## Getting Help

For help with installation:

- Check the [Troubleshooting Guide](troubleshooting.md).
- [Report an issue](https://github.com/KrutikaBorase/AI-Tutor/issues)
- Visit [GitHub Discussions](https://github.com/KrutikaBorase/AI-Tutor/discussions)

---

**Success!** 🎉 You should now have AI Tutor running locally on your machine.
