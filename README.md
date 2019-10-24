# Effortless Deep Training for Traffic Sign Detection Using Templates and Arbitrary Natural Images

[Lucas Tabelini Torres](https://github.com/lucastabelini), [Thiago M. Paixão](https://sites.google.com/view/thiagopx), [Rodrigo F. Berriel](http://rodrigoberriel.com), [Alberto F. De Souza](https://inf.ufes.br/~alberto), [Claudine Badue](https://www.inf.ufes.br/~claudine/), [Nicu Sebe](http://disi.unitn.it/~sebe/) and [Thiago Oliveira-Santos](https://www.inf.ufes.br/~todsantos/home)

Paper published in [IJCNN](https://www.ijcnn.org/) 2019 Conference. DOI: [10.1109/IJCNN.2019.8852086](https://doi.org/10.1109/IJCNN.2019.8852086).
![Overview](https://github.com/LCAD-UFES/publications-tabelini-ijcnn-2019/blob/master/images/overview.png)

#### Abstract

Deep learning has been successfully applied to several problems related to autonomous driving. Often, these solutions rely on large networks that require databases of real image samples of the problem (i.e., real world) for proper training. The acquisition of such real-world data sets is not always possible in the autonomous driving context, and sometimes their annotation is not feasible (e.g., takes too long or is too expensive). Moreover, in many tasks, there is an intrinsic data imbalance that most learning-based methods struggle to cope with. It turns out that traffic sign detection is a problem in which these three issues are seen altogether. In this work, we propose a novel database generation method that requires only (i) arbitrary natural images, i.e., requires no real image from the domain of interest, and (ii) templates of the traffic signs, i.e., templates synthetically created to illustrate the appearance of the category of a traffic sign. The effortlessly generated training database is shown to be effective for the training of a deep detector (such as Faster R-CNN) on German traffic signs, achieving 95.66% of mAP on average. In addition, the proposed method is able to detect traffic signs with an average precision, recall and F1-score of about 94%, 91% and 93%, respectively. The experiments surprisingly show that detectors can be trained with simple data generation methods and without problem domain data for the background, which is in the opposite direction of the common sense for deep learning. 

### Source-code

#### Faster R-CNN
The Faster R-CNN implementation used in this paper is publicly available [here](https://github.com/endernewton/tf-faster-rcnn).

#### Data set generation
New data sets can be generated with the script `generate_dataset.py`. As described in the paper, background images and templates are necessary.
### Pre-trained models
Every model trained is available [here](https://drive.google.com/drive/folders/1YUwrWCGhALFq3X8rm4dcXevNd5tE6GTN?usp=sharing).
Each model directory follows the following pattern:
`{experiment}_cycle{id}_binary_train`  
Where _experiment_ can be "germany", "germany_singleimage", or "coco_gtsd", for the upper bound, lower bound and proposed method experiments, respectively. The _id_ is the run number of the experiment (10 runs for each).

### Data sets

#### GTSDB

The German Traffic Sign Detection Benchmark (GTSDB) data set is available [here](http://benchmark.ini.rub.de/?section=gtsdb&subsection=news).

#### Data sets generated by the proposed method

An example (which was used in the paper) of a data set generated by the proposed method is available [here](https://drive.google.com/drive/folders/1YUwrWCGhALFq3X8rm4dcXevNd5tE6GTN?usp=sharing). 

### Qualitative results
[![Video1](https://github.com/LCAD-UFES/publications-tabelini-ijcnn-2019/blob/master/images/video.png)](https://www.youtube.com/watch?v=zK5qaY3uzhE)


### False False-Positives

The impact of removal of False False-Positives on the metrics and its cases can be seen in the file [False-FalsePositives.pdf](https://github.com/LCAD-UFES/publications-tabelini-ijcnn-2019/blob/master/False-FalsePositives.pdf).


#### BibTeX

```

@article{tabelini2019ijcnn,
    Author    = {Lucas Tabelini Torres and Thiago M. Paixão and Rodrigo F. Berriel and Alberto F. De Souza and Claudine Badue and Nicu Sebe and Thiago Oliveira-Santos},
    Booktitle = {International Joint Conference on Neural Networks (IJCNN)},
    Title     = {{Effortless Deep Training for Traffic Sign Detection Using Templates and Arbitrary Natural Images}},
    Year      = {2019},
    DOI       = {10.1109/IJCNN.2019.8852086}
}

```
