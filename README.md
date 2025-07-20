# 🧠 Nimbus-Q | Agent Integration Demo

This repo shows how AI agents (like **Grok, ChatGPT, Claude, Gemini, or Perplexity**) can securely access user-uploaded video files via temporary, expiring links — without storing data or requiring infra setup.

> **Patent Pending | US Provisional Application Filed (April 2025)**  
> This is a stripped-down demo, not a clone or SDK. It shows how any AI system can interact with the Nimbus-Q flow.

---

## 🔍 What This Demo Covers

- `example-agent-call.js` → Simulated agent fetch to temp video link
- `sample-response.json` → Sample API response format
- `DEMO_LINK.txt` → Live product demo: [https://nimbus-q.web.app/](https://nimbus-q.web.app/)
- `LICENSE` → Custom license for demo/eval only

No backend logic, infrastructure, or deletion system is included here — just the public-facing usage path.

---

## ⚙️ How It Works

1. **User uploads video** via frontend or API
2. **(Optional)** SFW content check runs via base AI model
3. System generates **expiring, encrypted link** for agent access
4. Agent (Grok, GPT, Claude, etc.) fetches video and processes
5. **Auto-deletion** is triggered by agent confirmation or fallback timer

---

## 👀 Sample Agent Fetch
```js
const fetch = require('node-fetch');

const TEMP_LINK = 'https://temp-nimbus-link.com/abc123'; // example only

async function runAgent() {
  const response = await fetch(TEMP_LINK);
  const videoBuffer = await response.arrayBuffer();
  console.log('Video fetched. AI can now process it.');
}

runAgent();

---

## 💡 Use Case

Nimbus-Q was designed to give AI agents **real-world video vision** without the storage risks or infra bloat.  
Great for:
- Agents summarizing or translating user videos
- Enterprise AI chatbots that accept video input
- Temporary, zero-retention data flows for privacy-first apps

---

## 🔐 Licensing Note

This repo is for **evaluation and integration demo purposes only.**  
The core backend logic, deletion engine, and secure access system are **proprietary and patent-protected.**  
No reproduction, derivative systems, or commercial use without explicit license.

📩 To request API keys or private test access:  
**nimbusq.com@gmail.com**

---

## 🌐 Demo

Check it out in action:  
🔗 [https://nimbus-q.web.app/](https://nimbus-q.web.app/)

---

## 🚀 Built to let AI agents see the world — without seeing your data.
