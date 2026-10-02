# 🤖 Autonomous AI Financial & Market Intelligence Agent

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/krishadesai16/autonomous-financial-intelligence-agent/blob/main/Autonomous_AI_Financial_%26_Market_Intelligence_Agent.ipynb)

An autonomous financial intelligence agent that bridges **Financial Natural Language Processing (NLP)** with quantitative momentum tracking to deliver real-time, risk-weighted investment decision support.

---

## 📌 Architectural Workflow
1. **Live Quantitative Ingestion:** Pulls closing price history, 30-day percentage returns, and 20-day Simple Moving Averages (SMA) via `yfinance`.
2. **Real-Time Qualitative Ingestion:** Scrapes breaking equity headlines dynamically using Google News RSS feeds.
3. **Domain-Specific NLP Inference:** Classifies headline sentiment using `ProsusAI/finbert` (PyTorch transformer) to compute continuous polarity scores:
   $$\text{Polarity} = P(\text{Positive}) - P(\text{Negative}) \in [-1.0, +1.0]$$
4. **Multi-Factor Decision Fusion:** Cross-references sentiment polarity against 20-day SMA momentum to assign stances (`BULLISH`, `BEARISH`, or `NEUTRAL / HOLD`).
5. **Interactive Executive Interface:** Built with Gradio Blocks and Plotly, featuring a searchable ticker catalog, radial sentiment dials, and headline audit logs.

---

## 🛠️ Tech Stack
* **Deep Learning & NLP:** PyTorch, Hugging Face Transformers (`ProsusAI/finbert`)
* **Financial Data Pipelines:** `yfinance`, Google News RSS
* **Visualization & Frontend:** Gradio Blocks, Plotly Graph Objects
* **Execution Environment:** Google Colab (T4 GPU Accelerated)

---

## 🚀 How to Run
1. Click the **"Open In Colab"** badge above.
2. Ensure runtime is set to **T4 GPU** (`Runtime` → `Change runtime type` → `T4 GPU`).
3. Run all cells sequentially. Gradio will launch the dashboard with a shareable public URL.
