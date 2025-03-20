# Semantic book recommender
This project demonstrates 


how to use llm to build a semantic book recommender. The result webpage can search by *book description*, *book category*, and *emotional tone*.
.The project is based on the tutorial from the YouTube video [LLM Course – Build a Semantic Book Recommender (Python, OpenAI, LangChain, Gradio)](https://www.youtube.com/watch?v=Q7mS1VHm3Yw&ab_channel=freeCodeCamp.org) by Jodie Burchell.

## Requirements
- Python 3.x
- OpenAI account, HuggingFace account
   - create a .env file with `OPENAI_API_KEY` and `HUGGINGFACE_API_TOKEN` inside.

## Installation
1. Install Python 3.x from the official Python website.
2. Install the libraries using pip:
```
pip install -r requirements.txt
```

### Dependencies
- Langchain
- Chroma
- Gradio
- Pandas, Numpy, Matplotlib, Seaborn
- Transformers

## Usage
If you want to know the process of data preprocessing, run the jupyternotebook scripts by following order. If you only want to run the gradio app, skip to the last step.
1. data-exploration.ipynb: 
    - Download the data from kaggle
    - Perform data exploration.
    - Data preprocessing and data cleaning, and generate `data/books_cleaned.csv`.
2. vector-search.ipynb: 
    - Do word embedding on books description using OpenAI embeddings. Store in Chroma database.
    - Zero-shot classification on book categories using transformer model (facebook/bart-large-mnli). The prediction is around 78% accurate. It fills missing book categories with predictions.
    - Generate `data/books_with_categories.csv`
3. semantic-search.ipynb:
    - Do semantic text-classification on book description with transformer model (j-hartmann/emotion-english-distilroberta-base). 7 emotions are predicted. (anger, disgust, fear, joy, neutral, sadness, surprise).
    - Generate `data/books_with_emotions.csv`

4. Run the gradio app:
    - Run `python3 gradio-dashboard.py`


Areas for Improvement
Counting Error: The current implementation has counting errors that need to be improved.
