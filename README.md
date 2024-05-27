# 🐘 Introducing Loyal Elephie: Your Trusty AI Companion and Episodic Memory Manager! 🧠
<p align="center">
  <img src=".public/image.png" alt="Your image description" width="200" style="display: block; margin: 0 auto;">
</p>
🚀 Embark on a exciting adventure with Loyal Elephie, your faithful AI sidekick! This project combines the power of a neat Next.js web UI and a mighty Python backend, leveraging the latest advancements in Large Language Models (LLMs) and Retrieval Augmented Generation (RAG) to deliver a seamless and meaningful chatting experience! 🎉

## Features

1. **🎛️ Controllable Memory:** Take control of Loyal Elephie's memory! You decide which moments to save, and you can easily edit the context as needed. 📝

2. **🔍 Hybrid Search:** Experience the powerful combination of Chroma and BM25 for efficient searches! It's also optimized for handling date-based queries. 📅

3. **🔒 Secure Web Access:** With a built-in login feature, only authorized users can access your AI companion, ensuring your conversations remain private and secure over the internet. 🛡️

4. **🌐 Simplified Agent:** No function-calling required. Loyal Elephie is optimized for cached generation and works smoothly with many top-notch local LLMs running with Llama.cpp or ExllamaV2. 💬

5. **📝 (Optional) Markdown Editor Integration:** Connect with online Markdown editors to view the original referred document during chats and experience real-time LLM knowledge integration after editing your notes online. ✍️

Loyal Elephie supports both open and proprietary LLM APIs in the OpenAI API format. 

## Screenshots 
*Meta-Llama-3-70B-Instruct.Q4_K_S.gguf is used when capturing the below screenshots*

![](.public/screenshot1.png)

![](.public/screenshot2.png)


![](.public/screenshot4.png)
With [SilverBulletMd](https://github.com/silverbulletmd/silverbullet), you can edit a note on the browser and then let Loyal Elephie rememebers it!

![](.public/screenshot3.png)

The UI is modified from https://github.com/mckaywrigley/chatbot-ui-lite, credits to the author Mckay Wrigley!

## Deployment

**1. Clone Repo**

```bash
git clone https://github.com/v2rockets/Loyal-Elephie.git
```

**2. Install Frontend Requirments**

```bash
npm i
```

**3. Configure Login Users**
```json
# frontend/users.json
[{
    "username":"admin",
    "password":"admin"
}]
```

**4. Install Backend Requirents**

```bash
pip install requirements.txt
```

**5. Configure Backend Settings**

edit backend/users.json
```python
# backend/settings.py

CHAT_BASE_URL = 'https://api.openai.com/v1' # Modify to your OpenAI compatible API url
CHAT_API_KEY = 'your-api-key'
CHAT_MODEL_NAME = "gpt-3.5-turbo"
```

**6. Run App**

frontend:
```bash
npm run build
npm run start
```
backend:
```bash
python app.py
```

# Usage Tips
* use "Save" button to save the current conversation into Loyal Elephie's memory.
* use "Reset" button to clear the current conversation (it won't affect save status), it's the same as refreshing page.
* click on the titles in "Reference" to navigate to the corresponding Mardown note (but SilverBulletMd has to be hosted and configured).
