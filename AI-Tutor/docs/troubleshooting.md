# 🔧 Troubleshooting Guide

This guide helps you resolve common issues with AI Tutor.

## Quick Diagnosis

Before troubleshooting a specific issue, verify the following:

- [ ] Ollama is installed and running
- [ ] At least one AI model is downloaded
- [ ] Python dependencies are installed
- [ ] Ports `8501` and `11434` are available
- [ ] Sufficient RAM and storage are available

## Common Issues and Solutions

### 1. No Ollama Models Found

#### Symptoms

- The model list is empty.
- You see a message indicating that no Ollama models are available.
- Conversations cannot be started.

#### Diagnosis

```bash
ollama list
```

If Ollama is not running, start it:

```bash
ollama serve
```

#### Install a Model

```bash
ollama pull gemma3
ollama list
```

#### Restart Ollama

```bash
ollama serve
```

## 2. Connection Errors

### Symptoms

- "Error connecting to Ollama"
- "Connection refused"
- The application hangs when starting a conversation

### Diagnosis

Test the Ollama API:

```bash
curl http://localhost:11434/api/version
```

Check whether port `11434` is being used:

```bash
netstat -an | grep 11434
```

### Possible Solutions

#### Port Conflict

**macOS/Linux:**

```bash
lsof -i :11434
```

**Windows:**

```bash
netstat -ano | findstr :11434
```

Restart Ollama after resolving the conflict.

#### Firewall Issues

- **Windows**: Allow Ollama through Windows Firewall.
- **macOS**: Check firewall and application permissions.
- **Linux**: Check firewall rules for port `11434`.

## 3. Model Performance Issues

### Symptoms

- Responses are very slow.
- The application becomes unresponsive.
- CPU or RAM usage becomes high.

### Check System Resources

```bash
# Linux
free -h

# macOS/Linux
top

# Windows
taskmgr
```

Check installed models:

```bash
ollama list
```

### Use a Smaller Model

```bash
ollama pull gemma2:2b
```

You can also remove unused models:

```bash
ollama rm llama3
```

### General Optimization

- Close unnecessary applications.
- Use SSD storage.
- Increase available RAM or swap when necessary.
- Use a smaller model on resource-limited systems.

## 4. Streamlit Issues

### Symptoms

- `streamlit` command is not recognized.
- The application does not start.
- The browser does not open automatically.

### Check Streamlit

```bash
pip list | grep streamlit
```

Test Streamlit:

```bash
streamlit hello
```

### Reinstall Dependencies

Activate the virtual environment first.

**macOS/Linux:**

```bash
source ai-tutor-env/bin/activate
```

**Windows:**

```bash
ai-tutor-env\Scripts\activate
```

Then run:

```bash
pip install -r requirements.txt --force-reinstall
```

### Run Streamlit on Another Port

```bash
streamlit run app.py --server.port 8502
```

## 5. Model Loading Errors

### Symptoms

- "Model not found"
- A selected model does not work.
- The application cannot load a specific model.

### Check Model Names

```bash
ollama list
```

Test a model directly:

```bash
ollama run gemma3 "Hello, how are you?"
```

### Reinstall a Model

```bash
ollama rm gemma3
ollama pull gemma3
```

Make sure the model name used by the application matches the model available in Ollama.

## 6. UI and Display Issues

### Symptoms

- Broken layout
- Missing sidebar
- Incorrect text formatting

### Try the Following

- Clear your browser cache.
- Open the application in private/incognito mode.
- Try another browser.
- Make sure JavaScript is enabled.
- Disable browser extensions that may interfere.

### Clear Streamlit Cache

```bash
streamlit cache clear
```

## 7. Memory and Resource Issues

### Symptoms

- Out-of-memory errors
- System becomes slow
- Application crashes unexpectedly

### Check System Resources

**Linux:**

```bash
htop
```

**macOS:**

Use Activity Monitor.

**Windows:**

Use Task Manager.

### Use Lightweight Models

```bash
ollama pull gemma2:2b
```

Remove unused models:

```bash
ollama list
ollama rm unused-model-name
```

Also close unnecessary applications when running larger models.

## Platform-Specific Issues

### Windows

Common issues include:

- PowerShell execution policy
- Windows Defender warnings
- Python PATH configuration

Use the following when appropriate:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### macOS

Common issues include:

- Gatekeeper restrictions
- Apple Silicon compatibility
- Application permissions

Make sure Ollama is allowed to run in your system security settings.

### Linux

Install common dependencies:

```bash
sudo apt update
sudo apt install curl build-essential
```

## Advanced Troubleshooting

### Debug Logging

Add logging to `app.py` when debugging:

```python
import logging

logging.basicConfig(level=logging.DEBUG)
```

Run Streamlit with debug logging:

```bash
streamlit run app.py --logger.level debug
```

### Streamlit Logs

```bash
streamlit run app.py 2>&1 | tee debug.log
```

### Test Ollama API

```bash
curl http://localhost:11434/api/tags
```

You can also test the generate endpoint:

```bash
curl -X POST http://localhost:11434/api/generate \
  -H "Content-Type: application/json" \
  -d '{"model":"gemma3","prompt":"Hello"}'
```

## Getting Additional Help

### Gather Information

Before reporting a problem, collect:

- Operating system and version
- Python version:

```bash
python --version
```

- Ollama version:

```bash
ollama --version
```

- Exact error message
- Steps used to reproduce the issue

### Useful Resources

- [Ollama Documentation](https://ollama.com/)
- [Streamlit Documentation](https://docs.streamlit.io)
- [GitHub Issues](https://github.com/KrutikaBorase/AI-Tutor/issues)

### Report an Issue

When reporting a bug, include:

- System information
- Error messages
- Relevant logs
- Steps to reproduce the issue
- Expected behavior
- Actual behavior

### Community Support

- [GitHub Discussions](https://github.com/KrutikaBorase/AI-Tutor/discussions)
- Stack Overflow

## Maintenance Tips

Keep your environment and models updated:

```bash
# Update models
ollama pull gemma3

# Clear Streamlit cache
streamlit cache clear

# Update Python dependencies
pip install -r requirements.txt --upgrade
```

---

## Still Having Issues?

If the problem persists:

1. Create a minimal reproducible example.
2. Check existing GitHub issues.
3. Open a new [GitHub issue](https://github.com/KrutikaBorase/AI-Tutor/issues) with complete details.

Most issues are caused by configuration, dependencies, model availability, or system-resource limitations. 🔧
