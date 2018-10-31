# dsga1011hw2
This is the second project of the DS-GA 1011 Natural Language Processing.
The project is designed to apply CNN and RNN models to classify the matches of two language sentences
which are defined as premise and hypothesis. There are three types of matched of sentence which
are treated as ’contradiction’, ’entailment’ and ’neutral’. All data used in this program comes fromthe Stanford
Natural Language Inference which can be accessed by the following link: https://nlp.stanford.edu/projects/snli/.
The definitions of the three types of matches of premise and hypothesis can be found on the website. In
this project, these three types of match are treated as labels.
The data is first loaded from the original files and tokenized. In this project, no embedding layer is
applied and jointly trained with the RNN or CNN model. Instead, a Fasttext pretrained embedding layer
has been directly applied. The pretrained model can be found at https://fasttext.cc/docs/en/englishvectors.
html. In this project, the model named ’wiki-news-300d-1M.vec’ has been used.
Two different sets of datasets are downloaded and applied in this project. One is the data set which
only contains single genre while the other one contains multi genres. The general logic of this project is
that the training set of single-genre dataset is used to trained the model and then the validation set for
single-genre dataset is used for scoring. Then consider the accuracy on the single-genre data set, the best
performed CNN and RNN model will be selected to perform prediction on the multi-genre data set. Since
there are multiple genres for the multi-genre data set. The dataset is initially divided to several subsets
with each set contains the matched of sentence with the same genre then the prediction is carried out
based on these subsets. In other words, we will perform a cross genre prediction for the multi-genre set.
Please see the source code for the detail information.
