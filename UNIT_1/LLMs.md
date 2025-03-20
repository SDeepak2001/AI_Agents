# 📚 What are LLMs? 🤖

In the previous section, we learned that each Agent needs an **AI Model at its core**, and that **LLMs (Large Language Models)** are the most common type of AI models for this purpose. 

Now, let’s dive into understanding what LLMs are and how they power AI Agents.

---

## 🔍 What is a Large Language Model?

### Definition:
A **Large Language Model (LLM)** is a type of AI model that excels at **understanding and generating human language**. These models are trained on vast amounts of text data, allowing them to learn patterns, structure, and even nuance in language. 

Most LLMs today are built on the **Transformer architecture**, a deep learning model based on the “Attention” mechanism. 

---

## 🔑 Types of Transformers

Transformers come in **three forms**:

### 1. **Encoders**
- Takes text (or other data) as input and outputs a dense representation of that text.
- **Example:** BERT (Google)
- **Use Cases:** Text classification, semantic search, Named Entity Recognition.
- **Size:** Millions of parameters.

---

### 2. **Decoders**
- Focuses on generating new tokens to complete a sequence, one token at a time.
- **Example:** LLaMA (Meta)
- **Use Cases:** Text generation, chatbots, code generation.
- **Size:** Billions of parameters.

---

### 3. **Seq2Seq (Encoder–Decoder)**
- Combines an encoder and a decoder. The encoder processes input sequences, and the decoder generates output sequences.
- **Example:** T5, BART
- **Use Cases:** Translation, Summarization, Paraphrasing.
- **Size:** Millions of parameters.

---

## 💡 How Do LLMs Work?

The principle behind LLMs is **simple yet powerful**: 

**Objective:** Predict the next token, given a sequence of previous tokens.

---

### 🔍 What is a Token?
A **Token** is the smallest unit of information an LLM processes. While English has around **600,000 words**, LLMs often have a vocabulary of around **32,000 tokens** (like LLaMA 2). Tokens can represent words, parts of words, or even single characters.

---

### 🌟 Example of Tokens:
- **"Interesting"** could be split into tokens: "interest" and "ing".
- **"Interested"** could be split into tokens: "interest" and "ed".

---

## 📚 Popular LLMs

| Model        | Provider     |
|--------------|---------------|
| Deepseek-R1  | DeepSeek      |
| GPT-4        | OpenAI        |
| LLaMA 3      | Meta          |
| SmolLM2      | Hugging Face   |
| Gemma        | Google        |
| Mistral      | Mistral       |

---

## 📌 Special Tokens in LLMs

Each LLM has some **special tokens** specific to the model, which indicate the start or end of a sequence, message, or response. The most important of these is the **End of Sequence (EOS)** token.

| Model      | Provider     | EOS Token         | Functionality                    |
|------------|--------------|------------------|----------------------------------|
| GPT-4      | OpenAI       | `<|endoftext|>`    | End of message text              |
| LLaMA 3    | Meta         | `<|eot_id|>`       | End of sequence                  |
| Deepseek-R1| DeepSeek     | `<|end_of_sentence|>`| End of message text            |
| SmolLM2    | Hugging Face | `<|im_end|>`       | End of instruction or message    |
| Gemma      | Google       | `<end_of_turn>`    | End of conversation turn         |

---

## 🔄 Understanding Next Token Prediction

### **What does 'Autoregressive' mean?**
LLMs are **autoregressive**, meaning the output from one pass becomes the input for the next one. This process continues until the model predicts the **EOS token**, at which point the model stops.

---

### 📌 How the Decoding Process Works
1. **Tokenization:** Input text is converted into tokens.
2. **Representation:** The model computes a representation of the sequence, understanding the meaning and position of each token.
3. **Prediction:** The model outputs scores ranking the likelihood of each token being the next one in the sequence.
4. **Decoding Strategies:** 
   - **Greedy Decoding:** Always picks the token with the highest score.
   - **Beam Search:** Explores multiple candidate sequences to find the most probable one.

---

## 🔥 Why Are LLMs So Powerful?

The **Attention Mechanism** in Transformers allows the model to focus on the most relevant parts of the input when making predictions.

For example:
In the sentence **“The capital of France is …”**, words like **“France”** and **“capital”** carry the most meaning for predicting the next token.

---

## 🧩 How Are LLMs Trained?

1. **Pre-Training:**
   - Models learn language structure by predicting the next word in a sequence.
   - Uses **self-supervised learning**.
   
2. **Fine-Tuning:**
   - Models are trained for specific tasks, like conversations or code generation.
   - Uses **supervised learning**.

---

## 💡 How Are LLMs Used in AI Agents?

LLMs provide the **foundation for understanding and generating human language**. They help AI Agents:

- **Interpret user instructions.**
- **Maintain context in conversations.**
- **Define plans and decide which tools to use.**

The **LLM** is the **brain of the Agent**, providing the reasoning power to understand instructions and generate appropriate responses.

---

## 🌟 How Can I Use LLMs?

You have two main options:

1. **Run Locally:** Requires high-performance hardware.
2. **Use a Cloud/API:** Via platforms like **Hugging Face Serverless Inference API**.

---

## 📌 Key Takeaways

- LLMs are powerful AI models designed to **predict the next token** in a sequence.
- They excel at **natural language understanding and generation**.
- They are the core reasoning engine of AI Agents, providing them with the ability to **understand, plan, and respond**.

---

Would you like me to prepare **some cool visuals to explain the concepts of LLMs**, such as the **Transformer architecture, attention mechanism, and tokenization process**? 

Also, shall I proceed to show you how to **integrate this code into your repository's `README.md`** with visuals? 😊

