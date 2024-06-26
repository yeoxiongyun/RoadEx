# RoadEx
Extraction of Road Networks from Aerial Images with Reinforcement Learning

**Project Description**


Road network extraction from aerial images is a challenging task that requires significant effort and time when performed manually. Most current approaches apply a post-processing step that vectorizes road segmentation predicted by a CNN, but this results in connectivity issues in road graphs due to segmentation errors. In this project, we will explore another approach that models the process of a reinforcement learning agent iteratively constructing the road graph directly from visual inputs.


## Introduction


## Data


#### Kaggle DeepGlobe Road Extraction Dataset

The DeepGlobe Road Extraction Dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset). The Kaggle dataset includes only the training data from the DeepGlobe Challenge (collected by DigitalGlobe's satellite). This data subset is procured from [Road Extraction Track](https://competitions.codalab.org/competitions/18467) in the [DeepGlobe Challenge 2018](http://deepglobe.org/challenge.html). The dataset is governed by [The DigitalGlobe's Internal Use License Agreement](http://deepglobe.org/docs/CVPR_InternalUseLicenseAgreement_07-11-18.pdf) and [Annotation License Agreement](http://deepglobe.org/docs/Annotation%20License%20Agreement.pdf).


* **Mask Labeling**: White pixels ≡ road, Black pixels ≡ background
* **Mask Binarization Threshol**d: Binarize masks values at 128

**Note**: The labels are not perfect, especially in rural areas.

| Image Attributes   | Images                      | Masks                 | Graphs                |
|-------------------|------------------------------|-----------------------|-----------------------|
| Type              | RGB                          | Grayscale             | -                     |
| Number            | 6226                         | 6226                  | -                     |
| Filename          | '_sat.jpg'                   | '_mask.png'           | -                     |
| Dimensions        | 1024 x 1024                  | 1024 x 1024           | -                     |
| Pixel Resolution  | 50cm                         | 50                    | -                     |


#### MUNO21: A Dataset for Map Update using Aerial Images
[MUNO21 Dataset](https://favyen.com/muno21/) includes imagery and road network data from 21 cities in the US: Atlanta, Austin, Baltimore, Boston, Chicago, Dallas, DC, Denver, Detroit, Houston, Los Angeles, Miami, New Orleans, New York, Philadelphia, Phoenix, Pittsburgh, San Antonio, Seattle, San Francisco, and Las Vegas

| Image Attributes   | Images                      | Masks                 | Graphs                |
|-------------------|------------------------------|-----------------------|-----------------------|
| Type              | RGB                          | -                     | JSON/ OSM             |
| Number            | 157                          | -                     | -                     |
| Filename          | '.jpg'                       | -                     | '.graph'              |
| Dimensions        | 11133 × 13384                | -                     | -                     |
| Pixel Resolution  | 100cm                        | -                     | -                     |

#### Cityscale Dataset
[Cityscale Dataset](https://drive.google.com/drive/folders/1uABt127ehNBQyfCnv6OND841ZrUlhmNB)

| Image Attributes   | Images                      | Masks                 | Graphs                |
|-------------------|------------------------------|-----------------------|-----------------------|
| Type              | RGB                          | RGB/ Grayscale        | Pickle/ JSON          |
| Number            | -                            | -                     | -                     |
| Filename          | '.png'                       | '.png'                | '.p'                  |
| Dimensions        | 2048 × 2048                  | 2048 × 2048           | -                     |
| Pixel Resolution  | 10cm                         | -                     | -                     |

#### Sat2Graph Dataset
[Sat2Graph SpaceNet3 Dataset](https://drive.google.com/drive/folders/1uABt127ehNBQyfCnv6OND841ZrUlhmNB)

| Image Attributes   | Images                      | Masks                 | Graphs                |
|-------------------|------------------------------|-----------------------|-----------------------|
| Type              | RGB                          | Grayscale             | Pickle                |
| Number            | -                            | -                     | -                     |
| Filename          | '.png'                       | '.png'                | 'gt_graph.p'          |
| Dimensions        | 400 × 400                    | 400 × 400             | -                     |
| Pixel Resolution  | 30cm                         | -                     | -                     |

[Google Drive](https://drive.google.com/drive/folders/1uABt127ehNBQyfCnv6OND841ZrUlhmNB)

## Methodology
<img width="500" alt="Screenshot 2024-06-26 at 6 38 07 PM" src="https://github.com/yeoxiongyun/RoadEx/assets/84406436/fda547bb-6f0f-4a8f-8f2e-3821b56b7db1">


## Evaluation
<img width="500" alt="Screenshot 2024-06-26 at 6 38 11 PM" src="https://github.com/yeoxiongyun/RoadEx/assets/84406436/648011a8-809e-44e8-a807-3f685537e063">

<img width="500" alt="Screenshot 2024-06-26 at 6 38 14 PM" src="https://github.com/yeoxiongyun/RoadEx/assets/84406436/c7cf7d5a-f043-451e-a9a8-617f7b9a23e0">


Detailed examples of the metrics can be found in the [evaluation metrics](https://github.com/yeoxiongyun/RoadEx/blob/main/src/evaluation_metrics.ipynb) Jupyter Notebook.



## License
Not allowed for commercial purposes. Only for academic research.

