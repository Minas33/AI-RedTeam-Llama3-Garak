# AI Prompt Injection Attack Lab on Llama3 (Base64 Encoding)

## Overview
This project documents an AI red team lab focused on Base64-encoded prompt injection testing against a locally hosted Llama3 model.

The work was performed in a Kali Linux virtual machine using Ollama and Garak-related setup steps. The project also captures practical issues encountered during tool execution inside a constrained VM environment.

---

## Attack Type
**Encoding-based Prompt Injection (Base64)**

Target technique:
`encoding.InjectBase64`

---

## How the Attack Works
Base64 encoding can hide instructions inside encoded text.

An AI system may decode or process the hidden content in ways that can weaken safety controls or bypass simple filters.

Example:
- Normal prompt → may be blocked
- Base64-encoded prompt → may pass basic filtering

---

## Lab Environment
- Kali Linux (VirtualBox)
- Ollama (local Llama3 model)
- Python virtual environment
- Garak setup and execution attempt

---

## Command Used
```bash
python3 -m garak --target_type ollama --target_name llama3 --probes encoding.InjectBase64 --generations 1
