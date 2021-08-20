## Art Description Generation for Paintings

<p align="center">
  <img width="460" src="https://github.com/noagarcia/explain-paintings/blob/main/main.png?raw=true">
</p>

This repository is for the annotated data in the [paper]() *Explain Me the Painting: Multi-TopicKnowledgeable Art Description Generation*, 
published at [ICCV 2021](http://iccv2021.thecvf.com/).

The code for the model introduced in the paper can be found in this other [repository]().

### Data
Art descriptions can be classified into three main topics [1]:
- Form: describes how the work looks, i.e. the constituent  elements  of  the  work  independent  of  their  meaning.
- Content: describes what the artwork is about, i.e. the message.
- Context: describes in what circumstancesthe work is or was.

In order to study automatic art description generation, we annotated a subset of the SemArt dataset [1], associating every sentence in a description to one of the above topics. 

In total, we annotated 17,249 images along with 33,543 sentences. 

We release this data to the public in order to promote research on machine learning for art.

Annotations can be found in `annotations/` directory in json format. Data format is as follows:

````
annotations[{
"img" : str, 
"description" : str
"content" : [str], 
"form" : [str], 
"context" : [str], 
}]
````

where `img` is the filename of the image in the SemArt dataset, `description` is the original description, and `content`/`form`/`context` are lists with the sentences annotated to each topic, respectively. If an image doesn't have any sentences for a certain topic, the list for that topic is empty.

[1] Robert Belton. Art history: A preliminary handbook. British Columbia: University of British Columbia, 1996.
[2] Noa Garcia and George Vogiatzis. How to read paintings:Semantic art understanding with multi-modal retrieval. In Proc. ECCV Workshops, 2018.

### Code
In the paper, we introduced a model to generate multi-topic knowledgeable description from paintings. The code for this model can be found in this [repository]().

### Maintenance
If you have questions or have any doubt about the data in this repository, please contact Noa Garcia.


### Citation

If you find the data in this repository useful, please cite our paper:
````
@InProceedings{bai2021explain,
   author    = {Zechen Bai and Yuta Nakashima and Noa Garcia},
   title     = {Explain Me the Painting: Multi-TopicKnowledgeable Art Description Generation},
   booktitle = {Proceedings of the International Conference in Computer Vision Workshops},
   year      = {2021},
}
````

