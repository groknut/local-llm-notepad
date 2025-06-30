# Local LLM Notepad
Run a modern LLM anywhere locally with a double‑click. 

No installation, no internet, no API, no GPU, no admin rights required. 

Local_LLM_Notepad is an open-source, offline plug-and-play app for running local large-language model. Drop the single bundled .exe onto a USB stick, walk up to any computer, and start chatting, brainstorming, or drafting documents. 

# Why you’ll love it

🔌 Portable

Drop the one‑file EXE and your .gguf model onto a flash drive; run on any Windows PC without admin rights.

🪶 Clean UI

Two‑pane layout: type prompts below, watch token‑streamed answers above—no extra chrome.

🔍 Source‑word under‑lining

Every word or number you wrote in your prompt is automatically bold‑underlined in the model’s reply. Ctrl+left click on them to view them in a separate window. Handy for fact‑checking summaries, tables, or data extractions.

💾 Save/Load chats

One‑click JSON export keeps conversations with the model portable alongside the EXE.

⚡ Llama.cpp inside

CPU‑only by default for max compatibility.

🎹 Hot‑keys

Ctrl + S to send, Ctrl + Z to stop, Ctrl + F to find, Ctrl + Mouse‑Wheel zoom, etc.


# Quick Start

Download Local_LLM_Notepad-portable.exe from the Releases page.

Copy the EXE and a compatible GGUF model (e.g. gemma-3-1b-it-Q4_K_M.gguf) onto your USB.

Double‑click the EXE on any Windows computer. First launch caches the model into RAM; subsequent prompts stream instantly.

Need another model? Use File ▸ Select Model… and point to a different GGUF.


# Download links:


| File | Link | Notes |
|------|------|-------|
| **Local_LLM_Notepad-portable.exe** | [Direct download (v1.0.0)](https://github.com/runzhouye/Local_LLM_Notepad/releases/download/v1.0.0/Local_LLM_Notepad_v1.0.0.exe) | ~45 MB, contains the GUI, Python runtime, and llama.cpp |
| **Gemma-3-1B-IT Q4_K_M GGUF** | [Hugging Face](https://huggingface.co/ggml-org/gemma-3-1b-it-GGUF/resolve/main/gemma-3-1b-it-Q4_K_M.gguf?download=true) | Fast CPU model (~0.8 GB) we recommend for first-time users |
| **Icon (optional)** | [Notepad icon PNG](https://upload.wikimedia.org/wikipedia/commons/c/c9/Windows_Notepad_icon.png) | Save as `Icon.png` next to the EXE and it will be used automatically |


# (Optional) Building Your Own Portable EXE
## 1. Clone
$ git clone https://github.com/yourname/Local_LLM_Notepad.git
$ cd Local_LLM_Notepad

## 2. Create env & install deps
$ python -m venv .venv && .\.venv\Scripts\activate
$ pip install -r requirements.txt

## 3. Bundle everything
$ pyinstaller --onefile --noconsole main.py

## 4. Grab dist/Local_LLM_Notepad.exe (≈45 MB)

