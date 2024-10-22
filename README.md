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

In the first section, dedicated to the Exploratory Data Analysis (EDA) phase, I aimed to extract important information from each book using `regex`. Additionally, leveraging [`together.ai`](https://www.together.ai/) and the large language model [`Llama`](https://ollama.com/library/llama3:8b), I converted an unstructured file into two structured JSON files named `bookinfo.json` and `bookInfo(withSummary).json`. 

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

Finally, using the `ydata_profiling` library, I generated a report on the dataset, which can be found in the `bookReport.html` file.

## Missing Values Handling

Various approaches were considered to address the issue of missing values. However, so far, the desired result has not been achieved. Detailed explanations can be found in the `MissingValue.ipynb` notebook. I tried using [NER language models](https://medium.com/@grisanti.isidoro/named-entity-recognition-with-llms-extract-conversation-metadata-94d5536178f2) from Hugging Face🤗, but they fell short in performance and the powerful models demanded robust hardware resources

# NLP Summarization
In the second phase, I experimented with language models tailored for summarization available on Hugging Face🤗. Specifically, I employed the [`facebook/bart-large-cnn`](https://huggingface.co/facebook/bart-large-cnn?text=I%27ll+give+you+the+summary+of+a+book+and+I+want+you+to+give+me+the+name+of+that+book%3A%0D%0AThe+book+follows+the+journey+of+an+Anabaptist+radical+across+Europe+in+the+first+half+of+the+16th+century+as+he+joins+in+various+movements+and+uprisings+that+come+as+a+result+of+the+Protestant+reformation.+The+book+spans+30+years+as+he+is+pursued+by+%5C%27Q%5C%27+%28short+for+%22Qo%C3%A8let%22%29%2C+a+spy+for+the+Roman+Catholic+Church+cardinal+Giovanni+Pietro+Carafa.+The+main+character%2C+who+changes+his+name+many+times+during+the+story%2C+first+fights+in+the+German+Peasants%5C%27+War+beside+Thomas+M%C3%BCntzer%2C+then+is+in+M%C3%BCnster%5C%27s+siege%2C+during+the+M%C3%BCnster+Rebellion%2C+and+some+years+later%2C+in+Venice) model for compressing book summaries, yielding satisfactory results.

# Computer Vision
For generating visual representations of book summaries, I utilized the `Stable Diffusion` model available on [Hugging Face🤗](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0?text=The+book+follows+the+journey+of+an+Anabaptist+radical+across+Europe+in+the+first+half+of+the+16th+century+as+he+joins+in+various+movements+and+uprisings+that+come+as+a+result+of+the+Protestant+reformation.+The+book+spans+30+years+as+he+is+pursued+by+%5C%27Q%5C%27+%28short+for+%22Qo%C3%A8let%22%29%2C+a+spy+for+the+Roman+Catholic+Church+cardinal+Giovanni+Pietro+Carafa.+The+main+character%2C+who+changes+his+name+many+times+during+the+story%2C+first+fights+in+the+German+Peasants%5C%27+War+beside+Thomas+M%C3%BCntzer%2C+then+is+in+M%C3%BCnster%5C%27s+siege%2C+during+the+M%C3%BCnster+Rebellion%2C+and+some+years+later%2C+in+Venice). [Stable Diffusion](https://stability.ai/stable-image) is a deep learning, text-to-image model released in 2022 from [stability.ai](https://stability.ai/) based on diffusion techniques. It is considered to be a part of the ongoing artificial intelligence boom. Although this model provides excellent results, it demands substantial hardware resources. Due to memory constraints, I resorted to the [`Clipdrop`](https://clipdrop.co/) platform, allowing me to generate images using the Stable Diffusion API. 

# Results
The first generated image is available below. Additionally, I provide some statistics regarding the dataset used for evaluation.
<div align="center">
<center><img src="https://github.com/ShayanDarabi/Book-Summaries/blob/master/img/firstGeneratedImage.png" alt="Image Description" style="width:50%;"/></center>
</div>
<div align="center">
<center><img src="https://github.com/ShayanDarabi/Book-Summaries/blob/master/img/genrebarplot.png" alt="Image Description" style="width:50%;"/></center>
</div>
<div align="center">
<center><img src="https://github.com/ShayanDarabi/Book-Summaries/blob/master/img/authorbarplot.png" alt="Image Description" style="width:50%;"/></center>
</div>
