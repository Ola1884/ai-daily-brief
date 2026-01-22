
---

## 📰 README Template for `ai-daily-brief` (Your AI Newsletter)

```
# 📬 AI Daily Brief: Your Personalized AI News Digest

> **"Cut through the noise. Get only what matters — explained clearly."**

AI Daily Brief delivers a **daily email** of the most relevant AI news, papers, and tools — tailored to your interests (e.g., "Computer Vision" or "LLMs"). No fluff, just signal.

## 🎯 Problem
AI moves fast. But:
- RSS feeds are overwhelming
- Summaries lack context
- Most tools don’t personalize by *your* focus areas

## 💡 Solution
A smart curation pipeline that:
1. **Scrapes** arXiv, Hacker News, Reddit, blogs
2. **Ranks** by relevance to your profile
3. **Summarizes** with LLM + adds “Why This Matters”
4. **Delivers** daily 

## 🛠️ Tech Stack
- **Data Sources**: arXiv API, PRAW (Reddit), Requests (Hacker News)
- **Embeddings**: `all-MiniLM-L6-v2` (sentence-transformers)
- **LLM**: Mistral 7B (via Ollama) for summarization & explanation
- **Backend**: FastAPI + PostgreSQL
- **Email**: Resend API
- **Scheduler**: GitHub Actions (cron)
- **Retrieval**: FAISS vector store

## 📦 Features
- ✅ Select topics: “Robotics”, “GenAI”, “BCI”, etc.
- ✅ One-click signup (no password)
- ✅ “Ask follow-up” button → opens RAG chat
- ✅ Clean, mobile-friendly email template



## 📊 Personalization Logic
- User interest vector ← average of selected topic embeddings
- Article score = cosine(article_emb, user_emb) + recency boost
- Top 5 articles selected daily

## 📧 Sample Output
> **🔥 New: Efficient Transformers for Edge Devices**  
> *Summary*: Researchers propose SparseFormer, reducing FLOPs by 60%...  
> **Why it matters**: Perfect for your robotics edge deployment project!  
> [Read Paper] | [Ask Follow-up]


## 🙌 Data Sources
- arXiv.org
- Hacker News
- r/MachineLearning
- The Batch (DeepLearning.AI)

---
Stay informed, not overwhelmed.
