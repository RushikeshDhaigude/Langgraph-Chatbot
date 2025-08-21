# LangGraph Chatbot with Streamlit

A conversational chatbot built using LangGraph and Streamlit.
This project supports multi-session chat management, allowing you to start new conversations, revisit old ones, and view chat previews in the sidebar — similar to modern messaging apps.


### Features

1. Interactive chatbot interface built with Streamlit.
2. Powered by LangGraph for conversational flow management.
3. Multi-threaded chat sessions:
   - Start a new chat.
   - Retrieve previous conversations.
   - Switch between chat threads easily.
4. Sidebar shows chat previews (first user message).
5. Streaming responses for a real-time typing effect.

### Project Struture 

```
Langgraph_Chatbot/
│
├── backend.py  # Contains chatbot logic + thread retrieval functions
├── frontend.py  # Streamlit UI (main entrypoint)
├── requirements.txt  # Dependencies
├── README.md  # Project documentation
```


### Installation

1. Clone the repository
   ```
   git clone https://github.com/RushikeshDhaigude/Langgraph-Chatbot.git
   cd Langgraph-Chatbot
   
   ```
   
2. Create virtual environment
   ```
   python3 -m venv langraph_chatbot_env
   source langraph_chatbot_env/bin/activate   # Mac/Linux
   langraph_chatbot_env\Scripts\activate      # Windows
   ```

3. Install dependencies
   ```
   pip install -r requirements.txt
   ```
   
4. Run the Streamlit app
   ```
   streamlit run frontend.py
   ```


### Usage Guide

1. New Chat: Click the New Chat button in the sidebar to start a fresh conversation.

2. My Conversations:
   - Displays all your saved threads.
   - Each thread shows a preview (first user message).
   - Click to load the conversation into the main chat window.
   - Chat Input: Type your question in the input box at the bottom, and the assistant will reply in streaming mode.

### Configuration

- Chat state is managed using st.session_state.
- Each conversation is identified by a unique thread_id (UUID).
