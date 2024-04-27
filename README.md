# Book Summaries
This repository is for book enthusiasts📕🪱

We have a text file of books called booksummaries.txt. Three main tasks need to be performed:
1. **Exploratory Data Analysis (EDA)**:
   - Identify and handle missing values in the dataset.

2. **NLP Summarization**:
   - Implement NLP techniques to generate condensed summaries of books from the provided text data.

3. **Computer Vision**:
   - Investigate methods for converting text summaries into images.
   - Experiment with text-to-image models to visualize book summaries.
  
# EDA Phase

In the first section, dedicated to the Exploratory Data Analysis (EDA) phase, I aimed to extract important information from each book using Regex. Additionally, leveraging together.ai and the large language model Llama, I converted an unstructured file into two structured JSON files named `bookinfo.json` and `bookInfo(withSummary).json`. 

## Dataframe Creation

The obtained data allowed me to create a dataframe with the following columns:

- **Book Name:** Name of each book.
- **Author Name:** Name of the author.
- **Publication Date:** Date when the book was published.
- **Book Genres:** Genres of the book.
- **Summary:** Summary of the book.

## Data Cleaning

Using this dataframe, I performed data cleaning operations on the columns to ensure data quality and consistency.

## Dataset Report

Finally, using the ydata_profiling library, I generated a report on the dataset, which can be found in the `bookReport.html` file.

## Missing Values Handling

Various approaches were considered to address the issue of missing values. However, so far, the desired result has not been achieved. Detailed explanations can be found in the `MissingValue.ipynb` notebook. I tried using NER language models from Hugging Face, but they fell short in performance and the powerful models demanded robust hardware resources

# NLP Summarization
In the second phase, I experimented with language models tailored for summarization available on Hugging Face. Specifically, I employed the `facebook/bart-large-cnn` model for compressing book summaries, yielding satisfactory results.

# Computer Vision
For generating visual representations of book summaries, I utilized the `Stable Diffusion` model available on Hugging Face. Stable Diffusion is a deep learning, text-to-image model released in 2022 based on diffusion techniques. It is considered to be a part of the ongoing artifical intelligence boom. Although this model provides excellent results, it demands substantial hardware resources. Due to memory constraints, I resorted to the `Clipdrop` platform, allowing me to generate images using the Stable Diffusion API. 

# Results
The generated image is available below. Additionally, I provide some statistics regarding the dataset used for evaluation.
