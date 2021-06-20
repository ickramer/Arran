# Arran
Arran: a benchmark dataset for automated object detection of archaeological sites on LiDAR data

The benchmark dataset can be accessed through https://drive.google.com/drive/folders/1BMdKLO2vDC70PVjyR07x9esDFvESUB5Y?usp=sharing.

In this drive 6 folders containing datasets for the original DTM and 5 different visualisations. Each folder contains 2 csv files for train and validation annotations and an image folder. The visualisations were created using the Relief Visualization Toolbox (RVT) (available through https://iaps.zrc-sazu.si/en/rvt). The csv-files describe the path to the images, box coordinates and class names (path/to/image.jpg,x1,y1,x2,y2,class name). Each line contains only one box annotation.

The original LiDAR data can be downloaded through https://remotesensingdata.gov.scot/.

![fig-ch4-15_v1](https://user-images.githubusercontent.com/16646078/122689447-72af3600-d21a-11eb-81d5-b2e405865f43.png)
*These images show the image pre-processing step from the Fizyr implementation of RetinaNet: debugging object detection input images (Gaiser, 2019).*

# Results
| | Round House | Small Cairn | Shieling | MaP |
| --- | --- | --- |  --- | --- |
| Slope | **83%** | 23% | 51% | 50% |
| SVF | 79% | 18% | 36% | 44%|
| Hillshade |73% | 13% | 40% | 42%|
| Open-positive |78% | 22% | **53%** | **51%** |
| Local dominance |78% | **31%** | 15% | 41% |

*Our results using the Fizyr implementation of RetinaNet in Keras (Gaiser, 2019).* 
