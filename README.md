# Neural-Machine-Translation-Japanese-to-English
Japanese to English Translation using Neural Networks and NLP

## Introduction
This project focuses on implementing a Neural Machine Translation model to translate Japanese sentences into English. In the field of Natural Language Processing, transformer architectures have emerged as the leading framework, achieving state-of-the-art results across a variety of tasks. Given their robustness and efficiency, transformers are expected to maintain their dominance in the near future. This project specifically utilizes the transformer architecture, as introduced in the seminal paper "Attention is All You Need," to develop a highly effective neural network model. By leveraging the power of self-attention mechanisms and the transformer architecture, this model aims to achieve accurate and fluent translations from Japanese to English.

## Datasets
The datasets consist of two datasets combines together. The first is the Kyoto Japanese English Bilingual parallel corpus. This dataset mainly deals about traditional Japanese culture, religion, and history.
The other dataset is the Anki Japnese-English Dataset. It consists more of daily life conversation or normal words that Japanese people use frequently.

## Methodolgy
### Data Preprocessing
The datasets are first imported and combined together. The Spacy Library is used for Tokenizing the data. The implementation is carried out using Pytorch so TorchText Fields are also used in preprocessing. Torch Text fields make it easy to make Dataloaders of the data for the models to train on.

### Model Architecture
Transformer model architecture also has Encoder and Decoder, but here "Multi Head Attention" is Used at Encoder and "Multi-Headed Attention" , "Masked Multi-headed Attention" are used in Decoder.
  
To prepare the input for the Encoder, we first pass tokens through an Input Embedding layer, converting them into numerical representations suitable for the model. Following this, a Positional Embedding layer is applied. This layer helps the model understand the sequence of tokens by embedding information about their relative or absolute positions within the sequence. 
  
Then Multi-Head Attention to process input tokens. This mechanism creates multiple attention vectors for each word, allowing the model to capture various aspects of word relationships. These vectors are then weighted by a learned matrix W_z which choose which attention vector to use.  
  
In the Decoder, which handles tasks like language generation or sequence-to-sequence tasks, we utilize both Multi-Head Attention and Masked Multi-Head Attention. Masked Multi-Head Attention ensures that during training, each word can only attend to previous words in the output sequence.  
  
Other typical components like Feed Forward Neural Networks and Normalization layers are used. These components enhance the model's ability to learn and generalize from the input data, ensuring effective training and performance in natural language processing tasks.

### Model Evaluation
 
