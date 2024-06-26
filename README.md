# RoadEx
Extraction of Road Networks from Aerial Images with Reinforcement Learning

**Project Description**


Road network extraction from aerial images is a challenging task that requires significant effort and time when performed manually. Most current approaches apply a post-processing step that vectorizes road segmentation predicted by a CNN, but this results in connectivity issues in road graphs with due to segmentation errors. In this project, we will explore another approach that models the process of a reinforcement learning agent iteratively constructing the road graph directly from visual inputs.


## Introduction


## Data


#### Kaggle DeepGlobe Road Extraction Dataset

The DeepGlobe Road Extraction Dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset). The Kaggle dataset includes only the training data from the DeepGlobe Challenge (collected by DigitalGlobe's satellite). This data subset is procured from [Road Extraction Track](https://competitions.codalab.org/competitions/18467) in the [DeepGlobe Challenge 2018](http://deepglobe.org/challenge.html). The dataset is governed by [The DigitalGlobe's Internal Use License Agreement](http://deepglobe.org/docs/CVPR_InternalUseLicenseAgreement_07-11-18.pdf) and [Annotation License Agreement](http://deepglobe.org/docs/Annotation%20License%20Agreement.pdf).


* **Mask Labeling**: White pixels ≡ road, Black pixels ≡ background
* **Mask Binarization Threshol**d: Binarize masks values at 128

**Note**: The labels are not perfect, especially in rural areas.

| Image Attributes   | Images                                   | Masks                                        |
|-------------------|-------------------------------------------|----------------------------------------------|
| Type              | RGB                                       | Grayscale                                    |
| Number            | 6226                                      | 6226                                         |
| Filename          | '_sat.jpg'                                | '_mask.png'                                  |
| Dimensions        | 1024 x 1024                               | 1024 x 1024                                  |
| Pixel Resolution  | 50cm                                      |                                              |

#### MUNO21: A Dataset for Map Update using Aerial Images
[MUNO21 Dataset](https://favyen.com/muno21/)

#### Cityscale Dataset (Google Drive)
[Cityscale Dataset](https://drive.google.com/drive/folders/1uABt127ehNBQyfCnv6OND841ZrUlhmNB)

#### Sat2Graph Dataset (Google Drive)
[Sat2Graph SpaceNet3 Dataset](https://drive.google.com/drive/folders/1uABt127ehNBQyfCnv6OND841ZrUlhmNB)

