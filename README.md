# Semantic Book Recommender
This project builds a semantic book recommender using LLMs, allowing searches by book description, book category, and emotional tone. It’s based on the [LLM Course – Build a Semantic Book Recommender (Python, OpenAI, LangChain, Gradio)](https://www.youtube.com/watch?v=Q7mS1VHm3Yw&ab_channel=freeCodeCamp.org) tutorial by Jodie Burchell on freeCodeCamp.org.

## Requirements
- Python 3.x
- OpenAI account and HuggingFace account
   - create a `.env` file with:
      ```
      OPENAI_API_KEY=your_openai_key
      HUGGINGFACE_API_TOKEN=your_hf_token
      ```
## Installation
1. Install Python 3.x from [python.org](https://www.python.org/).
2. Install dependencies:
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
To explore data preprocessing, run the Jupyter notebooks in order. To launch the Gradio app directly, skip to step 4.
1. data-exploration.ipynb: 
    - Download the data from Kaggle
    - Explores, cleans, and preprocesses data.
    - Outputs: `data/books_cleaned.csv`.
2. vector-search.ipynb: 
    - Embeds book descriptions using OpenAI embeddings, stored in a Chroma database.
    - Predicts missing book categories (~78% accuracy) with `facebook/bart-large-mnli`. (Zero-shot classification)
    - Outputs: `data/books_with_categories.csv`
3. semantic-search.ipynb:
    - Classifies book descriptions for 7 emotions (anger, disgust, fear, joy, neutral, sadness, surprise) using `j-hartmann/emotion-english-distilroberta-base`.
    - Outputs: `data/books_with_emotions.csv`

4. Run the Gradio App:
   ```
   python3 gradio-dashboard.py
   ```

