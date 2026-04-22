# 🧠 Blog Writing Agent (AI-Powered)

An intelligent, multi-agent blog generation system built using **LangGraph + LLMs** that can autonomously research, plan, write, and enhance blog content — including optional image generation.

---
  
## 🚀 Overview

This project implements a **modular AI pipeline** that transforms a simple topic into a structured, high-quality blog post.
 
It simulates a real-world content workflow:

* 🔍 Decide if research is needed
* 📚 Gather relevant information
* 🧩 Plan blog structure 
* ✍️ Generate sections
* 🖼️ Add contextual images
* 📄 Export final markdown

---

## ⚙️ Architecture

The system is built using a **multi-agent graph pipeline**:

```
Router → Research → Orchestrator → Workers → Reducer (with Images)
```

### Components:

* **Router**
  Determines whether the topic requires research (closed-book / hybrid / open-book)

* **Research Node**
  Fetches relevant data using Tavily (if needed)

* **Orchestrator**
  Plans the blog structure (sections, tone, audience)

* **Workers**
  Generate individual blog sections in parallel

* **Reducer**
  Merges content and optionally generates images

---

## 🧠 Tech Stack

* **LangGraph** – Multi-agent orchestration
* **LangChain** – LLM abstraction
* **Groq API** – Fast LLM inference
* **Tavily API** – Web research
* **Streamlit** – Interactive frontend
* **Python** – Core implementation

---

## 📦 Features

* ✅ Autonomous blog generation from a single topic
* ✅ Research-aware content creation
* ✅ Multi-agent parallel processing
* ✅ Markdown export + downloadable bundle
* ✅ Optional AI-generated images
* ✅ Streamlit UI for interaction
* ✅ Past blog history viewer

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Adarsh-0417/Blog-Writing_Agent.git
cd Blog-Writing_Agent
```

### 2. Create virtual environment

```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in root:

```env
GROQ_API_KEY=your_key_here
TAVILY_API_KEY=your_key_here   # optional
GOOGLE_API_KEY=your_key_here   # for image generation
```

---

## ▶️ Run the App

```bash
streamlit run bwa_frontend.py
```

---

## 🧪 Example Usage

Input:

```
Self Attention in Transformer Architecture
```

Output:

* Structured blog with multiple sections
* Research-backed insights (if required)
* Optional diagrams/images
* Downloadable markdown + assets

---

## ⚠️ Notes

* Free-tier APIs may hit **rate limits**
* Use lightweight models (e.g., `llama-3.1-8b-instant`) for efficiency
* Avoid committing `.env` (contains API keys)

---

## 📌 Future Improvements

* Better structured output handling for non-GPT models
* Caching layer for repeated topics
* Fine-tuned prompts for higher consistency
* Deployment (Docker / Cloud hosting)

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first.

---

## 📄 License

This project is open-source and available under the MIT License.

---

## ✨ Author

**Adarsh**
BTech Student | AI/ML Enthusiast

---

## 🧠 Final Thought

This project is not just a blog generator —
it’s a step toward building **autonomous AI systems that think, plan, and create**.
