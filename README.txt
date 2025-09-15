# Conversation Management & JSON Extraction Assignment

## Overview
This repository contains the implementation of a conversation management system and JSON information extraction task using the Groq API with OpenAI SDK compatibility. The assignment demonstrates:

1. Maintaining and summarizing conversation history.
2. Extracting structured information from chat messages into JSON format.

---

## Features

### 1. Conversation Management with Summarization
- Stores user and assistant messages as conversation history.
- Summarizes the conversation after every `k` turns to reduce memory usage.
- Maintains important context while truncating older messages.
- Supports simulation of conversations.

**Example:**
After every 3rd message, conversation is summarized to maintain context efficiently.

---

### 2. JSON Schema Extraction
- Extracts structured data from chat messages.
- Captures fields: `name`, `email`, `phone`, `location`, `age`.
- Handles missing or partial information gracefully.

**Example Chats & Output:**
```python
Chat: "Hi, my name is Rahul. I live in Delhi. My email is rahul123@gmail.com and I’m 22."
Extracted JSON: {'name': 'Rahul', 'email': 'rahul123@gmail.com', 'phone': None, 'location': 'Delhi', 'age': 22}

Chat: "Hello, I’m Ananya from Mumbai, 25 years old. You can reach me at ananya99@yahoo.com"
Extracted JSON: {'name': 'Ananya', 'email': 'ananya99@yahoo.com', 'phone': None, 'location': 'Mumbai', 'age': 25}

Chat: "This is Arjun, my phone is 9876543210, I stay in Bangalore."
Extracted JSON: {'name': 'Arjun', 'email': None, 'phone': '9876543210', 'location': 'Bangalore', 'age': None}



