<div align="center">

# OpenAI Whisper Voice Chat

**Voice-to-text pipeline integrated with ChatGPT — speech captured, transcribed and responded to in real time.**

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://platform.openai.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

</div>

---

## Overview

A Python notebook that chains **OpenAI Whisper** and **ChatGPT** into a voice conversation workflow. Audio input is captured at runtime, transcribed to text via Whisper's speech recognition model, forwarded to the ChatGPT API, and the response is returned to the user — creating a lightweight, end-to-end voice interface for a language model.

Designed to run on **Google Colab or Jupyter Notebook**, with no local infrastructure required beyond a valid OpenAI API key.

---

## Features

- Runtime audio capture from microphone input
- Speech-to-text transcription via OpenAI Whisper
- ChatGPT API integration for AI-generated responses
- Fully interactive notebook workflow — no backend server required

---

## Tech Stack

| Technology | Role |
|---|---|
| Python | Core scripting language |
| OpenAI Whisper | Speech recognition and transcription model |
| ChatGPT API (GPT-3.5 / GPT-4) | Natural language response generation |
| Google Colab / Jupyter Notebook | Execution environment |

---

## Architectural Decisions

**Whisper as the transcription layer** — OpenAI Whisper was chosen over browser-based Web Speech API or cloud STT alternatives for its accuracy across accents and background noise, and for running within the same Python environment as the ChatGPT integration — keeping the entire pipeline in a single runtime.

**Notebook as the interface** — A Jupyter/Colab notebook was selected over a CLI or web app to keep the project focused on the AI integration itself. Each step of the pipeline — capture, transcribe, respond — is visible and independently executable as a cell, making the flow easy to inspect and modify.

**Single API key, two models** — Both Whisper and ChatGPT are accessed through the same OpenAI API key, simplifying credential management and keeping the architecture minimal.

---

## Roadmap

- [x] Audio capture and Whisper transcription
- [x] ChatGPT API integration
- [x] End-to-end voice conversation flow in notebook
- [ ] Text-to-speech output — respond with audio, not just text
- [ ] Conversation history — maintain context across multiple turns
- [ ] Refactor into a standalone Python script with CLI interface
- [ ] Streaming responses for lower perceived latency

---

## How to Run

### Prerequisites

- OpenAI API key — [platform.openai.com](https://platform.openai.com/)
- Google Colab account **or** local Jupyter Notebook with Python 3.9+

### 1. Clone the repository

```bash
git clone https://github.com/gabrieodev/whisper-voice-chat.git
cd whisper-voice-chat
```

### 2. Install dependencies

```bash
pip install openai openai-whisper sounddevice scipy
```

### 3. Configure your API key

```python
import openai
openai.api_key = "your-api-key-here"
```

> For Google Colab, store the key in Colab Secrets or use `getpass` to avoid exposing credentials in the notebook.

### 4. Run the notebook

Open `voice_chat.ipynb` in Colab or Jupyter and execute the cells in order.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">

**Whisper Voice Chat** — Audio in, intelligence out.

Python · OpenAI Whisper · ChatGPT API

</div>
