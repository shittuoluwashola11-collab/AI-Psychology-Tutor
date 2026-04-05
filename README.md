# AI-Psychology-Tutor
A Python-based Psychology Tutor agent utilizing OpenAI's gpt-4o-mini and conversational memory to generate concise summaries of psychological schools of thought and theories.
## AI Psychology Tutor

An automated tutoring system designed to provide concise, academic summaries of various psychological schools of thought. This project leverages the OpenAI API to simulate a specialized tutor capable of explaining complex theories through a structured conversational loop.

## 🧠 Overview
The system is built to act as a **Psychology Tutor**. It maintains a conversation history to ensure context-aware responses while answering a series of foundational questions in the field of psychogy.

## 🛠️ Technical Stack
* **Language:** Python 3.12.11.
* **AI Model:** `gpt-4o-mini`.
* **Framework:** OpenAI API.
* **Execution Environment:** DataLab / Jupyter Notebook

## ✨ Key Features
* **Role-Based Prompting:** The assistant is strictly defined as a tutor that generates concise summaries.
* **Conversational Memory:** Uses a `conversation` list to store system instructions, previous user questions, and assistant responses, ensuring the model tracks the dialogue flow.
* **Automated Batch Processing:** Loops through a pre-defined list of core psychology questions to generate continuous learning material.
* **Deterministic Responses:** Uses a `temperature` setting of `0.0` to ensure factual and consistent academic output.

## 📋 Topics Covered
The tutor currently processes queries regarding:
* **Client-Centered Therapy**
* **Dream Analysis**
* **Freud’s Triad of Personality** (Id, Ego, Superego)
* **Classical Conditioning**.
* **Reinforcement Learning**.
* **General Theories of Psychology**.

## 💻 Implementation Details
The core logic resides in a loop that appends user questions to the conversation history and captures the model's responses for future context:

```python
for question in questions:
    input_dict = {"role": "user", "content": question}
    conversation.append(input_dict)
    # ... calls OpenAI API ...
    resp_dict = {"role": "assistant", "content": resp}
    conversation.append(resp_dict)

http://googleusercontent.com/immersive_entry_chip/0
