# 🚀 LENO-AI — AI-Powered Lecture-to-Notes Automation

**Turn Text, YouTube Videos, and PDF Documents into Smart Study Notes.**

LENO-AI is an AI-powered workflow automation project that helps students convert different types of learning content into structured notes through Telegram. It combines n8n workflow automation with Google Gemini to simplify the process of creating study material.

## ✨ Features

- 📝 **Text-to-Notes:** Convert submitted text into organized study notes.
- ▶️ **YouTube-to-Notes:** Generate notes from YouTube video links using AI-powered video analysis.
- 📄 **PDF-to-Notes:** Extract text from uploaded PDF documents and transform it into study notes.
- 🤖 **Telegram Integration:** Interact with the workflow through a Telegram bot.
- 🧠 **AI-Powered Processing:** Use Google Gemini 2.5 Flash to generate useful, readable notes.
- 📩 **Automated Delivery:** Split longer notes into manageable messages and send them through Telegram.

## 🛠️ Tech Stack

- **Workflow Automation:** n8n
- **AI Model:** Google Gemini 2.5 Flash
- **Messaging Platform:** Telegram Bot API
- **Document Processing:** PDF text extraction
- **Deployment & Testing:** Local n8n instance with Docker and an HTTPS tunnel for webhook access

## ⚙️ How It Works

### 1. Text-to-Notes
Submit text through Telegram. The workflow processes it with Gemini and returns generated notes.

### 2. YouTube-to-Notes
Send a YouTube video URL. The workflow passes the video to Gemini for content analysis and note generation.

### 3. PDF-to-Notes
Upload a PDF document. The workflow downloads the file, extracts its text, sends the extracted content to Gemini, and delivers the generated notes.

## 🏗️ Workflow Overview

```text
             Telegram Bot
                  |
             Input Detection
                  |
          Route by Input Type
           /       |       \
         Text   YouTube     PDF
           |       |         |
         Gemini  Gemini   Download PDF
           |    Analysis      |
           |       |      Extract Text
           |       |          |
           +-------+----------+
                   |
             Generate Notes
                   |
           Split Long Messages
                   |
             Telegram Output
```

## 🚀 Getting Started

### Prerequisites

- Docker Desktop
- n8n
- A Telegram bot created using BotFather
- A Google Gemini API key
- An n8n Google Gemini credential
- An n8n Telegram credential
- An HTTPS webhook URL for receiving Telegram updates when running locally

### Setup

1. Install and start Docker Desktop.
2. Run an n8n instance locally or use an existing n8n installation.
3. Create a Telegram bot through [BotFather](https://t.me/BotFather).
4. Configure your Telegram bot credentials in n8n.
5. Create a Google Gemini API key through [Google AI Studio](https://aistudio.google.com/).
6. Add the Gemini credential to n8n.
7. Import the LENO-AI workflow JSON into n8n.
8. Verify the node configurations and reconnect credentials if required.
9. Configure the Telegram webhook URL when running n8n locally.
10. Activate the workflow and test the text, YouTube, and PDF branches.

## 🔐 Environment & Security

- Keep API keys and bot tokens private.
- Never commit credentials, `.env` files, or secret tokens to GitHub.
- Use n8n credentials or environment variables to manage sensitive information securely.
- Configure webhook URLs according to your deployment environment.

## 🎯 Project Objective

The objective of LENO-AI is to make study-material preparation more convenient by automating the conversion of learning content into structured notes. It demonstrates the practical integration of AI models, messaging APIs, document processing, and workflow automation.

## 🔮 Future Enhancements

- Export notes to PDF or DOCX.
- Generate quizzes and flashcards from notes.
- Add multilingual note generation.
- Summarize long lectures into topic-wise sections.
- Integrate Google Docs or cloud storage.
- Add user preferences for note length and format.

## 🎥 Demo

- full demo of workflow: [demo video]( https://drive.google.com/file/d/1c7Rl5YPqie_jum2BDDCgYIjReeODYGNW/view?usp=sharing)

## 👨‍💻 Author

**Atharv Kate**

Computer Science & Engineering Student | AI & Automation Enthusiast

- GitHub: [notrealatharv7](https://github.com/notrealatharv7)
- LinkedIn: [Atharv Kate](https://www.linkedin.com/in/atharv-kate-0b906b32b)

---

⭐ If you find this project interesting, consider starring the repository!
