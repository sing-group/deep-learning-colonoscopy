# Deep Learning for Polyp Detection and Classification in Colonoscopy

This repository collects the most relevant studies applying Deep Learning for Polyp Detection and Classification in Colonoscopy from a technical point of view, focusing on the low-level details for the implementation of the DL models. In first place, each study is categorized in three types: (i) polyp detection and localization, (ii) polyp classification, and (iii) simultaneous polyp detection and classification. Secondly, a summary of the public datasets available as well as the private datasets used in the studies is provided. The third section focuses on technical aspects such as the Deep Learning architectures, the data augmentation techniques and the libraries and frameworks used. Finally, the fourth section summarizes the performance metrics reported by each study.

Suggestions are welcome, please check the [contribution guidelines](CONTRIBUTING.md) before submitting a pull request.

Table of Contents:

   * [Research](README.md#research)
      * [Polyp Detection and Localization](README.md#polyp-detection-and-localization)
      * [Polyp Classification](README.md#polyp-classification)
      * [Simultaneous Polyp Detection and Classification](README.md#simultaneous-polyp-detection-and-classification)
   * [Datasets](README.md#datasets)
      * [Public Datasets](README.md#public-datasets)
      * [Private Datasets](README.md#private-datasets)
   * [Deep Learning Models and Architectures](README.md#deep-learning-models-and-architectures)
      * [Deep Learning Architectures](README.md#deep-learning-architectures)
         * [Off-the-shelf Architectures](README.md#off-the-shelf-architectures)
         * [Custom Architectures](README.md#custom-architectures)
      * [Data Augmentation Strategies](README.md#data-augmentation-strategies)
      * [Frameworks and Libraries](README.md#frameworks-and-libraries)
   * [Performance](README.md#performance)
      * [Polyp Detection and Localization](README.md#polyp-detection-and-localization-1)
      * [Polyp Classification](README.md#polyp-classification-1)
      * [Simultaneous Polyp Detection and Classification](README.md#simultaneous-polyp-detection-and-classification-1)
   * [List of Acronyms and Abbreviations](README.md#list-of-acronyms-and-abbreviations)
   * [References and Further Reading](README.md#references-and-further-reading)

# Research

## Polyp Detection and Localization

Study | Date | Endoscopy type | Imaging technology | Localization type | Multiple polyp | Real time
--- | --- | --- | --- | --- | --- | ---
[Tajbakhsh et al. 2014](https://doi.org/10.1007/978-3-319-10470-6_23), [Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | Sept. 2014 / Apr. 2015 | Conventional | N/A | Bounding box | No | Yes
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | Oct. 2015 | Conventional | N/A | Bounding box (16x16 patches) | Yes | No
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | March 2016 | Conventional | NBI, WL | Bounding box | No | No
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | Jan. 2017 | Conventional | NBI, WL | Bounding box | No | No
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) |  Jan. 2017 | Conventional | NBI, WL | No | No | No
[Yuan and Meng 2017](https://doi.org/10.1002/mp.12147) | Feb. 2017 | WCE | N/A | No | No | No
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020) |  Feb. 2018 | Conventional/WCE | N/A | Binary mask | Yes | No
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) |  May 2018 | Conventional | WL | Bounding box | No | No
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003) | June 2018 | Conventional | WL | No | Yes | No
[Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | July 2018 | Conventional | NBI, WL | Bounding box | Yes | Yes
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | July 2018 | Conventional | WL | Bounding box | Yes | No
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | Sep. 2018 | Conventional | NBI, WL | Bounding box | No | Yes
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf), [GitHub](https://github.com/ahme0307/Ynet)| Sep. 2018 | Conventional | WL | Binary mask | Yes | Yes
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3), [Wang et al. 2018](http://dx.doi.org/10.1136/gutjnl-2018-317500) | Oct. 2018 | Conventional | N/A | Binary mask | Yes | Yes
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) |  Apr. 2019 | Conventional | NBI, WL | Bounding box | Yes | No
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) |  March 2019 | WCE | N/A | Bounding box | Yes | No
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) |  March 2019 | Conventional | N/A | Bounding box | Yes | Yes
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | June 2019 | Conventional | N/A | No | Yes | No
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | June 2019 | Conventional | N/A | No | No | Yes
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | June 2019 | Conventional | WL | Bounding box | Yes | Yes
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | June 2019 | Conventional/WCE | N/A | Binary mask | Yes | No
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | Sept. 2019 | Conventional | WL | Binary mask | Yes | No
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | Oct. 2019 | Conventional | N/A | Bounding box | Yes | No

## Polyp Classification

Study | Date | Endoscopy type | Imaging technology | Classes | Real time
--- | --- | --- | --- | --- | ---
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | Oct. 2016 | Conventional | WL | Neoplastic vs. Non-neoplastic | No
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Jan. 2017 | Conventional | NBI, WL | Adenoma vs. hyperplastic <br/> Resectable vs. non-resectable<br/> Adenoma vs. hyperplastic vs. serrated | No
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | Oct. 2017 | Conventional | NBI | Adenoma vs. hyperplastic | Yes
[Komeda et al. 2017](https://doi.org/10.1159/000481227) | Dec. 2017 | Conventional | NBI, WL, Chromoendoscopy | Adenoma vs. non-adenoma | No
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Feb. 2018 | Conventional | NBI | Neoplastic vs. hyperplastic | No
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Apr. 2019 | Conventional | NBI, WL | Endoscopically curable lesions vs. endoscopically incurable lesion | No
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | June 2019 | Conventional | N/A | Adenoma vs. hyperplastic vs. traditional serrated adenoma | No
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | Feb. 2020 | Conventional | NBI, BLI | *Modified Sano's (MS) classification*: MS I - Hyperplastic, MS II - Low-grade tubular adenomas, MS IIo - Nondysplastic or low-grade sessile serrated adenoma/polyp (SSA/P), MS IIIa - Tubulovillous adenomas or villous adenomas or any high-grade colorectal lesion, MS IIIb - Invasive colorectal cancers | Yes

## Simultaneous Polyp Detection and Classification

Study | Date | Endoscopy type | Imaging technology | Localization type | Multiple polyp | Classes | Real time
--- | --- | --- | --- | --- | --- | --- | ---
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Oct. 2019 | Conventional | WL | Bounding box | Yes | Polyp vs. adenoma | No
 
# Datasets
 
## Public Datasets

Dataset | References | Description | Format | Resolution (w x h) | Ground truth | Used in
--- | --- | --- | --- | --- | --- | ---
CVC-ClinicDB | [Bernal et al. 2015](https://doi.org/10.1016/j.compmedimag.2015.02.007) <br/> https://polyp.grand-challenge.org/CVCClinicDB/ | 612 sequential WL images with polyps extracted from 31 sequences with 31 different polyps. | Image | 388 × 284 | Polyp locations (binary mask)  | [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3), [Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059)
CVC-ColonDB | [Bernal et al. 2012](https://doi.org/10.1016/j.patcog.2012.03.002) <br/> [Vázquez et al. 2017](https://doi.org/10.1155/2017/4037190) | 380 sequential WL images with polyps extracted from 15 videos. | Image | 574 × 500 | Polyp locations (binary mask) | [Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404)
CVC-PolypHD | [Bernal et al. 2012](https://doi.org/10.1016/j.patcog.2012.03.002) <br/> [Vázquez et al. 2017](https://doi.org/10.1155/2017/4037190) | 56 WL images. | Image | 1920 × 1080 | Polyp locations (binary mask) | [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404)
ETIS-Larib | [Silva et al. 2014](https://doi.org/10.1007/s11548-013-0926-3) <br/> https://polyp.grand-challenge.org/EtisLarib/ | 196 WL images with polyps extracted from 34 sequences with 44 different polyps. | Image | 1225 × 966 | Polyp locations (binary mask) | [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059)
Kvasir-SEG | [Pogorelov et al. 2017](https://doi.org/10.1145/3083187.3083212) <br/> https://datasets.simula.no/kvasir-seg | 1 000 polyp images | Image | Various resolutions | Polyp locations (binary mask) | -
ASU-Mayo Clinic Colonoscopy Video | [Tajbakhsh et al. 2016](https://doi.org/10.1109/TMI.2015.2487997) <br/> https://polyp.grand-challenge.org/AsuMayo/ | 38 small SD and HD video sequences: 20 training videos annotated with ground truth and 18 testing videos without ground truth annotations. WL and NBI. | Video | N/A | Polyp locations (binary mask) | [Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026), [Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf)
CVC-ClinicVideoDB | [Angermann et al. 2017](https://doi.org/10.1007/978-3-319-67543-5_3) | 18 SD videos. | Video | 768 × 576 | Polyp locations (binary mask) | [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434)
Colonoscopic Dataset | [Mesejo et al. 2016](https://doi.org/10.1109/TMI.2016.2547947) <br/> http://www.depeca.uah.es/colonoscopy_dataset/ | 76 short videos (both NBI and WL). | Video | 768 × 576 | Polyp classification (Hyperplastic vs. adenoma vs. serrated) | [Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662)

## Private Datasets

Study | Patients | No. Images | No. Videos | No. Unique Polyps | Purpose | Comments
--- | --- | --- | --- | --- | --- | ---
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | N/A | 35 000 <br/> With polyps: 7 000 <br/> Without polyps: 28 000 | 40 short videos (20 positive and 20 negative) | N/A | Polyp localization	| -
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | N/A | 180 | - | N/A | Polyp localization | -
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | N/A | 652 <br/> With polyps: 92 | 35 (20’ to 40’) | N/A | Polyp localization | - 
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | 66 to 86 | 85 to 126 | - | N/A | Polyp classification (neoplastic vs non-neoplastic) | 8 datasets by combining: (i) with or without staining mucosa, (ii) 4 acquisition modes (without CVC, i-Scan1, i-Scan2, i-Scan3).
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662), [Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | N/A | 1930 <br/> Without polyps: 1 104 <br/> Hyperplastic: 263 <br/> Adenomatous: 563 | - | 215 polyps (65 hyperplastic and 150 adenomatous) | Polyp classification (hyperplastic vs. adenomatous) | PWH Database. <br/> Images taken under either WL or NBI endoscopy.
[Yuan and Meng 2017](https://doi.org/10.1002/mp.12147) | 35  | 4 000 <br/> Normal WCE images: 3 000 (1 000 bubbles, 1 000 turbid, and 1 000 clear) <br/> Polyp images: 1 000 | - | N/A | Polyp detection | -
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | N/A | N/A | 388 | N/A | Polyp classification (hyperplastic vs. adenomatous) | 
[Komeda et al. 2017](https://doi.org/10.1159/000481227) | N/A | 1 800 <br/> Adenomatous: 1200 <br/> Non-adenomatous: 600 | - | N/A | Polyp classification (adenomatous vs. non-adenomatous) | -
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | N/A | 2 441 <br/> Training: <br/> - Neoplastic: 1476 <br/> - Hyperplastic: 681 <br/> Testing: <br/> - Neoplastic: 188 <br/> - Hyperplastic: 96 | - | N/A | Polyp classification (hyperplastic vs. neoplastic) | -
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003) | 73 | N/A | 546 (155 positive and 391 negative) | 155 |  Polyp detection | -
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | > 2000 | 8 641 | - | 4 088 | Polyp localization | Used as training dataset.
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | N/A | 1 330 <br/> With polyps: 672  <br/> Without polyps: 658 | - | 672 | Polyp localization | Used as independent dataset for testing.
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | 9 | 44 947 <br/> With polyps: 13 292 <br/> Without polyps: 31 655 | 9 | 45 | Polyp localization | Used as independent dataset for testing.
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | 11 | N/A | 11 | 73 | Polyp localization | Used as independent dataset for testing with “deliberately more challenging colonoscopy videos.”.
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 1 290 | 5 545 <br/> With polyps: 3 634 <br/> Without polyps: 1 911 | - | N/A | Polyp localization | Used as training dataset.
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 1 138 | 27 113 <br/> With polyps: 5 541 <br/> Without polyps: 21 572 | - | 1 495 | Polyp localization | Used as testing dataset.
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 110 | - | 138 | 138 | Polyp localization | Used as testing dataset.
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 54 | - | 54 | 0 | Polyp localization | Used as testing dataset.
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | N/A | 8 000 <br/> Curable lesions: 4 000 <br/> Incurable lesions: 4 000 | - | Curable lesions: 159 <br/> Incurable lesions: 493 | Polyp classification (endoscopically curable vs. incurable lesions) | Used as training dataset. <br/> This study is focused on larger endoscopic lesions with risk of submucosal invasion and lymphovascular permeation. 
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | N/A | 567 | - | Curable: 56 <br/>  Incurable: 20 | Polyp classification (endoscopically curable vs. incurable lesions) | Used as testing dataset. <br/> This study is focused on larger endoscopic lesions with risk of submucosal invasion and lymphovascular permeation. 
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | 255 | 11 300 <br/> With polyps: 4 800 <br/> Without polyps: 6 500 | N/A | 331 polyps (OC) and 375 (CCE) | Polyp localization | CCE: Colorectal capsule endoscopy. <br/> OC: conventional optical colonoscopy.
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | 215 | 404 | - | N/A | Polyp localization | -
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | N/A | 3 017 088 | - | 930 | Polyp detection | Used as training set.
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | 64 (47 with polyps and 17 without polyps) | N/A | N/A | 87 | Polyp detection | Used as testing set.
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | 552 | N/A | - | 963 | Polyp classification (hyperplastic, sessile serrated adenomas, adenomas) | 
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | 283 | 1 991 | - | N/A | Polyp detection | Adenomatous polyps.
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | N/A | 83 716 <br/> With polyps: 14 634 <br/> Without polyps: 69 082  | 17 | 83 | Polyp localization | White Light Images.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | N/A | 55 | N/A | 67 | Polyp localization | Wireless Capsule Endoscopy videos. <br/> Used as testing set.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | N/A | 1 800 <br/> With polyps: 530 <br/> Without polyps: 1 270  | 18 | N/A | Polyp localization | Wireless Capsule Endoscopy videos. <br/> Used as training set.
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | N/A | 2 484 | - | 2 513 | Polyp localization | -
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | 1 661 | 3 428 | - | N/A | Polyp localization | -
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | 2 000 | 8 000 <br/> Polyp: 872 <br/> Adenoma: 1 210 | - | N/A | Polyp localization and classification (polyp vs. adenoma) | -
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 1 235 <br/> MS I: 103 <br/> MS II: 429 <br/> MS IIo: 293 <br/> MS IIIa: 295 <br/> MS IIIb: 115 | - | N/A | Polyp classification (5 classes) | Australian (AU) dataset (NBI). <br/> Used as training set.
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 20 <br/> MS I: 3 <br/> MS II: 5 <br/> MS IIo: 2 <br/> MS IIIa: 7 <br/> MS IIIb: 3 | - | N/A | Polyp classification (5 classes) | Japan (JP) dataset (NBI). <br/> Used as testing set.
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 49 <br/> MS I: 9 <br/> MS II: 10 <br/> MS IIo: 10 <br/> MS IIIa: 11 <br/> MS IIIb: 9 | - | N/A | Polyp classification (5 classes) | Japan (JP) dataset (BLI). <br/> Used as testing set.

# Deep Learning Models and Architectures

## Deep Learning Architectures

### Off-the-shelf Architectures

Study | Task | Models | Framework | TL | Layers fine-tuned | Layers replaced | Output layer
--- | --- | --- | --- | --- | --- | --- | ---
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | Classification | AlexNet, GoogLeNet, Fast CNN, Medium CNN, Slow CNN, VGG16, VGG19 | - | ImageNet | N/A | Layers after last CNN layer | SVM
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Detection and classification | CaffeNet | - | ImageNet and Places205 | N/A | Tested connecting classifier to each convolutional layer (5 convolutional layers) | SVM (Poly, Linear, RBF, and Tahn)
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Classification | Inception v3 | - | ImageNet | N/A | Last layer | FCL
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003), [Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | Detection | C3D | - | N/A | N/A | N/A | N/A
[Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | Localization | - | YOLOv1 | PASCAL VOC 2007 and 2012 | All | - | -
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | Localization | Inception ResNet-v2 | Faster R-CNN with post-learning schemes | COCO | All | - | RPN and detector layers
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | Localization | ResNet-50, VGG16, VGG19 | - | ImageNet <br/> Also without TL | All | Last layer | FCL
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | Localization | VGG16 | SegNet | N/A | N/A | N/A | N/A
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | Localization | ResNet101 | Mask R-CNN | COCO | All (incrementally) | Last layer | FCL
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | Localization | SSD Inception v2 | Tensorflow | N/A | N/A | - | -
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Localization and classification | Faster R-CNN with Inception Resnet v2 | Tensorflow | COCO | All | - | -

### Custom Architectures

Study | Task | Based on | Highlights
--- | --- | --- | ---
[Tajbakhsh et al. 2014](https://doi.org/10.1007/978-3-319-10470-6_23), [Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | Localization | None | Combination of classic computer vision techniques (detection and location) with DL (correction of prediction).<br/>The ML method proposes candidate polyps. Then, three sets of multi-scale patches around the candidate are generated (color, shape and temporal). Each set of patches is fed to a corresponding CNN.<br/>Each CNN has 2 convolutional layers, 2 fully connected layers, and an output layer.<br/>The maximum score for each set of patches is computed and averaged.
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | Localization | LeNet-5 | CNN fed with 32x32 images taken from patches generated via a sliding window of 16 pixels over the original images.<br/>The LeNet-5 network inspires the CNN architecture. ReLU used as activation function.<br/>Last two layers replaced with a cost-sensitive SVM.<br/>Positively selected patches are combined to generate the final output.
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | Localization | None | Based on a previous [work](https://doi.org/10.1109/TBME.2012.2188397) with no DL techniques.<br/>An initial quality assessment and preprocessing step filters and cleans images, and proposes candidate regions of interest (RoI).<br/>CNN replaces previous feature extractor. Three convolutional layers with two interspersed subsampling layers followed by a fully connected layer.<br/>A final step uses a Conditional Random Field (CRF) for RoI classification.
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | Localization | None | Two 3D-FCN are used:<br/>- An offline network trained with a training dataset.<br/>- An online network initialized with the offline weights and updated each 60 frames with the video frames. Only the last two layers are updated.<br/><br/>The last 16 frames are used for predicting each frame.<br/>Two convolutional layers followed by a pooling layer each, followed by two groups of two convolutional layers followed by a pooling layer each and finished with two convolutional layers converted from fully connected layers.<br/>The output of each network is combined to generate the final output.
[Yuan and Meng 2017](https://doi.org/10.1002/mp.12147) | Detection | Stacked Sparse AutoEncoder (SSAE) | A modification of a Sparse AutoEncoder to include an image manifold constraint, named Stacked Sparse AutoEncoder with Image Manifold Constraint (SSAEIM).<br/>SSAEIM is built by stacking three SAEIM layers followed by an output layer. Image manifold information is used on each layer.
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | Classification | Inception v3 | Last layer replaced with a fully connected layer.<br/>A credibility score is calculated for each frame with the current frame prediction and the credibility score of the previous frame.
[Komeda et al. 2017](https://doi.org/10.1159/000481227) | Classification | None | Two convolutional layers followed by a pooling layer each, followed by a final fully connected output layer.
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | Localization | AlexNet, GoogLeNet, ResNet-50, ResNet-101, ResNet-152, VGG | Networks pre-trained with PASCAL VOC and ImageNet datasets where converted into fully-connected convolutional networks by replacing the fully connected and scoring layers with a convolution layer. A final deconvolution layer with an output with the same size as the input.<br/>A regularization operation is added between every convolutional and activation layer.<br/>VGG, ResNet-101 and ResNet-152 were tested also using shape-form-shading features.
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) | Localization | YOLO | Custom architecture RYCO that consist of two networks:<br/>1. A regression-based deep learning with residual learning (ResYOLO) detection model to locate polyp in a frame.<br/>2. A Discriminative Correlation Filter (DCF) based method called [Efficient Convolution Operators (ECO)](https://doi.org/10.1109/CVPR.2017.733) to track the detected polyps.<br/><br/>The ResYOLO network detects new polyps in a frame, starting the polyp tracking.<br/>During tracking, both ResYOLO and ECO tracker are used to determine the polyp location.<br/>Tracking stops when a confidence score calculated using last frames is under a threshold value.
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | Detection | None | Two custom CNNs a proposed. First CNN is built just with convolutional, maximum pooling and fully connected layers. Second CNN also includes batch normalization layers and inception modules.
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | Localization | YOLO | The 5 CNNs used for detection (two custom, VGG16, VGG19 and ResNet-50) are modified by replacing the fully connected layers with convolutional layers.<br/>The last layer has 5 filter maps that have its outputs spaced over a grid over the input image. Each grid cell predicts its confidence with a sigmoid unit, the position of the polyp relative to the grid cell center, and its size. The final output is the weighted sum of all the adjusted positions and size predictions, weighted with the confidences.
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf) | Detection | Y-Net | The frame-work consists of two fully convolution encoder networks which are connected to a single decoder network that matches the encoder network resolution at each down-sampling operation. The network are trained with encoder specific adaptive learning rates that update the parameters of randomly initialized encoder network with a larger step size as compared to the encoder with pre-trained weights. The two encoders features are merged with a decoder network at each down-sampling paththrough sum-skip connection. .
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Classification | ResNet | Network with 5 convolutional layers and 2 fully connected layers but based on a pre-trained ResNet CNN backbone.
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | Localization | None | Framework for false positive (FP) reduction is proposed.<br/>The framework adds a FP reduction unit to an RPN network. This unit exploits temporal dependencies between frames (forward and backward) to correct the output.<br/>Faster R-CNN and SSD RPNs were tested.
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | Localization | R-CNN with AlexNet | Several modifications done to AlexNet:<br/>- Last fully connected layer replaced to output two classes.<br/>- 5 convolutional and 3 fully connected layers were fine-tuned.<br/>- Max-Pooling kernels, ReLU activation function and dropout used to avoid overfitting and build robustness to intra-class deformations.<br/>- Stochastic gradient descent with momentum used as the optimization algorithm.
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | Localization | SSD | SSD was modified to add three new pooling layers (Second-Max Pooling, Second-Min Pooling and Min-Pooling) and a new deconvolution layer whose features are concatenated to those from the Max-Pooling layer that are fed into the detection layer.<br/> Model was pre-trained on the ILSVRC CLS-LOC dataset.
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | Classification | CapsNet | A convolutional layer followed by 7 convolutional capsule layers and finalized with a global average pool by capsule type.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | Localization | Mask R-CNN | The region proposal network (RPN) uses a [Feature Pyramid Network](https://doi.org/10.1109/CVPR.2017.106) with a ResNet backbone. ResNet-50 and ResNet-101 were used, improved by extracting features from 5 different levels of layers. ResNet networks were initialized with COCO and ImageNet. Additionally, 76 random balloon images from Flickr were used to fine-tune networks initialized with COCO.<br/>The regions proposed by the RPN were filtered before the ROIAlign layer.<br/>The ROIAlign layer is followed by a pixel probability mask network, comprised of 4 convolutional layers followed by a transposed convolutional layer and a final convolutional layer with a sigmoid activation function that generates the final output. All convolutional layers except final are built with ReLU activation function.

## Data Augmentation Strategies

&nbsp; | Rotation | Flipping | Shearing | Translation | Gaussian smoothing | Crop | Scale | Resize | Random brightness | Zooming | Saturation adjustment | Random contrast | Exposure adjustment | Histogram equalization
--- | --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---:
Num. Studies | 17 | 12 | 5 | 3 | 4 | 5 | 3 | 2 | 4 | 2 | 1 | 1 | 1 | 1
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | X |  |  | X |  | X | X | X |  |  |  |  |  | 
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | X |  |  | X |  |  |  |  |  |  |  |  |  | 
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | X | X |  |  |  |  |  |  |  |  |  |  |  | 
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | X |  |  | X |  |  |  |  |  |  |  |  |  | 
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) |  | X |  |  |  | X |  | X |  |  |  |  |  | 
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020) |  | X |  |  |  |  |  |  |  |  |  |  |  | 
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) | X | X |  |  | X |  |  |  | X |  |  | X |  | 
[Zheng et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | X |  |  |  |  |  |  |  |  |  |  |  |  | 
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | X | X | X |  | X |  |  |  | X | X |  |  |  | 
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | X | X | X |  |  |  |  |  |  |  |  |  |  | 
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf)  | X | X | X |  | X |  | X |  | X |  |  |  |  | 
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | X | X | X |  |  |  |  |  |  | X |  |  |  | 
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | X | X |  |  |  | X |  |  |  |  |  |  |  | 
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | X |  |  |  |  |  |  |  |  |  |  |  |  | 
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | X |  |  |  |  |  |  |  |  |  | X |  | X | 
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | X | X | X |  | X |  | X |  |  |  |  |  |  | X
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | X | X |  |  |  |  |  |  |  |  |  |  |  | 
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | X |  |  |  |  | X |  |  | X |  |  |  |  | 
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | X | X |  |  |  | X |  |  | |  |  |  |  | 

## Frameworks and Libraries

Framework/Library | # Studies | Used by
--- | --- | --- 
Caffe | 5 | [Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087), [Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3), [Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133)
Tensorflow | 5 | [Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf), [Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576), [Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649)
Keras | 4 | [Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf)
C3D | 2 | [Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003), [Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134)
MatConvNet (MATLAB) | 1 | [Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725)

# Performance

> **Note**: Some performance metrics are not directly reported in the papers, but were derived using raw data or confusion matrices provided by them.

## Polyp Detection and Localization

Performance metrics on public and private datasets of all polyp detection and localization studies. 

- Between parentheses it is specified the type of performance metric: f = frame-based, p = polyp-based, and pa = patch.
- Between square brackets it is specified the dataset used, where “P” stands for private.
- Performances marked with an * are reported on training datasets.
- AP stands for Average Precision.

Study | Recall (sensitivity) | Precision (PPV) | Specificity | Others | Manually selected images?
--- | --- | --- | --- | --- | --- 
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | 70% (f) [P] | 63% (f) [P] | 90% (f) [P] | F1: 0.66, F2: 0.68 (f) [P] | No
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | 79.44% (pa) [P] | N/A | 79.54% (pa) [P] | Acc: 79.53% (pa) [P] | Yes
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | 86% (f) [P] * | - | 85% (f) [P] * | AUC: 0.86 (f) [P] * | Yes (on training)
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | 71% (f) [ASU-Mayo] | 88.1% (f) [ASU-Mayo] | N/A | F1: 0.786%, F2: 0.739% (f) [ASU-Mayo] | No
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | 97.6% (f) [P] | 99.4% (f) [P] | N/A | F1: 0.98, F2: 0.98, AUC: 1.00 (f) [P] | Yes
[Yuan and Meng 2017](https://doi.org/10.1002/mp.12147) | 98% (f) [P] * | 97% (f) [P] * | 99% (f) [P] * | F1: 0.98, F2: 0.98 (f) [P] | Yes
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020)  | ~90% (f) [ETIS-Larib]<br/>~90% (f) [CVC-ColonDB] | ~73% (f) [ETIS-Larib]<br/>~80% (f) [CVC-ColonDB] | N/A | F1: ~0.81, F2: ~0.86 (f) [ETIS-Larib]<br/>F1: ~0.85, F2: ~0.88 (f) [CVC-ColonDB] | Yes
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) | 71.6% (f) [ASU-Mayo] | 88.6% (f) [ASU-Mayo] | 97% (f) [ASU-Mayo] | F1: 0.792%, F2: 0.744% (f) [ASU-Mayo] | No
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003) | 90% (f) [P]<br/>94% (p) [P] | 55.1% (f) [P]<br/>48% (p) [P] | 63.3% (f) [P]<br/>40% (p) [P] | F1: 0.68 (f) 0.63 (p), F2: 0.79 (f) 0.78 (p) [P]<br/>Acc: 76.5% (f) 60% (p) [P] | No
[Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | 74% (f) [ETIS-Larib] | 77.4% (f) [ETIS-Larib] | N/A | F1: 0.757%, F2: 0.747% (f) [ETIS-Larib] | Yes
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | 80.3% (f) [ETIS-Larib]<br/>84.2% (f) [ASU-MAYO] <br/> 84.3% (f) [CVC-ClinicVideoDB] | 86.5% (f) [ETIS-Larib]<br/>82.7% (f) [ASU-MAYO]<br/>89.7% (f) [CVC-ClinicVideoDB] | N/A | F1: 0.833, F2: 0.815 (f) [ETIS-Larib]<br/>F1: 0.834, F2: 0.839 (f) [ASU-MAYO]<br/>F1: 0.869, F2: 0.853 (f) [CVC-ClinicVideoDB] | Yes (ETIS-Larib)<br/>No (ASU-Mayo, CVC-ClincVideoDB)
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | 93% (f) [P]<br/>100% (p) [P]<br/>93% (p) [P2] | 74% (f) [P]<br/>35% (p) [P]<br/>60% (p) [P2] | 93% (f) [P] | F1: 0.82, F2: 0.88 (f) [P]<br/>F1: 0.52, F2: 0.73 (p) [P]<br/>F1: 0.73, F2: 0.84 (p) [P2] | No
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 88.24% (f) [CVC-ClinicDB]<br/>94.38% (f) [P (dataset A)]<br/>91.64% (f), 100% (p) [P (dataset C)] | 93.13 (f) [CVC-ClinicDB]<br/>81.85 (f) [P (dataset A)] | 95.40% (f) [P (dataset D)] | F1: 0.91, F2: 0.89 (f) [CVC-ClinicDB]<br/>F1: 0.88, F2: 0.92, AUC: 0.984 (f) [P (dataset A)] | Yes (dataset A, CVC-ClinicDB)<br/>No (dataset C/D)
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf) | 84.4% (f) [ASU-Mayo] | 87.4 % (f) [ASU-Mayo] | N/A  | F1: 85.9%, F2: 85.0% (f) [ASU-Mayo] | No
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | 81.51% (f) [CVC-ClinicVideoDB] | 87.51% (f) [CVC-ClinicVideoDB] | 84.26% (f) [CVC-ClinicVideoDB] | F1: 0.844, F2: 0.83 (f) [CVC-ClinicVideoDB] | No
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | 97.1% (f) [P] | 91.4% (f) [P] | 93.3% (f) [P] | Acc: 96.4%, F1: 0.94, F2: 0.95 (f) [P] | N/A (not clear in the paper)
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | 76.37% (f) [P] | 93.92% (f) [P] | N/A | F1: 0.84, F2: 0.79  (f) [P] | Yes
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | 86% (p) [P] | N/A | 74% (f) [P] | - | No
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | 88.5% (f) [P] | N/A | 96.4% (f) [P] | - | No
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | 91.6% (f) [ETIS-Larib]<br/>84.5% (f) [P] | 75.3% (f) [ETIS-Larib] | 92.5% (f) [P] | F1: 0.83, F2: 0.88 (f) [ETIS-Larib] | Yes (ETIS-Larib)<br/>No (private)
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | June 2019 | Conventional | WL | Bounding box | Yes | Yes
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | 91.64% (f) [CVC-ColonDB]<br/>78.12% (f) [CVC-PolypHD]<br/>80.29% (f) [ETIS-Larib]<br/>95.52% (f) [P] | 89.94% (f) [CVC-ColonDB]<br/>83.33% (f) [CVC-PolypHD]<br/>72.93% (f) [ETIS-Larib]<br/>98.46% (f) [P] | N/A | F1: 0.9073, F2: 0.9127 (f) [CVC-ColonDB]<br/>F1: 0.8065, F2: 0.7911 (f) [CVC-PolypHD]<br/>F1: 0.7643, F2: 0.7870 (f) [ETIS-Larib]<br/>F1: 0.9667%, F2: 0.9610 (f) [P] | Yes (CVC-ClinicDB, ColonDB, ETIS-Larib)<br/>No (WCE video)
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | 86% (f) [CVC-ClinicDB]<br/>83% (f) [ETIS-Larib]<br/>93% (f) [P] | 80% (f) [CVC-ClinicDB]<br/>74% (f) [ETIS-Larib]<br/>86% (f) [P] | N/A | F1: 0.82, F2: 0.85 (f) [CVC-ClinicDB]<br/>F1: 0.79, F2: 0.81 (f) [ETIS-Larib]<br/>F1: 0.89, F2: 0.92 (f) [P]  | Yes
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) |  93.67% (f) [P] | N/A | 98.36% (f) [P]  | Accuracy: 96.04%, AP: 94.92% (f) [P] | Yes

## Polyp Classification

Performance metrics on public and private datasets of all polyp classification studies.

- Between square brackets it is specified the dataset used, where “P” stands for private. 

Study | Classes | Sensitivity | Specificity | PPV | NPV | Others | Polyp-level vs. frame-level | Dataset type
--- | --- | --- | --- | --- | --- | --- | --- | ---
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Adenoma vs. hyperplastic<br/>Resectable vs. non-resectable<br/>Adenoma vs. hyperplastic vs. serrated | 92% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.6% (adenoma vs. hyperplastic) [P] | 89.9% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>84.2% (adenoma vs. hyperplastic) [P] | 95.4% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.30% (adenoma vs. hyperplastic) [P] | 84.9% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.2% (adenoma vs. hyperplastic) [P] | Acc: 91.3% (resectable vs. non- resectable) [ColonoscopicDataset]<br/>Acc: 86.7% (adenoma vs. serrated adenoma vs. hyperplastic) [ColonoscopicDataset]<br/>Acc: 85.9% (adenoma vs. hyperplastic) [P] | frame | video (manually selected images)
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | Adenoma vs. hyperplastic | 98% [P] | 83% [P] | 90% [P] | 97% [P] | - | polyp | unaltered video
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Neoplastic vs. hyperplastic | 96.3% [P] | 78.1% [P] | 89.6% [P] | 91.5% [P] | N/A | frame | image dataset
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Endoscopically curable lesions vs. endoscopically incurable lesions | 88.2% [P] | 77.9% [P] | 92.1% [P] | 69.3% [P] | Acc: 85.5% [P] | frame | image dataset
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | Hyperplastic vs. serrated adenoma (near focus)<br/>Hyperplastic vs. adenoma (far focus) | 57.14% (hyperplastic vs. serrated) [P] <br/>75.63% (hyperplastic vs. adenoma) [P] | 68.52% (hyperplastic vs. serrated) [P] <br/>63.79% (hyperplastic vs. adenoma) [P] | N/A | N/A | Acc: 67.21% (hyperplastic vs. serrated) [P] <br/>Acc: 72.48% (hyperplastic vs. adenoma) [P] | frame | image dataset
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | 5-class (I, II, IIo, IIIa, IIIb)<br/><br/> Adenoma (classes II + IIo + IIIa) vs. hyperplastic (class I) | 97% (adenoma vs. hyperplastic) [P: AU] <br/> 100% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 100% (adenoma vs. hyperplastic) [P: JP-BLI] | 51% (adenoma vs. hyperplastic) [P: AU] <br/> 0% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 0% (adenoma vs. hyperplastic) [P: JP-BLI] | 95% (adenoma vs. hyperplastic) [P: AU] <br/> 82.4% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 77.5% (adenoma vs. hyperplastic) [P: JP-BLI] | 63.5% (adenoma vs. hyperplastic) [P: AU] <br/> - (adenoma vs. hyperplastic) [P: JP-NBI] <br/> - (adenoma vs. hyperplastic) [P: JP-BLI] | AUC (5-class): 94.3% [P: AU] <br/> AUC (5-class): 84.5% [P: JP-NBI] <br/>AUC (5-class): 90.3% [P: JP-BLI] <br/><br/>Acc: 72.3% (5-class) [P: AU] <br/> Acc: 59.8% (5-class) [P: JP-NBI] <br/> Acc: 53.1% (5-class) [P: JP-BLI] <br/><br/> Acc: 92.7% (adenoma vs. hyperplastic) [P: AU] <br/> Acc: 82.4% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> Acc: 77.5% (adenoma vs. hyperplastic) [P: JP-BLI] | frame | image dataset

## Simultaneous Polyp Detection and Classification

Performance metrics on public and private datasets of all simultaneous polyp detection and classification studies.

- Between square brackets it is specified the dataset used, where “P” stands for private.
- AP<sub>IoU</sub> stands for Average Precision and mAP<sub>IoU</sub> for Mean Average Precision (i.e. the mean of each class AP), calculated at the specified IoU (Intersection over Union) level.

Study | Classes | AP | mAP | Manually selected images?
--- | --- | --- | --- | ---
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Polyp vs. adenoma | Polyp: AP<sub>0.5</sub> =  83.39% [P]<br/>  Adenoma: AP<sub>0.5</sub> =  97.90% [P] | mAP<sub>0.5</sub> = 90.645% [P] | Yes

# List of Acronyms and Abbreviations

- AP: Average Precision.
- BLI: Blue Light Imaging.
- mAP: Mean Average Precision.
- NBI: Narrow Band Imaging.
- WCE: Wireless Capsule Endoscopy.
- WL: White Light.

# References and Further Reading

- [Object Detection Metrics](https://github.com/rafaelpadilla/Object-Detection-Metrics).
- [Evaluation metrics for object detection and segmentation: mAP](https://kharshit.github.io/blog/2019/09/20/evaluation-metrics-for-object-detection-and-segmentation).
