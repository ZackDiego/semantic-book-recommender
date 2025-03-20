# Semantic book recommender
This project demonstrates .....The project is based on the tutorial from the YouTube video [LLM Course – Build a Semantic Book Recommender (Python, OpenAI, LangChain, Gradio)](https://www.youtube.com/watch?v=Q7mS1VHm3Yw&ab_channel=freeCodeCamp.org) by Jodie Burchell.

## Requirements
- Python 3.x
- OpenAI account, HuggingFace account
   - create a .env file with `OPENAI_API_KEY` and `HUGGINGFACE_API_TOKEN` inside.

## Run the app
1. Install Python 3.x from the official Python website.
2. Install the libraries using pip:
```
pip install -r requirements.txt
```

## Dependencies
- Langchain
- Chroma
- Gradio
- Pandas, Numpy, Matplotlib, Seaborn
- Transformers

## Usage
Run the jupyternotebook scripts by following order:
1. data-exploration.ipynb: download the data, data exploration, and data cleaning (generate books_cleaned.csv).
2. vector-search.ipynb: vector search for book recommendations.
3. semantic-search.ipynb: semantic search for book recommendations.





Script Explanation
The script performs the following steps:


Areas for Improvement
Counting Error: The current implementation has counting errors that need to be improved.
