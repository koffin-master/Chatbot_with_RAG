
🧠 Multi-Threaded AI Chatbot with SQL Memory & RAG (Streamlit)

An advanced AI chatbot built with LLMs + RAG + SQL-based persistent memory + multi-thread support, wrapped inside an interactive Streamlit UI.

This project demonstrates production-style conversational AI architecture including state management, thread isolation, persistent storage, and retrieval-augmented generation.

⸻

🚀 Features

💬 Multi-Threaded Chat System
	•	Supports multiple chat sessions (like ChatGPT conversations)
	•	Each thread has a unique thread_id
	•	Users can switch between conversations
	•	Thread-specific context isolation

🗂 Persistent Memory (SQL-Based)
	•	Stores conversation history in a SQL database
	•	Maintains long-term memory across sessions
	•	Enables contextual continuity even after app restarts
	•	Structured schema for messages and thread mapping

📚 Retrieval-Augmented Generation (RAG)
	•	Uses document embeddings + vector search
	•	Retrieves relevant context before generating responses
	•	Improves factual accuracy and reduces hallucinations
	•	Supports custom document ingestion

🎨 Streamlit UI
	•	Clean chat interface
	•	Sidebar for thread management
	•	Session state handling
	•	Real-time response streaming

⸻

🏗️ Architecture Overview

User Query
   ↓
Thread Manager (thread_id)
   ↓
Memory Loader (SQL History)
   ↓
Retriever (Vector Search / RAG)
   ↓
LLM (Context + Retrieved Docs + Memory)
   ↓
Response Generator
   ↓
Store in SQL Database


⸻

🛠️ Tech Stack
	•	Python
	•	Streamlit (Frontend UI)
	•	LLM API
	•	SQL (SQLite / PostgreSQL) for persistent memory
	•	Vector Database for embeddings
	•	LangChain / Custom RAG Pipeline

⸻

🧠 Key Concepts Implemented
	•	Stateful AI systems
	•	Session vs persistent memory handling
	•	Thread-based conversation isolation
	•	SQL schema design for chat storage
	•	Retrieval-Augmented Generation (RAG)
	•	Context window management
	•	Scalable chatbot architecture

⸻

📂 Project Structure

chatbot/
│── app.py                # Streamlit UI
│── database.py           # SQL memory management
│── rag_pipeline.py       # Document retrieval logic
│── thread_manager.py     # Multi-thread handling
│── embeddings/           # Stored vector data
│── requirements.txt


⸻

⚙️ How It Works
	1.	User creates or selects a chat thread.
	2.	Each thread is assigned a unique thread_id.
	3.	When a message is sent:
	•	Previous conversation history is loaded from SQL.
	•	Relevant documents are retrieved using vector similarity search.
	•	Memory + retrieved docs are passed to the LLM.
	4.	The generated response is:
	•	Displayed in UI
	•	Stored back in SQL under the same thread.

⸻

🔥 Why This Project Matters

Unlike basic chatbots, this system demonstrates:
	•	Production-style memory persistence
	•	Multi-session architecture
	•	RAG integration for knowledge grounding
	•	Clean separation between UI, memory, and AI logic

This reflects real-world GenAI system design used in modern AI applications.

⸻

📈 Future Improvements
	•	Authentication system
	•	Cloud database integration
	•	Streaming token responses
	•	Hybrid search (keyword + vector)
	•	Deployment on cloud (AWS / GCP / Render)

⸻

👨‍💻 Author

Built by Khurshid
Aspiring iOS + AI Developer building intelligent systems 🚀
