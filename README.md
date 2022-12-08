<h1 align="center"> NMT_DL_Project </h1> 

![This is an image](https://www.intechopen.com/media/chapter/68953/media/F1.png)

## Problem Statement :
The ability to communicate with one another is a fundamental part of our daily life. There are nearly
7,000 different languages worldwide. As our world becomes increasingly connected, language
translation provides a critical cultural and economic bridge between people from different countries
and ethnic groups. Some of the more obvious use-cases include:
* **BUSINESS:** international trade, investment, contracts, finance
* **COMMERCE:** travel, purchase of foreign goods and services, customer support
* **MEDIA:** accessing information via search, sharing information via social networks, localization of content and advertising
* **EDUCATION:** sharing of ideas, collaboration, translation of research papers
* **GOVERNMENT:** foreign relations, negotiation

To meet these needs, technology companies are investing heavily in machine translation. This
investment and recent advancements in deep learning have yielded major improvements in
translation quality.

According to Google, switching to deep learning produced a 60% increase in translation
accuracy compared to the phrase-based approach previously used in Google Translate. Today,
Google and Microsoft can translate over 100 different languages and are approaching human-level
accuracy for many of them.
However, while machine translation has made lots of progress, it’s still not perfect. �

## Objective :
The goal is to have machines translate content well enough for human translators to understand its meaning and easily improve upon the text.

## Dataset :

The dataset used in this project for the task of converting/translating one language to another
language is taken from the below website.
> http://www.manythings.org/anki/

We downloaded an English-German dataset that consists of bilingual sentence pairs from the Tatoeba Project. In this project, text in English language is being translated into German Language.

## Metadata of the Dataset :

Each line in the dataset is a tab-delimited text consisting of an English text sequence, the translated German text sequence and some information regarding attribution. Note that each text sequence can be just one sentence, or a paragraph of multiple sentences. In this machine translation problem where English is translated into German, English is called the source language and German is called the target language.

## Exploratory Analysis :

The text data available at the above mentioned website is present in the raw form( consists of
punctuations, symbols, letters in both lower & upper case). So, pre-processing has been performed on the downloaded dataset and has been made ready! to be used for implementing various Deep Learning models and architectures.

> [Pre_processing_&_analysis_NMT.ipynb](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/Pre_processing_%26_analysis_NMT.ipynb)

## Preprocessing Pipeline :
Below are a few pre-processing steps implemented on the downloaded dataset:
1. Load & examine the data.
2. Cleaning the data. (includes the following)
   * Splitting each sample/text into English-German pairs.
   * Converting the data into an array for easy implementation.
   * Reducing the size of dataset to save the computation cost.(Only in this case)
   * Removing irrelevant text like attribution details
   * Removing punctuations.
   * Converting the text to lower case.
3. Tokenizing & vectorizing the text into numerical sequences.
4. Padding those sequences with 0’s to bring them to same length.

After Pre-processing, there are 2 columns. One column has English words/sentences and the other one has German words/sentences. And this dataset can now be used for language translation task.

## Models Implemented :
1) RNN + LSTM | [Link](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/DL%20Models/Model1_RNN%2BLSTM_NMT.ipynb)
2) RNN + Embedding + BiRNN | [Link](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/DL%20Models/Model2_RNN%2BEmbedding%2BBiRNN.pynb)
3) RNN + LSTM | [Link](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/DL%20Models/Model3_RNN%2BLSTM.ipynb)
4) LSTM + Attention Mechanism | [Link](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/DL%20Models/Model4-LSTM%20%2B%20AttentionMechanism.ipynb)
5) Encoder-Decoder with Loung Attention Layer | [Link](https://github.com/manoj24vvr/Neural-Machine-Translation/blob/main/DL%20Models/Model5_Encoder-Decoder-tf2.ipynb)

## Conclusion :

Continuous improvements in the implementations of the models are important. The idea behind the attention mechanism was to permit the decoder to utilize the most relevant parts of the input sequence in a flexible manner, by a weighted combination of all the encoded input vectors, with the most relevant vectors being attributed the highest weights. 

Hence, the model with the attention mechanism among the implemented models is performing better than the others by understanding the context behind the meaning of each input sentence.

## Future scope of the project :
We can implement Neural Machine Translation by using the Transformer networks which can perform way better than any other models including the Google translate model.

For example, if the input data is a natural language sentence, the transformer does not have to process one word at a time. This allows for more parallelization than RNNs and therefore reduces training times.
