# Harmful Content Detection using DistilBERT

This repository contains models for detecting harmful or offensive content in Tamil, Malayalam, Kannada, and English languages, including their respective mixed languages (Tanglish, Manglish, and Kanglish). The models are built using the DistilBERT model from the Hugging Face Transformers library.

## Project Structure

The repository is organized as follows:

1. `tamil_offensive/notoffensive.ipynb`: Detects offensive words in Tamil and Tanglish using DistilBERT.
2. `malayalam.ipynb`: Detects offensive words in Malayalam and Manglish using DistilBERT.
3. `kannada.ipynb`: Detects offensive words in Kannada and Kanglish using DistilBERT.
4. `english.ipynb`: Detects offensive words in English using DistilBERT.
5. `language_classification_and_offensivedetection.py`: Classifies the language of the input text using spaCy. It handles romanized Tanglish, Manglish, and Kanglish words and uses Unicode for Tamil, Kannada, and English to find the perfect words. After predicting the language, the sentence is sent to the respective DistilBERT model saved from the above notebooks.

## Dataset

The datasets used for training these models are sourced from Hugging Face:

- [Multilingual Sentiment Datasets](https://github.com/tyqiangz/multilingual-sentiment-datasets?tab=readme-ov-file)
- [Offensive-Multi Dataset](https://huggingface.co/datasets/valurank/offensive-multi)

## Installation

To use the models, you need to install the necessary libraries. You can do this using pip:

```bash
pip install transformers spacy
```

Additionally, you need to download the spaCy language models:

```bash
python -m spacy download en_core_web_sm
python install torch transformers datasets pandas scikit-learn
python install transformers[torch]
python install accelerate -U
```

## Usage

### Notebooks

You can run the individual Jupyter notebooks (`tamil.ipynb`, `malayalam.ipynb`, `kannada.ipynb`, `english.ipynb`) to see how the DistilBERT models are trained and used for detecting offensive content.

### Language Classification

The `language_classification.py` file contains the code for classifying the language of an input sentence and sending it to the respective DistilBERT model for offensive content detection. You can run this script as follows:

```bash
python language_classification_and_offensivedetection.py
```

## Model Training

To train the DistilBERT models, follow the steps in the respective Jupyter notebooks. Each notebook demonstrates the process of loading the dataset, preprocessing the data, training the model, and evaluating its performance.

## Contributing

If you wish to contribute to this project, please follow these steps:

1. Fork this repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Hugging Face Transformers](https://github.com/huggingface/transformers)
- [spaCy](https://github.com/explosion/spaCy)

