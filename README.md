#Halophilic Protein Classification

##Dataset
The dataset used in this study was obtained from the NCBI database. The protein sequences containing ambiguous residues, such as “X”, “B”, and “Z”, and the sequences, which are fragments of other proteins (protein length < 100) were excluded. 
To ensure non-redundancy between the two sets, redundancy reduction was performed using the MMSeqs2-UniqueProt algorithm. This algorithm reduced the sequence identity within the test set and between the training and test sets to 20% without further redundancy reduction within the training set.
The final dataset consisted of 5,018 halophilic proteins and 2,518 non-halophilic proteins. The dataset was then divided into a training set and a test set in an 80:20 ratio. It is located on /dataset/haloAdd.csv file. The file consist of identifier, sequence, label, and set columns.
Identifier column is the accession number of protein sequence.

##HOPE Model
HOPE (HalOphilic Protein classification using Embeddings) is an innovative in-silico method designed for the classification of alkaliphilic proteins using deep learning techniques. Inspired by recent advancements in language models (LMs) and protein language models (pLMs), 
HOPE employs embeddings derived from the ProtT5 pLM using a 1 dimension Capsule Network architecture. The approach bypasses manual feature extraction by leveraging natural language processing (NLP) techniques, treating protein sequences as if they were sentences and 
extracting vector representations (embeddings) directly. The comparison involved four different pretrained language models - ProtT5-XL-U50, ProstT5, Ankh, and ESM-2 with 3B parameters. These embeddings were used as input features for machine learning models, 
starting with a logistic regression model and subsequently extending to more complex models like HOPE, a one-dimensional Capsule Network.
