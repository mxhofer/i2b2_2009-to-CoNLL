# i2b2 2009 to CoNLL parser

Code parsing i2b2 2009 clinical text data to the well-known CoNLL format for use with models like https://github.com/mxhofer/Named-Entity-Recognition-BidirectionalLSTM-CNN-CoNLL. 

Note these limitations of the parser:
1) Annotations across line breaks are not considered (losing 71 out of 23,991 total annotations)
2) Chunk tagger only tags noun phrases (NP) and verb phrases (VP) 
3) BIO annotation scheme is implemented with the tag "B-XXX" at the start of each sequence of type XXX (instead of only to differentiate consecutive tags of type XXX)

Note that subsequent i2b2 challenges (e.g. 2010 and 2012) a very similar annotation scheme. Only minor modifications are required to make the code work with those data. 

# Dataset
i2b2 2009 clinical text data (requires Data Use Agreement): https://www.i2b2.org/NLP/DataSets/Download.php 

# Dependencies
1) nltk 
2) os
3) numpy
4) pandas