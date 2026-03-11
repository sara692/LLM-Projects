# 📄 PDF Q&A Bot

An AI-powered web app that lets you ask questions about PDF documents using open-source Large Language Models (LLMs) — no model downloads required.

Built with **Gradio** and **HuggingFace Inference API**, deployed on **HuggingFace Spaces**.

---

## 🚀 Live Demo

👉 [Try it on HuggingFace Spaces](https://huggingface.co/spaces/Sara65/llama_pdf_based)

---

## ✨ Features

- 📄 **Fixed document mode** — ask questions about a pre-loaded PDF
- 📤 **Upload mode** — upload your own PDF and ask questions about it
- 🤖 **Open-source LLMs** — powered by Llama via HuggingFace Inference API
- ⚡ **No model downloads** — models run on HuggingFace's servers
- 🔒 **Secure** — HF token stored as an encrypted secret, never in code
- ⚠️ **6,000 character limit** — optimized for small models, large PDFs are trimmed automatically

---

## 🖼️ App Preview

```
┌─────────────────────────────────┐
│  📄 PDF Q&A Bot                 │
│  ─────────────────────────────  │
│  🤖 Select Model    [Load Model]│
│  ─────────────────────────────  │
│  📂 Document Source             │
│  ● Use fixed document           │
│  ○ Upload my own PDF            │
│  ─────────────────────────────  │
│  ❓ Your Question               │
│  [                           ]  │
│           [  Ask  ]             │
│  ─────────────────────────────  │
│  💡 Answer                      │
│  [                           ]  │
└─────────────────────────────────┘
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Gradio | Web UI framework |
| pypdf | PDF text extraction |
| HuggingFace Hub | Model inference API |
| Llama 3.1 8B | Language model |
| HuggingFace Spaces | Deployment platform |

---

## 📁 Project Structure

```
pdf-qa-bot/
├── app.py              # Main application code
└── README.md           # This file
```

---

## ⚙️ How It Works

```
User question
     ↓
Gradio UI (app.py)
     ↓
Extract PDF text (pypdf)
     ↓
Build prompt (question + document context)
     ↓
HuggingFace Inference API (Llama model)
     ↓
Answer displayed to user
```

1. The PDF text is extracted and trimmed to 6,000 characters
2. The question and document text are sent to the LLM via the HF Inference API
3. The model answers based **only** on the document content
4. If the answer is not in the document, the model says so

---

## 🚀 Deploy Your Own

### 1. Fork or clone this repo
```bash
git clone https://github.com/sara692/LLM-and-Agents/edit/main/01-PDF-Q%26A-bot
cd 01-PDF-Q&A-bot
```

### 2. Create a HuggingFace Space
- Go to [huggingface.co/spaces](https://huggingface.co/spaces)
- Click **New Space** → choose **Gradio** → **CPU Free**

### 3. Add your HF Token as a Secret
- Space **Settings** → **Variables and Secrets** → **New Secret**
- Name: `HF_TOKEN`
- Value: your token from [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)

### 4. Upload files to your Space
Upload `app.py`, `requirements.txt`, `README.md`, and your PDF file

### 5. Accept Llama license
Visit [meta-llama/Llama-3.1-8B-Instruct](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct) and accept the license with your HF account

---

## 📦 Requirements

```
pypdf
gradio>=4.0
huggingface_hub
```

---

## ⚠️ Terms of Use

- This tool is for **educational and informational purposes only**
- Do not upload illegal or harmful content
- Answers are AI-generated — always verify important information
- PDF context is limited to 6,000 characters (~4–5 pages)

---

## 👩‍💻 Author

**Sara Ibrahim Omran**
- Mail: (saraomran433@gmail.com)

---

## 📄 License

This project is open source and available.
