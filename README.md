## Art Description Generation for Paintings

<p align="center">
  <img width="460" src="https://github.com/noagarcia/explain-paintings/blob/main/main.png?raw=true">
</p>

This repository is for the annotated data in the paper [Explain Me the Painting: Multi-TopicKnowledgeable Art Description Generatio](), 
published at [ICCV 2021](http://iccv2021.thecvf.com/).

The code for the model introduced in the paper can be found in this other [repository](https://github.com/JosephPai/Art-Description).

### Data
Art descriptions can be classified into three main topics [1]:
- **Form**: describes how the artwork looks.
- **Content**: describes what the artwork is about.
- **Context**: describes in what circumstances the work was done.

In order to study art description generation, we annotated a subset of the [SemArt dataset](https://noagarcia.github.io/SemArt/) [2], associating each sentence in a description to one of the above topics. 

In total, we annotated 33,543 sentences from 17,249 images. 

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

### Code
In the paper, we introduced a model to generate multi-topic knowledgeable description from paintings. The code for this model can be found in this [repository](https://github.com/JosephPai/Art-Description).

### Maintenance
If you have questions about the data in this repository, please contact Noa Garcia.

### References

[1] Robert Belton. [Art history: A preliminary handbook](https://d1wqtxts1xzle7.cloudfront.net/43880410/Preliminary_Handbook.pdf?1458371315=&response-content-disposition=inline%3B+filename%3DArt_History_A_Preliminary_Handbook_1996.pdf&Expires=1629445880&Signature=DtZmXwPBVzDayjhCpAPaJz1-ec44G5YFabIIs7STd~VTzjtLovcOsZOFYRn14lUraqvRG54b8Zxj8F~QJFhUEr3SWUUMUItGEDYQnZ1cMFjEwolLJ-G~xQO~~GXEGgJ5gI8scaczglTi~SckS0dSCPrVBtsMwQ794oHK~nsF4K2EilyLR4PHOpk0iPyF5Q8xgd~sY512wj2Eij6C8mdesFJe6CtZQH-ty-voHbgSwYrNcrbhg0gnGnWxJ~f9ioHmdvry8AwizfNTj7AyOmLBIP5XWZ~d1vurr6gyjB6PyEKu8dBHr2SaAF2ofibTK~thGN959hYcfe3wRtqDMN6r7Q__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA). British Columbia: University of British Columbia, 1996.

[2] Noa Garcia and George Vogiatzis. [How to read paintings:Semantic art understanding with multi-modal retrieval](https://arxiv.org/abs/1810.09617). In Proc. ECCV Workshops, 2018.


### Citation

If you find the data in this repository useful, please cite our paper:
````
@InProceedings{bai2021explain,
   author    = {Zechen Bai and Yuta Nakashima and Noa Garcia},
   title     = {Explain Me the Painting: Multi-Topic Knowledgeable Art Description Generation},
   booktitle = {International Conference in Computer Vision},
   year      = {2021},
}
````

