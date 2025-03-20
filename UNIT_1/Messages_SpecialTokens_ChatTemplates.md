# 💬 Messages, Special Tokens, and Chat Templates

Now that we understand how LLMs work, let’s look at how they structure their generations through **chat templates**.

Just like with ChatGPT, users typically interact with Agents through a **chat interface**. Therefore, it's essential to understand how LLMs manage chats.

---

## 🔍 What Are Messages and Special Tokens?

### Definition:
- **Messages:** Structured data exchanged between a User and an Assistant (LLM). 
- **Special Tokens:** Unique markers used by models to delimit the start and end of messages, instructions, or conversation turns. 

---

## 📖 System Messages and Conversation Structuring

An LLM doesn't remember past interactions. Instead, every conversation is passed as a single prompt formatted by **Chat Templates**.

### 🔑 System Messages
- Define how the model should behave.
- Provide instructions and context for the conversation.

**Example:**
```python
system_message = {
    "role": "system",
    "content": "You are a friendly and helpful assistant."
}
