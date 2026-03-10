# Lectura distante de reportes financieros

Data mining de un conjunto de reportes anuales "10-K" presentados por tres corporaciones tecnológicas (AMD, Intel, Qualcomm) para los periodos 2010-2020.

## Estructura del proyecto

```
/
├── data/                    # Datos de entrada y corpus procesado
│   ├── AMD/                 # PDFs 10-K de AMD (2010-2020)
│   ├── Intel/               # PDFs 10-K de Intel (2010-2020)
│   ├── Qualcomm/            # PDFs 10-K de Qualcomm (2010-2020)
│   ├── Corpus_Filtered/     # Corpus sin stopwords ni números
│   └── Corpus_Bigrams/     # Corpus con bigramas
├── output/                  # Resultados visuales
│   ├── Dist_Freq_Img/       # Gráficos de frecuencia
│   ├── TDIDF_Img/           # Gráficos TF-IDF
│   ├── Voyant_AMD.svg
│   ├── Voyant_Intel.svg
│   └── Voyant_Qualcomm.svg
├── notebooks/              # Notebooks Jupyter
│   ├── Text_Mining_10KReports.ipynb
│   ├── Text_Mining_10KReports_V2.ipynb
│   └── Stopwords_Especial.txt
└── README.md
```

## Funcionalidad

1. **Extracción de texto**: Lee archivos PDF 10-K de la SEC
2. **Preprocesamiento**: Tokenización, eliminación de números y stopwords
3. **Análisis de frecuencia**: Distribución de términos por año y empresa
4. **Bigramas**: Identificación de pares de palabras frecuentes
5. **TF-IDF**: Modelo de ponderación de términos
6. **Visualización**: Gráficos SVG de tendencias

## Dependencias

- `pdfminer.six` - Extracción de texto de PDFs
- `nltk` - Procesamiento de lenguaje natural
- `matplotlib` - Visualización de datos
- `pandas` - Manipulación de datos
- `scikit-learn` - TF-IDF y machine learning
- `gensim` - Modelado de temas (LDA)
- `pyLDAvis` - Visualización de temas
- `wordcloud` - Nubes de palabras
- `voyant` - Análisis de texto (opcional)

## Uso

Ejecutar los notebooks en orden:
1. `Text_Mining_10KReports.ipynb` - Análisis básico
2. `Text_Mining_10KReports_V2.ipynb` - Análisis avanzado con TF-IDF y LDA
