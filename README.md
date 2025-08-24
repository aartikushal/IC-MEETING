# 📝 Meeting Summary Bot

The **Meeting Summary Bot** is an AI-powered assistant that helps teams automatically generate structured meeting summaries. It integrates with **Telegram** for messaging, uses **n8n** for workflow automation, and leverages **OpenAI models** for extracting key points, action items, and decisions from meeting transcripts or chat logs.

---

## 🚀 Features
- 📄 **Summarizes Meetings** – Converts raw meeting transcripts into concise summaries.  
- ✅ **Action Items Extraction** – Highlights follow-up tasks and responsibilities.  
- 📌 **Decisions Tracking** – Records key decisions made in meetings.  
- 🔎 **Context-Aware Summaries** – Uses embeddings to understand context before summarizing.  
- 💬 **Telegram Bot Integration** – Users can upload transcripts or notes via Telegram and receive summaries instantly.  
- 🔗 **n8n Automation** – Manages the workflow between Telegram, OpenAI, and storage.  

---

## 🛠️ Tech Stack
- [n8n](https://n8n.io/) – Workflow automation platform  
- [OpenAI](https://platform.openai.com/) – Embedding + Chat models for NLP  
- [Telegram Bot API](https://core.telegram.org/bots/api) – Messaging interface  
- Google Drive (optional) – Store meeting transcripts and summaries  
- Pinecone (optional) – Vector search for past meetings  

---

## 📊 Architecture Flow

```mermaid
flowchart TD
    A[User uploads transcript in Telegram] --> B[Telegram Bot]
    B --> C[n8n Webhook]
    C --> D[OpenAI Embedding + Chat Model]
    D --> E[Meeting Summary Extracted]
    E --> F[Key Points, Action Items, Decisions]
    F --> G[Send Summary back to User via Telegram]
    C -->|Optional| H[Google Drive / Database for storage]

Usage

Open Telegram and start chatting with the bot.

Upload or paste your meeting transcript.

The bot will return a structured summary including:

✅ Key Points

📌 Decisions

📋 Action Items

🔮 Future Improvements

Multi-language meeting summaries

Calendar integration (Google Calendar, Outlook)

Export summaries as PDF/Docx

Searchable meeting archive with Pinecone

🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to improve.

📜 License

This project is licensed under the MIT License – see the LICENSE
 file for details.
