# 🧠 Personal AI Data Analyst

An interactive **Streamlit-based data analysis application** that allows users to upload datasets, explore them through **guided analysis suggestions**, and optionally ask **custom questions powered by a local LLM (Ollama)** — all without sending data to the cloud.

This project is designed to demonstrate practical skills in **Python, data analysis, Streamlit UI development, and local LLM integration**.

---

## ✨ Key Features

* 📁 Upload CSV, Excel, or JSON datasets
* 🔍 Automatic dataset inspection and smart analysis suggestions
* 📊 Built-in deterministic analyses (EDA, plots, correlations, anomalies)
* 🤖 Optional **local LLM (Ollama)** for custom natural-language queries
* 📈 Supports text output, tables, and visualizations
* 🔒 Runs fully locally (no data leaves your machine)

---

## 🧱 Project Architecture

```
Personal-AI-Data-Analyst/
│
├── app.py          # Streamlit UI & interaction logic
├── analyst.py      # Core analysis engine & LLM interface
├── requirements(PDA).txt
└── README.md
```

### app.py

* Handles Streamlit UI
* File upload and preview
* Prompt selection and execution
* Output rendering (text / table / chart)

### analyst.py

* Dataset loading (CSV, Excel, JSON)
* Column type detection
* Suggested analysis generation
* Prompt-to-code mapping (deterministic)
* Safe execution of generated Python code
* Optional local LLM execution via Ollama CLI

---

## 🚀 Getting Started

### 1️⃣ Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements(PDA).txt
```

Or manually:

```bash
pip install streamlit pandas matplotlib numpy scipy openpyxl
```

---

## 🤖 Optional: Enable Local LLM (Ollama)

This app can optionally use a **local LLM** for free-form analysis prompts.

### Install Ollama

Download from:
[https://ollama.com](https://ollama.com)

### Pull a model

```bash
ollama pull llama3.1
```

### Verify installation

```bash
ollama --version
```

In the app sidebar, enable:

```
☑ Use local LLM (ollama)
Model name: llama3.1
```

---

## ▶ Running the App

```bash
streamlit run app.py
```

Then open the browser URL shown in the terminal.

---

## 🧪 Example Analyses Supported

* Dataset summary (rows, columns, missing values)
* Top categories and counts
* Numeric statistics (mean, std, quartiles)
* Histograms and scatter plots
* Correlation heatmaps
* Monthly time-series aggregation
* Anomaly detection using Z-score

Custom prompts are supported when LLM mode is enabled.

---

## 🔐 Security & Safety

* Code execution is sandboxed to a limited namespace
* No arbitrary file system access
* No internet calls from the LLM
* All data remains local

---

## 🎯 Learning Outcomes

This project demonstrates:

* Practical Streamlit application development
* Real-world Exploratory Data Analysis (EDA)
* Safe dynamic code execution patterns
* Local LLM integration using CLI tools
* Clean separation of UI and logic layers

---

## 📌 Future Enhancements (Planned)

* UI theming (light/dark)
* Chat-style analysis history
* Smarter prompt understanding
* Dataset profiling report export
* Multi-tab dashboard layout

---

## 📄 License

This project is for educational and portfolio purposes.
You are free to fork and extend it.
