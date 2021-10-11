# Deep Learning for Polyp Detection and Classification in Colonoscopy
> This repository was created from the following review paper: A. Nogueira-Rodríguez; R. Domínguez-Carbajales; H. López-Fernández; Á. Iglesias; J. Cubiella; F. Fdez-Riverola; M. Reboiro-Jato; D. Glez-Peña (2020) [**Deep Neural Networks approaches for detecting and classifying colorectal polyps**](https://doi.org/10.1016/j.neucom.2020.02.123). *Neurocomputing*.
>
> Please, cite it if you find it useful for your research.

This repository collects the most relevant studies applying Deep Learning for Polyp Detection and Classification in Colonoscopy from a technical point of view, focusing on the low-level details for the implementation of the DL models. In first place, each study is categorized in three types: (i) polyp detection and localization, (ii) polyp classification, and (iii) simultaneous polyp detection and classification (i.e. studies based on the usage of a single model such as YOLO or SSD to performs simultaneous polyp detection and classification). Secondly, a summary of the public datasets available as well as the private datasets used in the studies is provided. The third section focuses on technical aspects such as the Deep Learning architectures, the data augmentation techniques and the libraries and frameworks used. Finally, the fourth section summarizes the performance metrics reported by each study.

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
      * [Reviews](README.md#reviews)
      * [Randomized Clinical Trials](README.md#randomized-clinical-trials)

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
[Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645) | Sept. 2019 | WCE | N/A | No | No | No
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | Oct. 2019 | Conventional | N/A | Bounding box | Yes | No
[Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827) | Jan. 2020 | Conventional | N/A | Binary mask | Yes | No
[Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663) | May 2020 | Conventional | N/A | Bounding box | Yes | No
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | May 2020 | Conventional | N/A | Bounding box | Yes | Yes
[Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927) | Oct. 2020 | Conventional | N/A | No | No | No
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | Dec. 2020 | Conventional | N/A | Bounding box | No | Yes
[Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897) | Feb. 2021 | Conventional | WL | Bounding box | Yes | Yes
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503) | Feb. 2021 | Conventional | WL | Bounding box | Yes | Yes
[Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519) | July 2021 | Conventional | WL | Bounding box | Yes | Yes
[Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052) | July 2021 | Conventional | N/A | Bounding box | Yes | Yes
[Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4) | August 2021 | Conventional | NBI, WL | Bounding box | Yes | Yes

## Polyp Classification

Study | Date | Endoscopy type | Imaging technology | Classes | Real time
--- | --- | --- | --- | --- | ---
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | Oct. 2016 | Conventional | WL | Neoplastic vs. Non-neoplastic | No
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Jan. 2017 | Conventional | NBI, WL | Adenoma vs. hyperplastic <br/> Resectable vs. non-resectable<br/> Adenoma vs. hyperplastic vs. serrated | No
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | Oct. 2017 | Conventional | NBI | Adenoma vs. hyperplastic | Yes
[Komeda et al. 2017](https://doi.org/10.1159/000481227) | Dec. 2017 | Conventional | NBI, WL, Chromoendoscopy | Adenoma vs. non-adenoma | No
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Feb. 2018 | Conventional | NBI | Neoplastic vs. hyperplastic | No
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Apr. 2019 | Conventional | NBI, WL | Endoscopically curable lesions vs. endoscopically incurable lesion | No
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | June 2019 | Conventional | N/A | Adenoma vs. hyperplastic vs. serrated (sessile serrated adenoma/traditional serrated adenoma) | No
[Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429) | Oct. 2019 | Conventional | NBI, WL | Adenoma vs. serrated | Yes
[Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816) | Dec. 2019 | Conventional | N/A | *Paris classification*: not dangeours (types Ip, Is, IIa, and IIb) vs. dangerous (type  IIc) vs. cancer (type III) | No
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | Jan. 2020 | Conventional | WL | *Kudo's classification*: malignant (types I, II, III, and IV) vs. non-malignant (type V) | No
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | Feb. 2020 | Conventional | NBI, BLI | *Modified Sano's (MS) classification*: MS I (Hyperplastic) vs. MS II (Low-grade tubular adenomas) vs. MS IIo (Nondysplastic or low-grade sessile serrated adenoma/polyp [SSA/P]) vs. MS IIIa (Tubulovillous adenomas or villous adenomas or any high-grade colorectal lesion) vs. MS IIIb (Invasive colorectal cancers) | Yes
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) | May 2020 | Conventional | WL | 7-class: CRC T1 vs. CRC T2 vs. CRC T3 vs. CRC T4 vs. high-grade dysplasia (HGD) vs. tubular adenoma with or without low grade dysplasia (TA) vs. non-neoplastic lesions <br/><br/> 4-class: advanced CRC (T2, T3, and T4) vs. early CRC/HGD (CRC T1 and HGD) vs. TA vs. non-neoplastic lesions <br/><br/> Advanced colorectal lesions (HGD and T1, T2, T3, and T4 lesions) vs. non-advanced colorectal lesions (TA and non-neoplastic lesions) <br/><br/> Neoplastic lesions (TA, HGD, and stages T1, T2, T3, and T4) vs. non-neoplastic lesions | No

## Simultaneous Polyp Detection and Classification

Study | Date | Endoscopy type | Imaging technology | Localization type | Multiple polyp | Classes | Real time
--- | --- | --- | --- | --- | --- | --- | ---
[Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521)<sup>1</sup> | Apr. 2019 | Conventional | N/A | Bounding box | Yes | *Modified Sano's (MS) classification*: MS I (Hyperplastic) vs. MS II (Low-grade tubular adenomas) vs. MS IIo (Nondysplastic or low-grade sessile serrated adenoma/polyp [SSA/P]) vs. MS IIIa (Tubulovillous adenomas or villous adenomas or any high-grade colorectal lesion) vs. MS IIIb (Invasive colorectal cancers) | No
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Oct. 2019 | Conventional | WL | Bounding box | Yes | Polyp vs. adenoma | No
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659)<sup>2</sup> | Feb. 2020 | Conventional | NBI, WL | Bounding box | Yes | Adenoma vs. hyperplastic vs. sesile serrated adenoma/polyp (SSAP) vs. cancer vs. other types (Peutz-Jeghers, juvenile, or inflammation polyps) | Yes

1. Tian X. et al. 2019 is based on the usage of a single model (RetinaNet) that performs simultaneous polyp detection and classification. However, the paper only reports detection results using the ETIS-Larib dataset and therefore this results are included in the [Polyp Detection and Localization](README.md#polyp-detection-and-localization-1) section.
2. Ozawa. et al. 2020 work is based on the usage of a single model (Single Show MultiBox Detector, SSD) that performs simultaneous polyp detection and classification. Nevertheless, since the detection and classification results are reported independently, they are included in the sections [Polyp Detection and Localization](README.md#polyp-detection-and-localization-1) and [Polyp Classification](README.md#polyp-classification-1), respectively.

# Datasets
 
## Public Datasets

Dataset | References | Description | Format | Resolution (w x h) | Ground truth | Used in
--- | --- | --- | --- | --- | --- | ---
CVC-ClinicDB | [Bernal et al. 2015](https://doi.org/10.1016/j.compmedimag.2015.02.007) <br/> https://polyp.grand-challenge.org/CVCClinicDB/ | 612 sequential WL images with polyps extracted from 31 sequences with 31 different polyps. | Image | 388 × 284 | Polyp locations (binary mask)  | [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3), [Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827), [Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663), [Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1), [Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735), [Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897), [Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503), [Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519), [Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052)
CVC-ColonDB | [Bernal et al. 2012](https://doi.org/10.1016/j.patcog.2012.03.002) <br/> [Vázquez et al. 2017](https://doi.org/10.1155/2017/4037190) | 380 sequential WL images with polyps extracted from 15 videos. | Image | 574 × 500 | Polyp locations (binary mask) | [Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827), [Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735), [Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897), [Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503), [Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519)
CVC-EndoSceneStill | [Vázquez et al. 2017](https://doi.org/10.1155/2017/4037190) | 912 WL images with polyps extracted from 44 videos (CVC-ClinicDB + CVC-ColonDB). | Image | 574 × 500, 388 × 284  | Locations for polyp, background, lumen and specular lights (binary mask) | -
CVC-PolypHD | [Bernal et al. 2012](https://doi.org/10.1016/j.patcog.2012.03.002) <br/> [Vázquez et al. 2017](https://doi.org/10.1155/2017/4037190) | 56 WL images. | Image | 1920 × 1080 | Polyp locations (binary mask) | [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404)
ETIS-Larib | [Silva et al. 2014](https://doi.org/10.1007/s11548-013-0926-3) <br/> https://polyp.grand-challenge.org/EtisLarib/ | 196 WL images with polyps extracted from 34 sequences with 44 different polyps. | Image | 1225 × 966 | Polyp locations (binary mask) | [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521), [Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827), [Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735), [Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897), [Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503), [Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519), [Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052)
Kvasir-SEG / HyperKvasir | [Pogorelov et al. 2017](https://doi.org/10.1145/3083187.3083212) <br/> [Borgli et al. 2020](https://doi.org/10.1038/s41597-020-00622-y) <br/> https://datasets.simula.no/kvasir-seg <br/> https://datasets.simula.no/hyper-kvasir/ | 1 000 polyp images | Image | Various resolutions | Polyp locations (binary mask) | [Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735)
ASU-Mayo Clinic Colonoscopy Video | [Tajbakhsh et al. 2016](https://doi.org/10.1109/TMI.2015.2487997) <br/> https://polyp.grand-challenge.org/AsuMayo/ | 38 small SD and HD video sequences: 20 training videos annotated with ground truth and 18 testing videos without ground truth annotations. WL and NBI. | Video | N/A | Polyp locations (binary mask) | [Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026), [Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf)
CVC-ClinicVideoDB | [Angermann et al. 2017](https://doi.org/10.1007/978-3-319-67543-5_3) | 18 SD videos. | Video | 768 × 576 | Polyp locations (binary mask) | [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434), [Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663), [Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503)
Colonoscopic Dataset | [Mesejo et al. 2016](https://doi.org/10.1109/TMI.2016.2547947) <br/> http://www.depeca.uah.es/colonoscopy_dataset/ | 76 short videos (both NBI and WL). | Video | 768 × 576 | Polyp classification (Hyperplastic vs. adenoma vs. serrated) | [Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662)
PICCOLO | [Sánchez-Peralta et al. 2020](https://doi.org/10.3390/app10238501) <br/> https://www.biobancovasco.org/en/Sample-and-data-catalog/Databases/PD178-PICCOLO-EN.html | 3433 images (2131 WL and 1302 NBI) from 76 lesions from 40 patients. | Image | 854 × 480, 1920 × 1080 | Polyp locations (binary mask) <br/> Polyp classification, including: Paris and NICE classifications, Adenocarcinoma vs. Adenoma vs. Hyperplastic, and histological stratification | -
LDPolypVideo | [Ma Y. et al. 2021](https://doi.org/10.1007/978-3-030-87240-3_37) <br/> https://github.com/dashishi/LDPolypVideo-Benchmark | 160 videos (40 266 frames: 33 884 polyp images and 6 382 no-polyp images) with 200 labeled polyps. <br/> 103 videos (861 400 frames: 371 400 polyp images and 490 000 no-polyp images) without full annotations. | Video | 768 x 576 (videos), 560 × 480 (images) | Polyp locations (bounding box) | -

## Private Datasets

Study | Patients | No. Images | No. Videos | No. Unique Polyps | Purpose | Comments
--- | --- | --- | --- | --- | --- | ---
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | N/A | 35 000 <br/> With polyps: 7 000 <br/> Without polyps: 28 000 | 40 short videos (20 positive and 20 negative) | N/A | Polyp localization	| -
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | N/A | 180 | - | N/A | Polyp localization | -
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | N/A | 652 <br/> With polyps: 92 | 35 (20’ to 40’) | N/A | Polyp localization | - 
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | 66 to 86 | 85 to 126 | - | N/A | Polyp classification (neoplastic vs non-neoplastic) | 8 datasets by combining: (i) with or without staining mucosa, (ii) 4 acquisition modes (without CVC, i-Scan1, i-Scan2, i-Scan3).
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662), [Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | N/A | 1930 <br/> Without polyps: 1 104 <br/> Hyperplastic: 263 <br/> Adenomatous: 563 | - | 215 polyps (65 hyperplastic and 150 adenomatous) | Polyp classification (hyperplastic vs. adenomatous) | PWH Database. <br/> Images taken under either WL or NBI endoscopy.
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
[Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521) | 218 | 871 <br/> MS I: 102 <br/> MS II: 346 <br/> MS IIo: 281 <br/> MS IIIa: 79 <br/> MS IIIb: 63 | - | N/A | Polyp classification (5 classes) | -
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | 255 | 11 300 <br/> With polyps: 4 800 <br/> Without polyps: 6 500 | N/A | 331 polyps (OC) and 375 (CCE) | Polyp localization | CCE: Colorectal capsule endoscopy. <br/> OC: conventional optical colonoscopy.
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | 215 | 404 | - | N/A | Polyp localization | -
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | N/A | 3 017 088 | - | 930 | Polyp detection | Used as training set.
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | 64 (47 with polyps and 17 without polyps) | N/A | N/A | 87 | Polyp detection | Used as testing set.
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | 552 | N/A | - | 963 | Polyp classification (hyperplastic, serrated adenomas (sessile/traditional), adenomas) | 
[Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429) | N/A | 5 278 <br/> Adenoma: 3 310 <br/> Serrated: 1 968 | - | 5 278 | Polyp classification (adenoma vs. serrated) | Used as training set.
[Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429) | N/A | 634 | - | N/A | Polyp classification (adenoma vs. serrated) | Used as testing set.
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | 283 | 1 991 | - | N/A | Polyp detection | Adenomatous polyps.
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | N/A | 83 716 <br/> With polyps: 14 634 <br/> Without polyps: 69 082  | 17 | 83 | Polyp localization | White Light Images.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | N/A | 55 | N/A | 67 | Polyp localization | Wireless Capsule Endoscopy videos. <br/> Used as testing set.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | N/A | 1 800 <br/> With polyps: 530 <br/> Without polyps: 1 270  | 18 | N/A | Polyp localization | Wireless Capsule Endoscopy videos. <br/> Used as training set.
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | N/A | 2 484 | - | 2 513 | Polyp localization | -
[Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645) | 80 | 7 200 <br/> Polyp images: 1 200 <br/> Normal images (mucosa, bubbles, and turbid): 6 000 | 80 | N/A | Polyp detection | -
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | 1 661 | 3 428 | - | N/A | Polyp localization | -
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | 2 000 | 8 000 <br/> Polyp: 872 <br/> Adenoma: 1 210 | - | N/A | Polyp localization and classification (polyp vs. adenoma) | -
[Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816) | N/A | 785 <br/> Not dangerous: 699 <br/> Dangerous: 25<br/> Cancer: 61 | - | N/A | Polyp classification (not dangerous vs. dangerous vs. cancer) | -
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | 142 | 600 <br/> Type I: 47 <br/> Type II: 90 <br/> Type III: 183 <br/> Type IV: 187 <br/> Type V: 93 | - | N/A | Polyp classification (malignant vs. non-malignant) | -
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 1 235 <br/> MS I: 103 <br/> MS II: 429 <br/> MS IIo: 293 <br/> MS IIIa: 295 <br/> MS IIIb: 115 | - | N/A | Polyp classification (5 classes) | Australian (AU) dataset (NBI). <br/> Used as training set.
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 20 <br/> MS I: 3 <br/> MS II: 5 <br/> MS IIo: 2 <br/> MS IIIa: 7 <br/> MS IIIb: 3 | - | N/A | Polyp classification (5 classes) | Japan (JP) dataset (NBI). <br/> Used as testing set.
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | N/A | 49 <br/> MS I: 9 <br/> MS II: 10 <br/> MS IIo: 10 <br/> MS IIIa: 11 <br/> MS IIIb: 9 | - | N/A | Polyp classification (5 classes) | Japan (JP) dataset (BLI). <br/> Used as testing set.
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659) | 3 417 (3 021 with polyps and 396 without polyps) | 20 431 <br/><br/> WL: 17 566 <br/> - Adenoma: 9 310 <br/> - Hyperplastic: 2 002 <br/> - SSAP: 116 <br/> - Cancer: 1 468 <br/> - Other types: 657 <br/> - Normal mucosa: 4 013 <br/><br/> NBI: 2 865 <br/> - Adenoma: 2 085 <br/> - Hyperplastic: 519 <br/> - SSAP: 23 <br/> - Cancer: 131 <br/> - Other types: 107 <br/> - Normal mucosa: 0 | - | 4 752 <br/> Adenoma: 3 513 <br/> Hyperplastic: 1 058 <br/> SSAP: 22 <br/> Cancer: 68 <br/> Other types: 91 | Polyp localization and classification (Adenoma vs. hyperplastic vs. SSAP vs. cancer vs. other types) | Used as training set.
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659) | 174 | 7 077 <br/><br/> WL: 6 748 <br/> - Adenoma: 639 <br/> - Hyperplastic: 145 <br/> - SSAP: 33 <br/> - Cancer: 30 <br/> - Other types: 27 <br/> - Normal mucosa: 5 874 <br/><br/> NBI: 329 <br/> - Adenoma: 208 <br/> - Hyperplastic: 69 <br/> - SSAP: 8 <br/> - Cancer: 3 <br/> - Other types: 10 <br/> - Normal mucosa: 31 | - | 309 <br/> Adenoma: 218 <br/> Hyperplastic: 63 <br/> SSAP: 7 <br/> Cancer: 4 <br/> Other types: 17 | Polyp localization and classification (Adenoma vs. hyperplastic vs. SSAP vs. cancer vs. other types) | Used as testing set.
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | 103 | 8 075 | 181 | N/A | Polyp localization | Used as training set.
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | 203 | 420 | N/A | 322 hyperplastic or sessile serrated adenomas | Polyp localization | Used as training set.
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | 7 | 108 778 <br/> - With polyps: 7 022 <br/> - Without polyps: 101 756 | 7 | 26 | Polyp localization | Used as testing set.
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) | 1 339 | 3 828 <br/> - Tubular adenoma: 1 316 <br/> - Non-neoplastic: 896 <br/> - High-grade dysplasia: 621 <br/> | - | N/A | Polyp classification | Used as training/test set.
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) | 240 | 240 <br/> - Tubular adenoma: 116 <br/> - Non-neoplastic: 113 <br/> - Early CRC/High-grade dysplasia: 8<br/> - Advanced CRC: 3 | - | N/A | Polyp classification | External validation dataset.
[Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927) | - | 7 384 <br/> - With polyps: 509 <br/> - Without polyps: 6 875 | 23 | N/A | Polyp detection | Colonoscopy videos obtained from YouTube, VideoGIE, and Vimeo.
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | 123 | 79 284 | 157 | N/A | Polyp localization | Used as development (train/validation split) dataset.
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | - |  2 678 | - | N/A | Polyp localization | Used as development (train/validation split) dataset.
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | 34 | - | 42 | N/A | Polyp localization | Used as testing dataset.
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503) | 262 | 1 482 | - | 1 683 | Polyp localization | RenjiImageDB. Used as testing set.
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503) | 14 |  8 837 <br/> With polyps:  3 294 <br/> Without polyps: 5 543 | 14 | 15 | Polyp localization | RenjiVideoDB. Used as testing set.
[Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4) | 330 |  28 576 <br/> White-light: 21 046 <br/> NBI:  7530 | - | 941 | Polyp localization | -

# Deep Learning Models and Architectures

## Deep Learning Architectures

### Off-the-shelf Architectures

Study | Task | Models | Framework | TL | Layers fine-tuned | Layers replaced | Output layer
--- | --- | --- | --- | --- | --- | --- | ---
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | Classification | AlexNet, GoogLeNet, Fast CNN, Medium CNN, Slow CNN, VGG16, VGG19 | - | ImageNet | N/A | Layers after last CNN layer | SVM
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Detection and classification | CaffeNet | - | ImageNet and Places205 | N/A | Tested connecting classifier to each convolutional layer (5 convolutional layers) | SVM (Poly, Linear, RBF, and Tahn)
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Classification | Inception v3 | - | ImageNet | N/A | Last layer | FCL
[Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521) | Localization and Classification | RetinaNet (based on ResNet-50) | N/A | ImageNet | N/A | Last layer | N/A
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003), [Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | Detection | C3D | - | N/A | N/A | N/A | N/A
[Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | Localization | - | YOLOv1 | PASCAL VOC 2007 and 2012 | All | - | -
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | Localization | Inception ResNet-v2 | Faster R-CNN with post-learning schemes | COCO | All | - | RPN and detector layers
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | Localization | ResNet-50, VGG16, VGG19 | - | ImageNet <br/> Also without TL | All | Last layer | FCL
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | Localization | VGG16 | SegNet | N/A | N/A | N/A | N/A
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | Localization | ResNet101 | Mask R-CNN | COCO | All (incrementally) | Last layer | FCL
[Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645) | Detection | DenseNet | Tensorflow | - | All | - | FCL
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | Localization | SSD Inception v2 | Tensorflow | N/A | N/A | - | -
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Localization and classification | Faster R-CNN with Inception Resnet v2 | Tensorflow | COCO | All | - | -
[Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429) | Classification | Inception ResNet-v2 | Tensorflow | ImageNet | N/A | Last layer | Graded scale transformation with sigmoid activation
[Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816) | Classification | ResNet-50, ResNet-101, Xception, VGG19, Inception v3 | Keras (Tensorflow) | Yes | N/A | Last layer | N/A
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | Classification | VGG16 | Keras (Tensorflow) | ImageNet | None, Last three | Last layer | Dense with sigmoid activation
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659) | Localization and Classification | SSD (Single Shot MultiBox Detector) | Caffe | N/A | All | - | -
[Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663) | Localization | YOLOv3, RetinaNet | N/A | ImageNet | N/A | N/A | N/A
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | Localization | YOLOv2 | N/A | N/A | N/A | N/A | N/A
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) | Classification | ResNet-152, Inception-ResNet-v2 | PyTorch | ImageNet | All | N/A | N/A
[Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927) | Detection | AlexNet | Caffe | ImageNet | N/A | N/A | N/A
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | Localization | EfficientNet B4, RetinaNet | N/A | No | - | N/A | N/A
[Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4) | Localization | YOLOv3 | MXNet | PASCAL VOC 2007 and 2012 | All | - | FCL

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
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf) | Detection | Y-Net | The frame-work consists of two fully convolution encoder networks which are connected to a single decoder network that matches the encoder network resolution at each down-sampling operation. The network are trained with encoder specific adaptive learning rates that update the parameters of randomly initialized encoder network with a larger step size as compared to the encoder with pre-trained weights. The two encoders features are merged with a decoder network at each down-sampling paththrough sum-skip connection.
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Classification | ResNet | Network with 5 convolutional layers and 2 fully connected layers but based on a pre-trained ResNet CNN backbone.
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | Localization | None | Framework for false positive (FP) reduction is proposed.<br/>The framework adds a FP reduction unit to an RPN network. This unit exploits temporal dependencies between frames (forward and backward) to correct the output.<br/>Faster R-CNN and SSD RPNs were tested.
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | Localization | R-CNN with AlexNet | Several modifications done to AlexNet:<br/>- Last fully connected layer replaced to output two classes.<br/>- 5 convolutional and 3 fully connected layers were fine-tuned.<br/>- Max-Pooling kernels, ReLU activation function and dropout used to avoid overfitting and build robustness to intra-class deformations.<br/>- Stochastic gradient descent with momentum used as the optimization algorithm.
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | Localization | SSD | SSD was modified to add three new pooling layers (Second-Max Pooling, Second-Min Pooling and Min-Pooling) and a new deconvolution layer whose features are concatenated to those from the Max-Pooling layer that are fed into the detection layer.<br/> Model was pre-trained on the ILSVRC CLS-LOC dataset.
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | Classification | CapsNet | A convolutional layer followed by 7 convolutional capsule layers and finalized with a global average pool by capsule type.
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | Localization | Mask R-CNN | The region proposal network (RPN) uses a [Feature Pyramid Network](https://doi.org/10.1109/CVPR.2017.106) with a ResNet backbone. ResNet-50 and ResNet-101 were used, improved by extracting features from 5 different levels of layers. ResNet networks were initialized with COCO and ImageNet. Additionally, 76 random balloon images from Flickr were used to fine-tune networks initialized with COCO.<br/>The regions proposed by the RPN were filtered before the ROIAlign layer.<br/>The ROIAlign layer is followed by a pixel probability mask network, comprised of 4 convolutional layers followed by a transposed convolutional layer and a final convolutional layer with a sigmoid activation function that generates the final output. All convolutional layers except final are built with ReLU activation function.
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | Classification | None | The model is composed by four convolutional layers, each one of them followed by a max pooling layer. After that, the model has a dropout layer to reduce overfitting and then add a final dense layer with sigmoid activation that outputs the probability of the current polyp being malignant. The model was trained using the RMSprop optimizer with a learning rate of 1×10<sup>−4</sup>.
[Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827) | Localization | ResNet-50, Feature Pyramid Network, and Faster R-CNN | Authors propose a two-stage framework, where the polyp proposal stage (stage I) is constructed as a region-level polyp detector that is capable of guiding the pixel-level learning in the polyp segmentation stage (stage II), aiming to accurately segment the area the polyp occupies in the image. This framework has a backbone network composed by a ResNet-50 followed by a Feature Pyramid Network, producing a set of feature maps that are used by the two-stage framework. The polyp proposal stage was created as as an extension of faster R-CNN, which performs as a region-level polyp detector to recognize the lesion area as a whole. Then, the polyp segmentation stage is built in a fully convolutional fashion for pixelwise segmentation. This two-stage framework has a feature sharing strategy in which the learned semantics of polyp proposals of stage I are transferred to the segmentation task of stage II.
[Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897) | Localization | Resnet34 and MDeNet | Authors propose a modified version of MDeNet, proposed them in [Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434). See section *2.3. F-CNN models for polyp detection* of [Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897) for more details.
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503) | Localization | YOLOv3 | Authors present a framework based on YOLOv3 to improve detection. This frameworks adds: (i) a False Positive Relearning Module (FPRM) to make the detector network learning more about the features of FPs for higher precision; (ii) an Image Style Transfer Module (ISTM) to enhance the features of polyps for higher sensitivity; (iii) an Inter-Frame Similarity Correlation unit (ISCU) to integrate spatiotemporal information, which is combined with the image detector network to improve performance in video detection in order to reduce FPs.
[Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519) | Localization | YOLOv4 | Authors propose several models based on YOLOv4. To create their "Proposed Model1 (Small)" they first replaced the whole structure with Cross Stage Partial Networks (CSPNet), then substitute the Mish activation function for the Leaky ReLu activation function and also substituted the Distance Intersection over Union (DIoU) loss for the Complete Intersection over Union (CIoU) loss.
[Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052) | Localization | Resnet101 and Domain adaptive Faster R-CNN | Authors propose a consolidated domain adaptive framework with a training free style transfer process, a hierarchical network, and a centre besiegement loss for accurate cross-domain polyp detection and localization.

## Data Augmentation Strategies

&nbsp; | Rotation | Flipping (Mirroring) | Shearing | Translation (Shifting) | Crop | Random brightness | Zooming | Scale | Gaussian smoothing | Saturation adjustment | Gaussian distortion | Blurring | Resize | Random contrast | Exposure adjustment |Color augmentations in HSV | Histogram equalization | Skew | Random erasing | Color distribution adjust | Clipping | Sharpening | Mosaic | Cutmix | Mix-up | Color jittering|Random image expansion
:---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---:| :---:| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---:| :---:| :---: | :---: | :---: | :---: | :---: | :---: 
Num. Studies |26|22|10|8|8|7|6|6|4|3|3|3|3|2|2|2|1|1|1|1|1|1|1|1|1|1|1
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | X |  |  | X | X |  |  | X |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | X |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | |  |  |  |  |  |  |  
[Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725) | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | X |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) |  | X |  |  | X |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020) |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) | X | X |  |  |  | X |  |  | X |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  
[Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | X | X | X |  |  | X | X |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | X | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf)  | X | X | X |  |  | X |  | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | X | X | X |  |  |  | X |  |  |  |  |  |  |  |  |  |  | |  |  |  |  |  |  |  |  |  
[Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521) | X | X | X | X |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | X | X |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | X |  |  |  |  |  |  |  |  | X |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | X | X | X |  |  |  |  | X | X |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645) | X | X |  | X |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | X |  |  |  | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816) | X | X | X |  |  | X | X |  |  | X | X |  |  |  |  |  |  | X | X |  |  |  |  |  |  |  |  
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | X | X | X | X |  | | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | X | X |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663) | X |  | X |  |  |  | X |  |  |  |  | X |  |  |  |  |  |  |  |  | X |  |  |  |  |  |  
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) |  |  |  |  |  | X |  |  |  |  |  | X |  | X |  |  |  |  |  |  |  | X |  |  |  |  |  
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) |  | X |  |  |  |   |  |  |  |  |  |   |  |   |  |  |  |  |  |  |  |   |  |  |  |  |  
[Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927) | X |  |  | X | X |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |   |  |  |  |  |  
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) | X | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |   |  |  |  |  |  
[Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897) | X | X |  |  |  |  | X |  |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503)  |  | X |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | X |
[Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519) | X | X | X | X | X | X |  | X |  | X |  | X |  |  | X | X |  |  |  |  |  | X | X | X |  |  |  
[Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052) | X | X | X |  |  | X | X |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  
[Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4) |  | X |  |  | X |  |  |  |  |  |  |  | X |  |  |  |  |  |  |  |  |  |  |  |  |  | X 

## Frameworks and Libraries

Framework/Library | # Studies | Used by
--- | --- | --- 
Tensorflow | 9 | [Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010), [Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf), [Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645), [Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576), [Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649), [Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429), [Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816), [Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501)
Caffe | 8 | [Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087), [Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004), [Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020), [Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3), [Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133), [Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659), [Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827), [Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927)
Keras | 6 | [Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037), [Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf), [Sornapudi et al. 2019](https://doi.org/10.3390/app9122404), [Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059), [Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816), [Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501), [Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503)
C3D | 2 | [Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003), [Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134)
PyTorch | 3 | [Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593), [Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519), [Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052)
MatConvNet (MATLAB) | 1 | [Ribeiro et al. 2016](http://dx.doi.org/10.1155/2016/6584725)
DarkNet | 1 | [Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519)
MXNet | 1 | [Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4)

# Performance

> **Note**: Some performance metrics are not directly reported in the papers, but were derived using raw data or confusion matrices provided by them.

## Polyp Detection and Localization

Performance metrics on public and private datasets of all polyp detection and localization studies. 

- Between parentheses it is specified the type of performance metric: f = frame-based, p = polyp-based, pa = patch, and pi = pixel-based.
- Between curly brackets it is specified the **training dataset**, where "P" stands for private.
- Between square brackets it is specified the **test dataset** used for computing the performance metric, where "P" stands for private.
- For instance, [{P}] means that development and test splits of the same private dataset have been used for training and testing respectively.
- Performances marked with an * are reported on training datasets.
- AP stands for Average Precision.

Study | Recall (sensitivity) | Precision (PPV) | Specificity | Others | Manually selected images?
--- | --- | --- | --- | --- | --- 
[Tajbakhsh et al. 2015](https://doi.org/10.1109/ISBI.2015.7163821) | 70% (f) \{[P]\} | 63% (f) \{[P]\} | 90% (f) \{[P]\} | F1: 0.66, F2: 0.68 (f) \{[P]\} | No
[Zhu R. et al. 2015](https://doi.org/10.1109/CISP.2015.7407907) | 79.44% (pa) \{[P]\} | N/A | 79.54% (pa) \{[P]\} | Acc: 79.53% (pa) \{[P]\} | Yes
[Park and Sargent 2016](https://doi.org/10.1117/12.2217148) | 86% (f) \{P\} * | - | 85% (f) \{P\} * | AUC: 0.86 (f) \{P\} * | Yes (on training)
[Yu et al. 2017](https://doi.org/10.1109/JBHI.2016.2637004) | 71% (f) \{[ASU-Mayo]\} | 88.1% (f) \{[ASU-Mayo]\} | N/A | F1: 0.786, F2: 0.739 (f) \{[ASU-Mayo]\} | No
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | 97.6% (f) \{[P]\} | 99.4% (f) \{[P]\} | N/A | F1: 0.98, F2: 0.98, AUC: 1.00 (f) \{[P]\} | Yes
[Yuan and Meng 2017](https://doi.org/10.1002/mp.12147) | 98% (f) \{P\} * | 97% (f) \{P\} * | 99% (f) \{P\} * | F1: 0.98, F2: 0.98 (f) [P] | Yes
[Brandao et al. 2018](https://doi.org/10.1142/S2424905X18400020)  | ~90% (f) \{CVC-ClinicDB + ASU-Mayo\} [ETIS-Larib]<br/>~90% (f) \{CVC-ClinicDB + ASU-Mayo\} [CVC-ColonDB] | ~73% (f) \{CVC-ClinicDB + ASU-Mayo\} [ETIS-Larib]<br/>~80% (f) \{CVC-ClinicDB + ASU-Mayo\} [CVC-ColonDB] | N/A | F1: ~0.81, F2: ~0.86 (f) \{CVC-ClinicDB + ASU-Mayo\} [ETIS-Larib]<br/>F1: ~0.85, F2: ~0.88 (f) \{CVC-ClinicDB + ASU-Mayo\} [CVC-ColonDB] | Yes
[Zhang R. et al. 2018](https://doi.org/10.1016/j.patcog.2018.05.026) | 71.6% (f) \{[ASU-Mayo]\} | 88.6% (f) \{[ASU-Mayo]\} | 97% (f) \{[ASU-Mayo]\} | F1: 0.792, F2: 0.744 (f) \{[ASU-Mayo]\} | No
[Misawa et al. 2018](https://doi.org/10.1053/j.gastro.2018.04.003) | 90% (f) \{[P]\}<br/>94% (p) \{[P]\} | 55.1% (f) \{[P]\}<br/>48% (p) \{[P]\} | 63.3% (f) \{[P]\}<br/>40% (p) \{[P]\} | F1: 0.68 (f) 0.63 (p), F2: 0.79 (f) 0.78 (p) \{[P]\}<br/>Acc: 76.5% (f) 60% (p) \{[P]\} | No
[Zheng Y. et al. 2018](https://doi.org/10.1109/EMBC.2018.8513337) | 74% (f) \{CVC-ClinicDB + CVC-ColonDB\} [ETIS-Larib] | 77.4% (f) \{CVC-ClinicDB + CVC-ColonDB\} [ETIS-Larib] | N/A | F1: 0.757, F2: 0.747 (f) \{CVC-ClinicDB + CVC-ColonDB\} [ETIS-Larib] | Yes
[Shin Y. et al. 2018](https://doi.org/10.1109/ACCESS.2018.2856402) | 80.3% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 84.2% (f) \{CVC-ClinicDB\} [ASU-Mayo]  <br/>  84.3% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | 86.5% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 82.7% (f) \{CVC-ClinicDB\} [ASU-Mayo] <br/> 89.7% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | N/A | F1: 0.833, F2: 0.815 (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> F1: 0.834, F2: 0.839 (f) \{CVC-ClinicDB\} [ASU-Mayo] <br/> F1: 0.869, F2: 0.853 (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | Yes (ETIS-Larib) <br/> No (ASU-Mayo, CVC-ClinicVideoDB)
[Urban et al. 2018](https://doi.org/10.1053/j.gastro.2018.06.037) | 93% (f) \{P1\} [P2] <br/> 100% (p) \{P1\} [P2] <br/> 93% (p) \{P1\} [P3] | 74% (f) \{P1\} [P2] <br/> 35% (p) \{P1\} [P2] <br/> 60% (p) \{P1\} [P3] | 93% (f) \{P1\} [P2] | F1: 0.82, F2: 0.88 (f) \{P1\} [P2] <br/> F1: 0.52, F2: 0.73 (p) \{P1\} [P2] <br/> F1: 0.73, F2: 0.84 (p) \{P1\} [P3] | No
[Wang et al. 2018](https://doi.org/10.1038/s41551-018-0301-3) | 88.24% (f) \{P\} [CVC-ClinicDB]<br/>94.38% (f) \{P\} [P (dataset A)]<br/>91.64% (f), 100% (p) \{P\} [P (dataset C)] | 93.13 (f) \{P\} [CVC-ClinicDB]<br/>81.85 (f) \{P\} [P (dataset A)] | 95.40% (f) \{[P]\} [P (dataset D)] | F1: 0.91, F2: 0.89 (f) \{P\} [CVC-ClinicDB]<br/>F1: 0.88, F2: 0.92, AUC: 0.984 (f) \{P\} [P (dataset A)] | Yes (dataset A, CVC-ClinicDB)<br/>No (dataset C/D)
[Mohammed et al. 2018](http://bmvc2018.org/contents/papers/0487.pdf) | 84.4% (f) \{[ASU-Mayo]\} | 87.4 % (f) \{[ASU-Mayo]\} | N/A  | F1: 0.859, F2: 0.85 (f) \{[ASU-Mayo]\} | No
[Qadir et al. 2019](https://doi.org/10.1109/JBHI.2019.2907434) | 81.51% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | 87.51% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | 84.26% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | F1: 0.844, F2: 0.83 (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | No
[Tian Y. et al. 2019](https://doi.org/10.1109/ISBI.2019.8759521) | 64.42% (f) \{P\} [ETIS-Larib] | 73.6% (f) \{P\} [ETIS-Larib] | - | F1: 0.687, F2: 0.66 (f) \{P\} [ETIS-Larib] | Yes
[Blanes-Vidal et al. 2019](https://doi.org/10.1080/0284186X.2019.1584404) | 97.1% (f) \{[P]\} | 91.4% (f) \{[P]\} | 93.3% (f) \{[P]\} | Acc: 96.4%, F1: 0.94, F2: 0.95 (f) \{[P]\} | N/A (not clear in the paper)
[Zhang X. et al. 2019](https://doi.org/10.1371/journal.pone.0214133) | 76.37% (f) \{[P]\} | 93.92% (f) \{[P]\} | N/A | F1: 0.84, F2: 0.79(f) \{[P]\} | Yes
[Misawa et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1134) | 86% (p) \{P1\} [P2] | N/A | 74% (f) \{P1\} [P2] | - | No
[Zhu X. et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1087) | 88.5% (f) \{P1\} [P2] | N/A | 96.4% (f) \{P1\} [P2] | - | No
[Ahmad et al. 2019](https://doi.org/10.1016/j.gie.2019.03.1135) | 91.6% (f) \{P\} [ETIS-Larib]<br/>84.5% (f) \{ETIS-Larib + P\} [P] | 75.3% (f) \{P\} [ETIS-Larib] | 92.5% (f) \{ETIS-Larib + P\} [P] | F1: 0.83, F2: 0.88 (f) \{P\} [ETIS-Larib] | Yes (ETIS-Larib)<br/>No (private)
[Sornapudi et al. 2019](https://doi.org/10.3390/app9122404) | 91.64% (f) \{CVC-ClinicDB\} [CVC-ColonDB] <br/> 78.12% (f) \{CVC-ClinicDB\} [CVC-PolypHD] <br/> 80.29% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 95.52% (f) \{[P]\} | 89.94% (f) \{CVC-ClinicDB\} [CVC-ColonDB] <br/> 83.33% (f) \{CVC-ClinicDB\} [CVC-PolypHD] <br/> 72.93% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 98.46% (f) \{[P]\} | N/A | F1: 0.9073, F2: 0.9127 (f) \{CVC-ClinicDB\} [CVC-ColonDB] <br/> F1: 0.8065, F2: 0.7911 (f) \{CVC-ClinicDB\} [CVC-PolypHD] <br/> F1: 0.7643, F2: 0.7870 (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> F1: 0.966, F2: 0.961 (f) \{[P]\} | Yes (CVC-ClinicDB, CVC-ColonDB, ETIS-Larib)<br/>No (WCE video)
[Wittenberg et al. 2019](https://doi.org/10.1515/cdbme-2019-0059) | 86% (f) \{P\} [CVC-ClinicDB] <br/> 83% (f) \{P\} [ETIS-Larib]<br/>93% (f) \{[P]\} | 80% (f) \{P\} [CVC-ClinicDB] <br/> 74% (f) \{P\} [ETIS-Larib] <br/> 86% (f) \{[P]\} | N/A | F1: 0.82, F2: 0.85 (f) \{P\} [CVC-ClinicDB] <br/> F1: 0.79, F2: 0.81 (f) \{P\} [ETIS-Larib] <br/> F1: 0.89, F2: 0.92 (f) \{[P]\} | Yes
[Yuan Y. et al. 2019](https://doi.org/10.1109/TASE.2019.2936645) | 90.21% (f) \{[P]\} | 74.51% (f) \{[P]\} | 94.07% (f) \{[P]\} | Accuracy: 93.19%, F1: 0.81, F2: 0.86 (f) \{[P]\} | Yes
[Ma Y. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896576) | 93.67% (f) \{[P]\} | N/A | 98.36% (f) \{[P]\} | Accuracy: 96.04%, AP: 94.92% (f) \{[P]\} | Yes
[Jia X. et al. 2020](https://doi.org/10.1109/TASE.2020.2964827) | 92.1% (f) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> 59.4% (pi) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> 81.7% (f) \{CVC-ClinicDB\} [ETIS-Larib] | 84.8% (f) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> 85.9% (pi) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> 63.9% (f) \{CVC-ClinicDB\} [ETIS-Larib] | - | F1: 0.883, F2: 0.905 (f) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> F1: 0.702, F2: 0.633, Jaccard: 74.7±20.5, Dice: 83.9±13.6 (pi) \{CVC-ColonDB\} [CVC-ClinicDB] <br/> F1: 0.717, F2: 0.774 (f) \{CVC-ClinicDB\} [ETIS-Larib] | Yes (CVC-ClinicDB, ETIS-Larib)
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659) | 92% (f) \{P1\} [P2] <br/> 90% (f) \{P1\} [P2: WL] <br/> 97% (f) \{P1\} [P2: NBI] <br/> 98% (p) \{P1\} [P2] | 86% (f) \{P1\} [P2] <br/> 83% (f) \{P1\} [P2: WL] <br/> 97% (f) \{P1\} [P2: NBI] | N/A | F1: 0.88, F2: 0.88 (f) \{P1\} [P2] <br/> F1: 0.86, F2: 0.84 (f) \{P1\} [P2: WL] <br/> F1: 0.97, F2: 0.97 (f) \{P1\} [P2: NBI] | Yes
[Ma Y. et al. 2020](https://doi.org/10.1109/ISBI45749.2020.9098663) | 92% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | 87.50% (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | N/A | F1: 0.897, F2: 0.911 (f) \{CVC-ClinicDB\} [CVC-ClinicVideoDB] | No
[Young Lee J. et al. 2020](https://doi.org/10.1038/s41598-020-65387-1) | 96.7% (f) \{[P]\} <br/> 90.2% (f) \{P\} [CVC-ClinicDB] | 97.4% (f) \{[P]\} <br/> 98.2% (f) \{P\} [CVC-ClinicDB] | N/A | F1: 0.97, F2: 0.97 (f) \{[P]\} <br/> F1: 0.94, F2: 0.96 (f) \{P\} [CVC-ClinicDB] | Yes (CVC-ClinicDB, private)
[Li T. et al. 2020](https://doi.org/10.1055/a-1229-3927) | 73% (f) \{[P]\} | 93% (f) \{[P]\} | 96% (f) \{[P]\} | NPV: 83%, Acc: 86%, AUC: 0.94 (f) \{[P]\} | Yes
[Podlasek J. et al. 2020](https://doi.org/10.1055/a-1388-6735) |  91.2% (f) \{P\} [CVC-ClinicDB] <br/> 88.2% (f) \{P\} [Hyper-Kvasir] <br/> 74.1% (f) \{P\} [CVC-ColonDB] <br/> 67.3% (f) \{P\} [ETIS-Larib] | 97.4% (f) \{P\} [CVC-ClinicDB] <br/> 97.5% (f) \{P\} [Hyper-Kvasir] <br/> 92.4% (f) \{P\} [CVC-ColonDB] <br/> 79% (f) \{P\} [ETIS-Larib] | N/A |  F1: 0.942, F2: 0.924 (f) \{P\} [CVC-ClinicDB] <br/> F1: 0.926, F2: 0.899 (f) \{P\} [Hyper-Kvasir] <br/> F1: 0.823, F2: 0.771 (f) \{P\} [CVC-ColonDB] <br/>  F1: 0.727, F2: 0.693 (f) \{P\} [ETIS-Larib] | Yes
[Qadir et al. 2021](https://doi.org/10.1016/j.media.2020.101897) | 86.54% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 91% (f) \{CVC-ClinicDB\} [CVC-ColonDB] | 86.12% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 88.35% (f) \{CVC-ClinicDB\} [CVC-ColonDB] | N/A | F1: 0.863, F2: 0.864 (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> F1: 0.896, F2: 0.904 (f) \{CVC-ClinicDB\} [CVC-ColonDB] | Yes
[Xu J. et al. 2021](https://doi.org/10.1016/j.bspc.2021.102503) | 75.70% (f) \{CVC-ClinicDB + CVC-ColonDB + ETIS-Larib + CVC-ClinicVideoDB\} [P] <br/> 71.63% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 66.36% (f) [CVC-ClinicVideoDB] | 85.54% (f) \{CVC-ClinicDB + CVC-ColonDB + ETIS-Larib + CVC-ClinicVideoDB\} [P] <br/> 83.24% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 88.5% (f) [CVC-ClinicVideoDB] | N/A | F1: 0.799, F2: 0.773 (f) \{CVC-ClinicDB + CVC-ColonDB + ETIS-Larib + CVC-ClinicVideoDB\} [P] <br/> F1: 0.77, F2: 0.737 (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> F1: 0.7586, F2: 0.698 (f) [CVC-ClinicVideoDB] | Yes (ETIS-Larib, Private)<br/>No (CVC-ClinicVideoDB)
[Pacal et al. 2021](https://doi.org//10.1016/j.compbiomed.2021.104519) | 82.55% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 96.68% (f) \{CVC-ClinicDB\} [CVC-ColonDB] | 91.62% (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> 96.04% (f) \{CVC-ClinicDB\} [CVC-ColonDB] | N/A | F1: 0.868, F2: 0.842 (f) \{CVC-ClinicDB\} [ETIS-Larib] <br/> F1: 0.964, F2: 0.965 (f) \{CVC-ClinicDB\} [CVC-ColonDB] | Yes
[Liu et al. 2021](https://doi.org/10.1016/j.media.2021.102052) | 87.5% (f) \{CVC-ClinicDB\} [ETIS-Larib] | 77.8% (f) \{CVC-ClinicDB\} [ETIS-Larib] | - | F1: 0.824, F2: 0.854 (f) \{CVC-ClinicDB\} [ETIS-Larib] | Yes (ETIS-Larib)
[Nogueira-Rodríguez et al. 2021](https://doi.org/10.1007/s00521-021-06496-4) | 87% (f) \{[P]\} <br/> 89.91% (p) \{[P]\} | 89% (f) \{[P]\} | 54.97% (p) \{[P]\} | F1: 0.88 (f) \{[P]\} | Yes

## Polyp Classification

Performance metrics on public and private datasets of all polyp classification studies.

- Between square brackets it is specified the dataset used, where "P" stands for private.
- Performances marked with an * are reported on training datasets.

Study | Classes | Recall (sensitivity) | Specificity | PPV | NPV | Others | Polyp-level vs. frame-level | Dataset type
--- | --- | --- | --- | --- | --- | --- | --- | ---
[Zhang R. et al. 2017](https://doi.org/10.1109/JBHI.2016.2635662) | Adenoma vs. hyperplastic<br/>Resectable vs. non-resectable<br/>Adenoma vs. hyperplastic vs. serrated | 92% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.6% (adenoma vs. hyperplastic) [P] | 89.9% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>84.2% (adenoma vs. hyperplastic) [P] | 95.4% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.30% (adenoma vs. hyperplastic) [P] | 84.9% (resectable vs. non-resectable) [ColonoscopicDataset]<br/>87.2% (adenoma vs. hyperplastic) [P] | Acc: 91.3% (resectable vs. non- resectable) [ColonoscopicDataset]<br/>Acc: 86.7% (adenoma vs. serrated adenoma vs. hyperplastic) [ColonoscopicDataset]<br/>Acc: 85.9% (adenoma vs. hyperplastic) [P] | frame | video (manually selected images)
[Byrne et al. 2017](https://doi.org/10.1136/gutjnl-2017-314547) | Adenoma vs. hyperplastic | 98% [P] | 83% [P] | 90% [P] | 97% [P] | - | polyp | unaltered video
[Chen et al. 2018](https://doi.org/10.1053/j.gastro.2017.10.010) | Neoplastic vs. hyperplastic | 96.3% [P] | 78.1% [P] | 89.6% [P] | 91.5% [P] | N/A | frame | image dataset
[Lui et al. 2019](https://doi.org/10.1055/a-0849-9548) | Endoscopically curable lesions vs. endoscopically incurable lesions | 88.2% [P] | 77.9% [P] | 92.1% [P] | 69.3% [P] | Acc: 85.5% [P] | frame | image dataset
[Kandel et al. 2019](https://doi.org/10.1016/j.gie.2019.03.613) | Hyperplastic vs. serrated adenoma (near focus)<br/>Hyperplastic vs. adenoma (far focus) | 57.14% (hyperplastic vs. serrated) [P] <br/>75.63% (hyperplastic vs. adenoma) [P] | 68.52% (hyperplastic vs. serrated) [P] <br/>63.79% (hyperplastic vs. adenoma) [P] | N/A | N/A | Acc: 67.21% (hyperplastic vs. serrated) [P] <br/>Acc: 72.48% (hyperplastic vs. adenoma) [P] | frame | image dataset
[Zachariah et al. 2019](https://doi.org/10.14309/ajg.0000000000000429) | Adenoma vs. serrated | 95.7% [P] * | 89.9% [P] * | 94.1% [P] * | 92.6% [P] * | Acc: 93.6%, F1: 0.948, F2: 0.953 [P] * | polyp | image dataset
[Bour et al. 2019](https://doi.org/10.1109/ISSPIT47144.2019.9001816) | Not dangerous vs. dangerous vs. cancer | 88% (Cancer vs. others) [P] <br/> 84% (Not dangerous vs. others) [P] <br/> 90% (Dangerous vs. others) [P] | 94% (Cancer vs. others) [P] <br/> 93% (Not dangerous vs. others) [P] <br/> 93% (Dangerous vs. others) | 88% (Cancer vs. others) [P] <br/> 87% (Not dangerous vs. others) [P] <br/> 86% (Dangerous vs. others) | N/A | Acc: 87.1% [P] <br/> F1: 0.88 (Cancer vs. others) [P] <br/> F1: 0.86 (Not dangerous vs. others) [P] <br/> F1: 0.88 (Dangerous vs. others) | frame | image dataset
[Patino-Barrientos et al. 2020](https://doi.org/10.3390/app10020501) | Malignant vs. non-malignant | 86% [P] | N/A | 81% [P] | N/A | Acc: 83% [P] <br/>F1: 0.83 [P] | frame | image dataset
[Cheng Tao Pu et al. 2020](https://doi.org/10.1016/j.gie.2020.02.042) | 5-class (I, II, IIo, IIIa, IIIb)<br/><br/> Adenoma (classes II + IIo + IIIa) vs. hyperplastic (class I) | 97% (adenoma vs. hyperplastic) [P: AU] <br/> 100% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 100% (adenoma vs. hyperplastic) [P: JP-BLI] | 51% (adenoma vs. hyperplastic) [P: AU] <br/> 0% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 0% (adenoma vs. hyperplastic) [P: JP-BLI] | 95% (adenoma vs. hyperplastic) [P: AU] <br/> 82.4% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> 77.5% (adenoma vs. hyperplastic) [P: JP-BLI] | 63.5% (adenoma vs. hyperplastic) [P: AU] <br/> - (adenoma vs. hyperplastic) [P: JP-NBI] <br/> - (adenoma vs. hyperplastic) [P: JP-BLI] | AUC (5-class): 94.3% [P: AU] <br/> AUC (5-class): 84.5% [P: JP-NBI] <br/>AUC (5-class): 90.3% [P: JP-BLI] <br/><br/>Acc: 72.3% (5-class) [P: AU] <br/> Acc: 59.8% (5-class) [P: JP-NBI] <br/> Acc: 53.1% (5-class) [P: JP-BLI] <br/><br/> Acc: 92.7% (adenoma vs. hyperplastic) [P: AU] <br/> Acc: 82.4% (adenoma vs. hyperplastic) [P: JP-NBI] <br/> Acc: 77.5% (adenoma vs. hyperplastic) [P: JP-BLI] | frame | image dataset
[Ozawa. et al. 2020](https://doi.org/10.1177/1756284820910659) | Adenoma vs. hyperplastic vs. SSAP vs. cancer vs. other types | 97% (adenoma vs. other classes) [P: WL] <br/> 90% (adenoma vs. hyperplastic) [P: WL] <br/><br/> 97% (adenoma vs. other classes) [P: NBI] <br/> 86% (adenoma vs. hyperplastic) [P: NBI] | <br/> 81% (adenoma vs. hyperplastic) [P: WL] <br/><br/> 88% (adenoma vs. hyperplastic) [P: NBI] | 86% (adenoma vs. other classes) [P: WL] <br/> 98% (adenoma vs. hyperplastic) [P: WL] <br/><br/> 83% (adenoma vs. other classes) [P: NBI] <br/> 98% (adenoma vs. hyperplastic) [P: NBI] | 85% (adenoma vs. other classes) [P: WL] <br/> 48% (adenoma vs. hyperplastic) [P: WL] <br/><br/> 91% (adenoma vs. other classes) [P: NBI] <br/> 54% (adenoma vs. hyperplastic) [P: NBI] | Acc: 83% (5-class) [P: WL] <br/> F1: 0.91, F1: 0.88 (adenoma vs. other classes) [P: WL] <br/> F1: 0.94, F2: 0.96 (adenoma vs. hyperplastic) [P: WL] <br/><br/>  Acc: 81% (5-class) [P: NBI] <br/> F1: 0.89, F2: 0.85 (adenoma vs. other classes) [P NBI] <br/> F1: 0.92, F2: 0.95 (adenoma vs. hyperplastic) [P: NBI] | frame | image dataset
[Young Joo Yang et al. 2020](https://doi.org/10.3390/jcm9051593) | 7-class (CRC T1 vs. CRC T2 vs. CRC T3 vs. CRC T4 vs. high-grade dysplasia (HGD) vs. tubular adenoma with or without low grade dysplasia (TA) vs. non-neoplastic lesions) <br/><br/> 4-class (advanced CRC (T2, T3, and T4) vs. early CRC/HGD (CRC T1 and HGD) vs. TA vs. non-neoplastic lesions) <br/><br/> Advanced colorectal lesions vs. non-advanced colorectal lesions <br/><br/> Neoplastic lesions vs. non-neoplastic lesions | 94.1% (Neoplastic vs. non-neoplastic) [P: test] <br/> 83.2% (Advanced vs. non-advanced) [P: test] | 34.1% (Neoplastic vs. non-neoplastic) [P: test] <br/> 89.7% (Advanced vs. non-advanced) [P: test] | 86.1% (Neoplastic vs. non-neoplastic) [P: test] <br/> 84.5% (Advanced vs. non-advanced) [P: test] | 65% (Neoplastic vs. non-neoplastic) [P: test] <br/> 88.7% (Advanced vs. non-advanced) [P: test] | Acc: 0.795, F1: 0.899, F2: 0.923, AUC: 0.832 (Neoplastic vs. non-neoplastic) [P: test] <br/> Acc: 93.5%, F1: 0.838, F2: 0.934, AUC: 0.935 (Advanced vs. non-advanced) [P: test] <br/><br/> Acc: 71.5%, AUC: 0.760 (Neoplastic vs. non-neoplastic) [P: external] <br/> Acc: 87.1%, AUC: 0.935 (Advanced vs. non-advanced) [P: external] <br/><br/> Acc (7-class): 60.2% [P: test] 74.7% [P: external] <br/> Acc (4-class): 67.7% [P: test] 76% [P: external] | frame | image dataset

## Simultaneous Polyp Detection and Classification

Performance metrics on public and private datasets of all simultaneous polyp detection and classification studies.

- Between square brackets it is specified the dataset used, where "P" stands for private.
- AP<sub>IoU</sub> stands for Average Precision and mAP<sub>IoU</sub> for Mean Average Precision (i.e. the mean of each class AP), calculated at the specified IoU (Intersection over Union) level.

Study | Classes | AP | mAP | Manually selected images?
--- | --- | --- | --- | ---
[Liu X. et al. 2019](https://doi.org/10.1109/ISNE.2019.8896649) | Polyp vs. adenoma | Polyp: AP<sub>0.5</sub> =  83.39% [P]<br/>  Adenoma: AP<sub>0.5</sub> =  97.90% [P] | mAP<sub>0.5</sub> = 90.645% [P] | Yes

# List of Acronyms and Abbreviations

- AP: Average Precision.
- BLI: Blue Light Imaging.
- mAP: Mean Average Precision.
- NBI: Narrow Band Imaging.
- SSAP: Sesile Serrated Adenoma/Polyp.
- WCE: Wireless Capsule Endoscopy.
- WL: White Light.

# References and Further Reading

- [Object Detection Metrics](https://github.com/rafaelpadilla/Object-Detection-Metrics).
- [Evaluation metrics for object detection and segmentation: mAP](https://kharshit.github.io/blog/2019/09/20/evaluation-metrics-for-object-detection-and-segmentation).
- [A survey on Image Data Augmentation for Deep Learning](https://doi.org/10.1186/s40537-019-0197-0).

## Reviews

- Jun Ki Min, Min Seob Kwak, and Jae Myung Cha. [Overview of Deep Learning in Gastrointestinal Endoscopy](https://dx.doi.org/10.5009%2Fgnl18384). Gut Liver. 2019 Jul; 13(4): 388–393.
- Samy A Azer. [Challenges Facing the Detection of Colonic Polyps: What Can Deep Learning Do?](https://dx.doi.org/10.3390%2Fmedicina55080473). Medicina (Kaunas). 2019 Aug; 55(8): 473. 
- Wei-Lun Chao, Hanisha Manickavasagan, and Somashekar G. Krishna. [Application of Artificial Intelligence in the Detection and Differentiation of Colon Polyps: A Technical Review for Physicians](https://dx.doi.org/10.3390%2Fdiagnostics9030099). Diagnostics (Basel). 2019 Sep; 9(3): 99.
- Thomas KL. Lui, Chuan-Guo Guo, and Wai K. Leung. [Accuracy of Artificial Intelligence on Histology Prediction and Detection of Colorectal Polyps: a Systematic Review and Meta-Analysis](https://doi.org/10.1016/j.gie.2020.02.033). Gastrointest Endosc. 2020 Feb 28.
- Cristina Sánchez-Montes, Jorge Bernal, Ana García-Rodríguez, Henry Córdova, and Gloria Fernández-Esparrach. [Review of computational methods for the detection and classification of polyps in colonoscopy imaging](https://doi.org/10.1016/j.gastre.2019.11.003). Gastroenterol Hepatol. 2020 Apr; 43(4): 222-232.
- Luisa F.Sánchez-Peralta, Luis Bote-Curiel, Artzai Picón, Francisco M.Sánchez-Margallo, J. Blas Pagador. [Deep learning to find colorectal polyps in colonoscopy: A systematic literature review](https://doi.org/10.1016/j.artmed.2020.101923). Artificial Intelligence in Medicine. 2020 Aug; 108: 101923.
- Munish Ashat, Jagpal Singh Klair, Dhruv Singh, Arvind Rangarajan Murali, Rajesh Krishnamoorthi. [Impact of real-time use of artificial intelligence in improving adenoma detection during colonoscopy: A systematic review and meta-analysis](https://doi.org/10.1055/a-1341-0457). Endoscopy International Open. 2021 March; 09(04): E513-E521.
- Alexander Hann, Joel Troya, and Daniel Fitting. [Current status and limitations of artificial intelligence in colonoscopy](https://doi.org/10.1002/ueg2.12108). United European Gastroenteroly. 2021 Jun; 1-7.

## Randomized Clinical Trials

Study | Title | Date | Number of patients
--- | --- | --- | --- 
[Wang et al. 2019](https://doi.org/10.1136/gutjnl-2018-317500) | Real-time automatic detection system increases colonoscopic polyp and adenoma detection rates: a prospective randomised controlled study | Sep. 2019 | 1058
[Gong et al. 2020](https://doi.org/10.1016/s2468-1253%2819%2930413-3) | Detection of colorectal adenomas with a real-time computer-aided system (ENDOANGEL): a randomised controlled study | Jan. 2020 |  704
[Wang et al. 2020](https://doi.org/10.1016/S2468-1253%2819%2930411-X) | Effect of a deep-learning computer-aided detection system on adenoma detection during colonoscopy (CADe-DB trial): a double-blind randomised study | Jan. 2020 |  1010
[Liu et al. 2020](https://doi.org/10.4103/sjg.SJG_377_19) | Study on detection rate of polyps and adenomas in artificial-intelligence-aided colonoscopy | Feb. 2020 |  1026
[Su et al. 2019](https://doi.org/10.1016/j.gie.2019.08.026) | Impact of a real-time automatic quality control system on colorectal polyp and adenoma detection: a prospective randomized controlled study (with videos) | Feb. 2020 | 659
[Repici et al. 2020](https://doi.org/10.1053/j.gastro.2020.04.062) | Efficacy of Real-Time Computer-Aided Detection of Colorectal Neoplasia in a Randomized Trial | Aug. 2020 | 685 
