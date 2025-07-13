# 🧠 RAG-Based Loan Approval Q&A Chatbot

This project demonstrates a Retrieval-Augmented Generation (RAG) chatbot built using a loan approval dataset. It combines document retrieval with a language model to answer questions based on structured loan data, and features a Streamlit UI for easy interaction.

---

## 📦 Project Files

| File Name                   | Description                                                   |
|----------------------------|---------------------------------------------------------------|
| `Training Dataset.csv`     | Raw loan data for training                                    |
| `Testing Dataset.csv`      | Extra data for evaluation or future extension                 |
| `RAG_Loan_Approval_Chatbot.ipynb` | Jupyter notebook with complete data loading, embedding, RAG setup |
| `rag_index.pkl`            | Precomputed FAISS index + documents for fast chatbot startup  |
| `app.py`                   | Streamlit-based chatbot interface                             |

---

## 🚀 How to Run the Chatbot

1. Clone this repository or download all files.
2. Install required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the Streamlit chatbot:
   ```bash
   streamlit run app.py
   ```

---

## 💬 Example Questions

- What is the average loan amount for approved applicants?
- Which education group has the most loan rejections?
- What kind of applicants are more likely to be approved?
- How does credit history affect loan approval?

---

## 📊 Bonus: Data-Driven Analysis

The notebook also includes a Pandas-based analytical block:
```python
approved = df[df['Loan_Status'] == 'Y']
print("✅ Average Loan Amount (Approved):", round(approved['LoanAmount'].mean(), 2))
```

> ✅ Example Output: `Average Loan Amount (Approved): 146.41`

---

## 📚 Tech Stack

- `LangChain` + `FAISS` for semantic retrieval
- `sentence-transformers` for embeddings
- `transformers` (Falcon RW-1B) for generative answers
- `Streamlit` for user interface
- `Pandas` for statistical insights

---

## 🏁 Project Context

Developed as **Assignment 8** for the **Data Science Internship** at **Celebal Technologies**.

---
