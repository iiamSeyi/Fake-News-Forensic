# Fake News Forensic – Detecting & Summarizing Misinformation with GenAI

A Retrieval-Augmented Generation (RAG) pipeline that uses embeddings, FAISS vector search, and OpenAI LLMs to detect and summarize misinformation based on fact-check data.

## Folder Structure

```
fake-news-forensic/
├── notebook.ipynb           # Main Jupyter Notebook
├── README.md                # Project documentation (this file)
└── data/                   # Folder for local datasets (optional)
```

## Requirements

Install dependencies:

```bash
pip install sentence-transformers langchain chromadb faiss-gpu openai
```

## OpenAI API Key Setup

1. Get an API key from [platform.openai.com](https://platform.openai.com/).
2. Set your API key in your code:

```python
import openai
openai.api_key = "your-key-here"
```

For Kaggle users, use:
```python
from kaggle_secrets import UserSecretsClient
openai.api_key = UserSecretsClient().get_secret("OPENAI_API_KEY")
```

⚠️ Note: You may need a paid plan depending on your usage and rate limits.

## Example Usage

```python
query = "Vaccines cause autism."
retrieved = retrieve_similar_texts(query, k=3)
explanation = generate_explanation(query, retrieved)
print(explanation)
```

## Results & Discussion

### Observations

- **Effective Retrieval:** The system consistently returns semantically relevant fact-checks.
- **Grounded LLM Output:** LLM responses are better contextualized when supported by retrieved references.
- **Prompt Flexibility:** The design allows for customizable and structured outputs.

### Limitations

- **Dataset Coverage:** Might not support novel or emerging claims.
- **Data Dependency:** Inherits any biases present in the underlying fact-check data.
- **Static Knowledge:** Does not update in real time.
- **Language Scope:** Default setup is English-only; additional languages require further configuration.

## Customization Ideas

- Use your own datasets (e.g., health claims, financial scams).
- Incorporate multilingual models.
- Replace OpenAI with Hugging Face or other open-source alternatives.
- Deploy as a web app or browser extension.

## References

- ISOT Dataset: [Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- Snopes: [Snopes](https://www.snopes.com/)
- PolitiFact: [PolitiFact](https://www.politifact.com/)
- SentenceTransformers: [SBERT](https://www.sbert.net/)
- FAISS: [FAISS GitHub](https://github.com/facebookresearch/faiss)
- OpenAI API: [OpenAI Documentation](https://platform.openai.com/docs/introduction)

## Author

Built by [Oluwaseyi Salisu](https://oluwaseyisalisu.com)  
GitHub: [ayomide1234](https://github.com/iiamSeyi)  
LinkedIn: [oluwaseyi-salisu](https://www.linkedin.com/in/oluwaseyi-salisu/)

## License

This project is open-source under the MIT License. Feel free to fork, adapt, and expand!
```

---







