# AI Prompt Injection Attack on Llama3 (Base64 Encoding)

## Overview

This project demonstrates an AI red team attack using Base64 encoding to bypass content filters in a locally hosted Llama3 model.

The attack was executed using the Garak vulnerability scanner in a Kali Linux environment.

---

## Attack Type

**Encoding-based Prompt Injection (Base64)**

Attack used:
encoding.InjectBase64

---

## How the Attack Works

Base64 encoding hides malicious instructions inside encoded text.

AI models may decode and execute the hidden instructions, bypassing safety filters.

Example:

* Normal prompt → blocked
* Base64 encoded prompt → allowed

---

## Lab Environment

* Kali Linux (VirtualBox)
* Ollama (Local Llama3 model)
* Garak AI vulnerability scanner

---

## Command Used

```
python3 -m garak --target_type ollama --target_name llama3 --probes encoding.InjectBase64 --generations 1
```

---

## Results

Below is proof of execution:

![Garak Test Screenshot](screenshots/Screenshot 2026-03-15 014819.png)

---

## Security Impact

This vulnerability shows that AI systems can be manipulated using encoding techniques.

Potential risks:

* Jailbreaking AI systems
* Bypassing content filters
* Data leakage
* Unsafe outputs

---

## Conclusion

This project demonstrates a real-world AI attack technique used in AI red teaming.

Understanding these vulnerabilities is critical for building secure AI systems.
