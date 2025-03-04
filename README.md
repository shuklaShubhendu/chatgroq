# 🤖 LangChain Chatbot



## 📝 About
A simple yet powerful chatbot built with **LangChain**, **Streamlit**, and **Groq API**. Chat with AI models like LLaMA, Mixtral, or Gemma right from your browser! 🚀

---

## ✨ Features
✅ **Interactive Chat**: Real-time chatting with AI models.  
✅ **Model Selection**: Choose from LLaMA 3.1 70B, Mixtral 8x7B, or Gemma 7B.  
✅ **Chat History**: Keeps your conversation context (last 5 messages).  
✅ **Clear Chat**: Reset the conversation with one click.  
✅ **Streamlit UI**: Sleek, user-friendly interface with avatars ![User](user-icon.png) for you and ![Robot](robot-icon.png) for AI.

---

## 🛠️ Setup

### Prerequisites
- Python 3.8+
- A [Groq API Key](https://groq.com) (free tier available!)

### Installation

1️⃣ **Clone the repo**:

```bash
git clone https://github.com/yourusername/langchain-chatbot.git
cd langchain-chatbot
```

2️⃣ **Install dependencies**:

```bash
pip install -r requirements.txt
```

3️⃣ **Set your Groq API Key**:

Replace the empty string in the code:

```python
import os
os.environ["GROQ_API_KEY"] = "your-api-key-here"
```

Or set it as an environment variable:

```bash
export GROQ_API_KEY="your-api-key-here"
```

4️⃣ **Run the app**:

```bash
streamlit run app.py
```

---

## 🚀 Usage

1. Open the app in your browser (usually at `http://localhost:8501`).
2. Select a model from the sidebar (e.g., `llama-3.1-70b`).
3. Type your message in the chat input and hit Enter! 💬
4. Watch the AI respond with a cool "Thinking..." spinner. 🤖💭

---

## 📝 Code Overview

📜 `app.py` - Main script with Streamlit UI and LangChain logic.  
🧠 **LangChain Setup** - Uses `ChatGroq` for model access and `LLMChain` for conversation flow.  
📝 **Prompt Template** - Formats chat history for better context.  
⚡ **Caching** - `@st.cache_resource` speeds up model loading.

### 🔍 Core Logic

```python
# Snippet of the core logic
llm = get_llm(selected_model)
chain = LLMChain(llm=llm, prompt=prompt_template)
response = chain.run({"input": user_input})
```

---

## 🧩 Dependencies

📦 **Required Packages:**
- `streamlit` - For the web interface
- `langchain` - For chaining prompts and models
- `langchain-groq` - Groq API integration

📜 **See `requirements.txt` for full list**:
```bash
streamlit
langchain
langchain-groq
```

---

## 🌟 Example

**You**: "What's the meaning of life?"  
**AI**: "🤓 According to some, it’s 42. But I think it’s more about finding your own purpose—what do you say?"

---

## ⚠️ Notes

⚡ Make sure your Groq API key is set, or the app won’t work.  
🗂️ The app keeps only the last 5 messages in context to optimize performance.  
🔧 Want to tweak it? Play with the `prompt_template` or add more models!

---

## 🤝 Contributing

Feel free to fork, tweak, and PR! Issues and suggestions welcome. 😊

---

## 📌 Credits

Built with ❤️ by [Your Name] using LangChain and Streamlit. Powered by Groq’s awesome API.

🎉 Enjoy chatting! 🚀
