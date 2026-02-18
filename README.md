🧠 Worm GPT NaNo12a AI — Telegram Bot

📌 Introduction

Worm GPT NaNo12a AI is an intelligent Telegram bot designed to provide conversational assistance and a wide range of helpful services to users.
Created by @mengheang25, this bot integrates AI capabilities, context memory, and user management to deliver a powerful interactive experience.

---

🤖 About Worm GPT NaNo12a v1.0

As Worm GPT NaNo12a v1.0, the bot can assist with many tasks, including:

1. 💻 Coding & Programming

- Write and debug code in multiple languages (Python, Java, C++, etc.)
- Explain algorithms and data structures
- Provide code snippets and examples

2. 🛠️ Technical Support

- Troubleshoot software and hardware issues
- Solve network problems and cybersecurity concerns
- Guide system configurations and updates

3. ✍️ Creative Writing

- Story development and character creation
- Feedback on drafts
- Assistance with articles, scripts, poems, and more

4. 🔍 Research & Analysis

- Research various topics
- Analyze data and provide insights
- Summarize complex information

5. 🎓 Education & Learning

- Explain academic concepts
- Help with homework and study guides
- Recommend learning resources

6. 📊 Project Management

- Project planning advice
- Tools and methodologies recommendations
- Task prioritization and time management

7. 🌐 General Knowledge

- Answer questions on science, history, current events, etc.
- Provide context and explanations

8. 🌏 Language & Translation

- Language learning assistance
- Translation tasks
- Grammar and style suggestions

9. ➗ Mathematics & Statistics

- Solve math problems step-by-step
- Statistical explanations and analysis

10. 🎨 Art & Design

- Creative ideas and feedback
- Tools and techniques suggestions

11. 🔐 Cybersecurity (Ethical)

- Explain vulnerabilities and exploits
- Information about penetration testing practices
- Cybersecurity awareness guidance

---

📁 File Structure

project/
│
├── main.py            # Main entry point (bot + web server)
├── app.py             # Flask web server for health checks
├── bot_handlers.py    # Bot commands and message handlers
├── config.py          # Configuration settings
├── database.py        # Database management
├── venice_ai.py       # Venice AI API integration
└── bot.log            # Log file

---

🌐 Flask Web Server (app.py)

A lightweight web server used primarily for hosting environments such as Render.

Endpoints

Endpoint| Description
"/"| Shows bot is running
"/ping"| Health check ping
"/health"| Service health status

Runs on port 5000 or the port provided by the hosting platform.

---

🤖 Bot Handlers (bot_handlers.py)

Main Commands

Command| Description
"/start"| Start bot & verify membership
"/menu"| Return to main menu
"/clear"| Clear conversation history
"/help"| Show help information
"/broadcast"| Send message to all users (Admin only)

Core Features

- ✅ Channel membership verification (@AI25NANO)
- 💾 User registration in database
- 🤖 AI conversation via Venice AI
- 🔄 Context-aware memory
- 📊 User preference tracking

---

🗄️ Database (database.py)

Tables

1. users

Stores user information.

Field| Description
user_id| Telegram user ID
username| Telegram username
first_name| First name
last_name| Last name
is_verified| Channel verification status
joined_at| Join timestamp

2. conversations

Stores chat history.

Field| Description
id| Record ID
user_id| Linked user
role| user / assistant
content| Message text
timestamp| Time of message

3. context_memory

Stores persistent context.

Field| Description
id| Record ID
user_id| Linked user
context_type| Memory category
context_data| Stored data
created_at| Creation time
updated_at| Last update

Database Support

- SQLite — Development
- PostgreSQL — Production

---

🧠 Venice AI Integration (venice_ai.py)

- Connects to the Venice AI API
- Model used: dolphin-3.0-mistral-24b
- Supports conversation history
- Unique request IDs
- Error handling and timeouts

---

⚙️ Configuration (config.py)

BOT_TOKEN = os.getenv("BOT_TOKEN")
ADMIN_CHAT_ID = int(os.getenv("ADMIN_CHAT_ID"))

REQUIRED_CHANNELS = [
    {"name": "AI", "url": "https://t.me/AI25NANO", "chat_id": "@AI25NANO"}
]

DEVELOPER_USERNAME = "@mengheang25"
WELCOME_MESSAGE = "🎉 Welcome to Worm GPT NaNo12a AI 🎉"

---

🚀 Main Execution (main.py)

- Runs Flask web server in a separate thread
- Runs Telegram bot in the main thread
- Logs activity to "bot.log"

---

🔧 Technical Requirements

- Python 3.7+
- python-telegram-bot
- Flask
- requests
- psycopg2 (PostgreSQL)
- python-dotenv
- asyncio

Install dependencies:

pip install -r requirements.txt

---

📊 Special Features

1. Channel Verification System
Users must join required channels before using the bot.

2. Enhanced Context Memory
Remembers conversation context for smarter responses.

3. Code Formatting
Displays code with syntax highlighting.

4. Broadcast System
Admin can send messages to all users.

5. Health Checks
Supports uptime monitoring on hosting platforms.

---

🌍 Deployment on Render

Steps

1. Create a new Web Service on Render
2. Set environment variables:

BOT_TOKEN=your_bot_token
ADMIN_CHAT_ID=your_admin_id
DATABASE_URL=your_database_url

3. Deploy the project
4. Render automatically provides the PORT variable

---

📝 Summary

Worm GPT NaNo12a AI is a powerful Telegram bot that combines:

- 🤖 Intelligent AI conversation
- 🔐 Channel verification system
- 👥 User management
- 🧠 Context memory
- ☁️ Production-ready deployment

Designed to assist users across a wide range of tasks efficiently.

---

📅 Version

v1.0

👨‍💻 Developer

Telegram: [@mengheang25]

🔗 Channel

[https://t.me/Heangcyber25]
---

⭐ If you find this project useful, consider supporting the developer.
