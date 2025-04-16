# TVPReid-Dataset
TVPReid Dataset for our ACMMM2024 accepted paper [TVPR: Text-to-Video Person Retrieval and a New Benchmark](https://dl.acm.org/doi/10.1145/3664647.3681715)

![Dataset](./datasets-ciyun.png)

## Introduction
To make up for the lack of experimental data for Text-to-Video Person Retrieval (TVPR) tasks, we construct a large-scale dataset and name it the Text-to-Video Person Re-identification (TVPReid) dataset. Our dataset consists of 6559 pedestrian videos from three existing person re-identification datasets: PRID-2011 [[1]](#Reference), iLIDS-VID [[2]](#Reference), and DukeMTMC-VideoReID [[3]](#Reference). These source data contain image data of different pedestrians from surveillance videos. We first aggregate them into the video form required by the task. For image data from the same pedestrian in the same time period and the same viewpoint, we use OpenCV to integrate them into a video. After integrating the three complete person re-identification datasets and performing data cleaning, we obtain a total of 6559 unique pedestrian videos. We then annotate each pedestrian video with two different sentence descriptions, for a total of 13118 sentences. The sentence descriptions are in a natural language style and contain rich details about the pedestrian's appearance, actions, and environmental elements that the pedestrian interacts with. The average sentence length of the TVPReid dataset is 30 words, and the longest sentence contains 83 words. The TVPReid dataset is divided into training set, validation set and test set with a ratio of 0.8125:0.0625:0.125, which is based on the division method of the MSRVTT [[4]](#Reference) dataset. The details of each sub-dataset are shown in the following table, among which TVPReid-PRID has 2268 sentence descriptions, TVPReid-iLIDs has 1200 sentence descriptions, and the largest sub-dataset TVPReid-Duke has 9650 sentence descriptions.
### Details for three sub-datasets in TVPReid dataset
|    |  TVPReid-PRID  |  TVPReid-iLIDs  |  TVPReid@Duke |
|:-------:|:-------:|:-------:|:-------:|
| Train | 921 | 488 | 3920 |
| Validate | 71 | 37 | 302 |
| Test | 142 | 75 | 603 |
| Total | 1134 | 600 | 4825 |


## Dataset Access

### Google Drive
Link: https://drive.google.com/drive/folders/1lmLik5zEPckDGrwakWcAM9XpQQ7Q8NmW?usp=drive_link

### Baidu Netdisk
Link: https://pan.baidu.com/s/1SiaCgnEWlY98RNnhoCg0rg?pwd=5vmx 
Password: 5vmx

## Note
Using this project will download third-party open source datasets. Please check the license terms of these open source dataset projects before use.

## Reference
[1] Hirzer M, Beleznai C, Roth P M, et al. Person re-identification by descriptive and discriminative classification[C]//Image Analysis: 17th Scandinavian Conference, SCIA 2011, Ystad, Sweden, May 2011. Proceedings 17. Springer Berlin Heidelberg, 2011: 91-102.

[2] Wang T, Gong S, Zhu X, et al. Person re-identification by video ranking[C]//Computer Vision–ECCV 2014: 13th European Conference, Zurich, Switzerland, September 6-12, 2014, Proceedings, Part IV 13. Springer International Publishing, 2014: 688-703.

[3] Wu Y, Lin Y, Dong X, et al. Exploit the unknown gradually: One-shot video-based person re-identification by stepwise learning[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2018: 5177-5186.

[4] Xu J, Mei T, Yao T, et al. Msr-vtt: A large video description dataset for bridging video and language[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2016: 5288-5296.
