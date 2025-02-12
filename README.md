
 # Effect of Explainable Artificial Intelligence on Trust of Mental Health Professionals in an AI-based System for Suicide Prevention

<p align="center">
This repository provides codes of the Boamente prototype, questionnaires regarding the Level of Trust, and quality of explanations provided by LIME. 

</p>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/adonias-caetano/Suicidal-Ideation-BERTvsLLM.git">
    <img src="logo_boamente.png" alt="Logo" width="80" height="80">
  </a>
</div>

<div align="justify">

 ## 📋 Requirements
* Google Colab
* python pandas library
* python re library
* python unidecode library
* python random library
* python word_tokenize, stopwords, sent_tokenize (nltk) libraries
* python wordcloud library
* python matplotlib.pyplot library
* python transformers library
* python seaborn library
* python imblearn.under_sampling library
* python sklearn.model_selection library
* python BertTokenizer, BertForSequenceClassification (transformers) libraries
* python sklearn.model_selection library
* python datetime library
* python numpy library
* python scipy.special library
* python TensorDataset, DataLoader, RandomSampler, SequentialSampler (torch) libraries
* python tqdm.notebook library
* python gradio library
* python lime.lime_text library

## 📖  Dataset

The <a href="https://zenodo.org/records/10070747"><strong>original dataset</strong></a> consists of 2691 sentences without suicidal ideation and 1097 sentences with suicidal ideation in PT-BR. The dataset is available in Comma-separated values (CSV) format in two columns: text and target, respectively the sentence and class 0 (negative) or 1 (positive). 

## 🛠 Fine-tuning BERT-based Models

We use BERTimbau Large (BERT-Large), a model pre-trained in Brazilian Portuguese, from <a href="https://github.com/neuralmind-ai/portuguese-bert/"><strong>BERTimbau - Portuguese BERT</strong></a>.  

The AdamW optimizer was used to adjust parameters in the model, batch size of 16, configured with a learning rate equal to 2e-6 in seven training epochs. K-fold cross-validation was performed by dividing the pre-processed dataset into 80% for training and 20% for validation. 

## 🖥️ Development methodology

In this project, two prototypes of Boamente were developed using <a href="https://www.gradio.app/"><strong>Gradio</strong></a>. The first interface was implemented without using XAI methods, i.e., it only allows the typing of sentences and the activation of the "classify" function. The second interface allows the explanation of predictions using the Local Interpretable Model-Agnostic Explanations (<a href=" https://github.com/marcotcr/lime"><strong>LIME</strong></a>) method, in addition to also classifying sentences as "contains suicidal ideation" and "does not contain suicidal ideation".

## 🤖 Access our article in Review

Paper submitted to <a href="https://ieeeaccess.ieee.org/"> <strong>IEEE Access</strong></a>

### [Paper Link]() 

## 👏 Contributing
 
If there is a bug, or other improvement you would like to report or request, we encourage you to contribute.

Please, feel free to contact us for any questions: 

* [![Gmail Badge](https://img.shields.io/badge/-ariel.teles@ifma.edu.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ariel.teles@ifma.edu.br)](mailto:ariel.teles@ifma.edu.br )
* [![Gmail Badge](https://img.shields.io/badge/-adonias.oliveira@ifce.edu.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:adonias.oliveira@ifce.edu.br)](mailto:adonias.oliveira@ifce.edu.br )

## 📄 License

### <a href="https://doi.org/10.5281/zenodo.10070747"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10070747.svg" alt="DOI"></a> 

## 📚 References

* <a href="https://www.mdpi.com/2227-9032/10/4/698"><strong>Paper about Boamente System</strong></a>.
* <a href="https://www.sciencedirect.com/science/article/pii/S1877050922009668"><strong>Paper about XAI Boamente System</strong></a>.
* <a href="https://www.scielo.br/j/csp/a/XrbVfvybPj9tvJ8qWv7j8VC/?lang=en"><strong>Paper about Generative LLMs (ChatGPT 3.5, Google Bard, and Microsoft Bing) vs BERT Models (BERTimbau and Multilingual)</strong></a>.

