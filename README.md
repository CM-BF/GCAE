# This is a refresh version of GCAE

## requirements

* CUDA 10.0
* pytorch >= 1.0
* other packages: torchtext, nltk==3.2.5, sacremoses, simplejson

## Resources

GloVe: glove.840B.300d.txt (Please change the 2 paths in w2y.py)

Following the notice to download the nltk resources when you run the code.

Datasets:
* SemEval 2014 Task4
* SemEval 2015 Task12
* SemEval 2016 Task5

Please find them on their official website, and they will finally lead you to Metashare to download (you need a free account). To verify whether you have downloaded the right .xml file, please check 13-25 lines in getsemeval.py. You may have to change the name of 2015's .xml files.

## Run ACSA for test
```
python -m run -lr 1e-2 -batch-size 32 -verbose 1 -model CNN_Gate_Aspect -embed_file glove -r_l r -epochs 13
```


The following message is the original README file. (from https://github.com/wxue004cs/GCAE)

# Code and data for Aspect Based Sentiment Analysis with Gated Convolutional Networks

```
@inproceedings{DBLP:conf/acl/LiX18,
  author    = {Wei Xue and Tao Li},
  title     = {Aspect Based Sentiment Analysis with Gated Convolutional Networks},
  booktitle = {Proceedings of the 56th Annual Meeting of the Association for Computational
               Linguistics, {ACL} 2018, Melbourne, Australia, July 15-20, 2018, Volume
               1: Long Papers},
  pages     = {2514--2523},
  year      = {2018},
  crossref  = {DBLP:conf/acl/2018-1},
  url       = {https://aclanthology.info/papers/P18-1234/p18-1234},
  timestamp = {Thu, 12 Jul 2018 14:15:56 +0200},
  biburl    = {https://dblp.org/rec/bib/conf/acl/LiX18},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```


# Instructions:
Download glove or word2vec file and change the path in w2v.py correspondingly.

## ACSA
python -m run -lr 1e-2 -batch-size 32  -verbose 1  -model CNN_Gate_Aspect    -embed_file glove  -r_l r  -epochs 13

python -m run -lr 1e-2 -batch-size 32  -verbose 1  -model CNN_Gate_Aspect    -embed_file glove  -r_l r  -year 14 -epochs 5

## ATSA
python -m run -lr 5e-3 -batch-size 32  -verbose 1  -model CNN_Gate_Aspect  -embed_file glove  -r_l r -year 14 -epochs 6 -atsa

python -m run -lr 5e-3 -batch-size 32  -verbose 1  -model CNN_Gate_Aspect  -embed_file glove  -r_l l -year 14 -epochs 5 -atsa


