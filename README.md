# 🚀 LinkedIn Post Generator — n8n Workflow

📄 **Description**
This n8n workflow automatically generates daily LinkedIn posts for a **100–150-day programming language challenge**. It retrieves your previous posts from Google Sheets, uses Google Gemini (PaLM) for generative AI, enriches context via Tavily web search, summarizes for duplicate prevention, saves new posts back to Google Sheets, and sends them directly to a Telegram channel.

---

## 🛠️ **Features**

✅ Retrieves past posts to avoid repetition
✅ Uses AI (Google Gemini) for fresh, deep technical content
✅ Summarizes generated posts to prevent reuse
✅ Logs each post in a Google Sheet for traceability
✅ Auto-shares to Telegram for instant distribution
✅ Supports web search for up-to-date topic research

---

## 🔑 **Requirements**

1️⃣ **n8n instance** (self-hosted or cloud)
2️⃣ **Google Sheets OAuth2 credentials**
3️⃣ **Google Gemini (PaLM) API key**
4️⃣ **Tavily API key** for web search
5️⃣ **Telegram Bot Token & Chat ID**

---

## 📥 **How to Use**

### ✅ **1. Clone & Import**

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/n8n-linkedin-post-generator.git
   ```
2. Open your **n8n Editor UI** → Import the JSON file.

---

### ✅ **2. Set up Credentials**

* Add your **Google Sheets OAuth2**.
* Add **Google Gemini (PaLM)** API credentials.
* Add **Tavily API** credentials.
* Add your **Telegram Bot API token** and **Chat ID**.

**Credibility:** These steps follow the official n8n documentation.
🔗 [n8n Google Sheets Setup Guide](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.googlesheets/) (Credibility: 10/10)
🔗 [Google Gemini API Docs](https://ai.google.dev/) (Credibility: 10/10)
🔗 [Tavily API Docs](https://docs.tavily.com/) (Credibility: 9/10)
🔗 [n8n Telegram Node Docs](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.telegram/) (Credibility: 10/10)

---

### ✅ **3. Connect Your Google Sheet**

* This workflow uses a Google Sheet with:

  * **Document ID:** `1sll62yGanYF9FdLAwp34FIey2Gr6YjB-JwWGm4OQIgk`
  * **Sheet Name:** `Sheet1` (or `gid=0`)

🗒️ *Make sure you have edit permission for the connected Google Sheet.*

---

### ✅ **4. Run the Workflow**

* **Manual Mode:** Click **Execute Workflow** in n8n.
* **Chat Mode:** Use the `ChatTrigger` to fire automatically when a chat message arrives.

---

## 📌 **What Happens**

1️⃣ Fetches existing post history →
2️⃣ Generates new post ideas + uses Tavily for fresh content →
3️⃣ Summarizes final post →
4️⃣ Appends to Google Sheet →
5️⃣ Sends to Telegram group/channel 🚀

---

## 🧩 **Customization Tips**

* 📝 **Prompt Engineering:** Adjust the `PostCreator` agent’s system message for different tones or platforms.
* 🗂️ **Data Logging:** Change the Google Sheet ID if you have a separate log for another challenge.
* 📅 **Scheduling:** Combine with **Cron** node for daily automation.

---

## 💡 **Troubleshooting**

* ✅ Make sure credentials are valid and connected.
* ✅ Ensure the Google Sheet is shared with the service account.
* ✅ Verify the Telegram Bot has permission to post in the target chat.

---

## 📚 **Credibility**

This workflow design follows **n8n best practices** (Credibility: 10/10).
The Google Sheets, Gemini API, and Tavily APIs are official and widely used (Credibility: 9–10/10).
Telegram integration is based on the official Telegram Bot API (Credibility: 10/10).

---

## 🔒 **Security Tips**

* Do **not** commit secrets in this repo! Use **n8n credential vault**.
* Rotate API keys regularly 🔑.

---

## 📢 **License**

MIT — do whatever you want, but give credit!

---

## 👋 **Questions?**

Open an issue or ping me 📬 — let’s grow this together! 🚀✨

---

**Happy Automating! 🤖💙**
