# Financial Reports Distant Reading

Data mining of a set of annual "10-K" reports filed by three technology corporations (AMD, Intel, Qualcomm) for the periods 2010-2020.

## Project Structure

```
/
├── data/                    # Input data and processed corpus
│   ├── AMD/                 # AMD 10-K PDFs (2010-2020)
│   ├── Intel/               # Intel 10-K PDFs (2010-2020)
│   ├── Qualcomm/            # Qualcomm 10-K PDFs (2010-2020)
│   ├── Corpus_Filtered/     # Corpus without stopwords or numbers
│   └── Corpus_Bigrams/     # Corpus with bigrams
├── output/                  # Visual results
│   ├── Dist_Freq_Img/       # Frequency distribution charts
│   ├── TDIDF_Img/           # TF-IDF charts
│   ├── Voyant_AMD.svg
│   ├── Voyant_Intel.svg
│   └── Voyant_Qualcomm.svg
├── notebooks/              # Jupyter notebooks
│   ├── Text_Mining_10KReports.ipynb
│   ├── Text_Mining_10KReports_V2.ipynb
│   └── Stopwords_Especial.txt
└── README.md
```

## Functionality

1. **Text Extraction**: Reads 10-K PDF files from the SEC
2. **Preprocessing**: Tokenization, removal of numbers and stopwords
3. **Frequency Analysis**: Term distribution by year and company
4. **Bigrams**: Identification of frequent word pairs
5. **TF-IDF**: Term weighting model
6. **Visualization**: SVG trend charts

## Dependencies

- `pdfminer.six` - PDF text extraction
- `nltk` - Natural language processing
- `matplotlib` - Data visualization
- `pandas` - Data manipulation
- `scikit-learn` - TF-IDF and machine learning
- `gensim` - Topic modeling (LDA)
- `pyLDAvis` - Topic visualization
- `wordcloud` - Word clouds
- `voyant` - Text analysis (optional)

## Usage

Run the notebooks in order:
1. `Text_Mining_10KReports.ipynb` - Basic analysis
2. `Text_Mining_10KReports_V2.ipynb` - Advanced analysis with TF-IDF and LDA
