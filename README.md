![image](https://github.com/user-attachments/assets/852fd61e-78a0-41a7-86b7-d70fac6c0995)# TVPReid-Dataset
TVPReid Dataset for our ACMMM2024 accepted paper [TVPR: Text-to-Video Person Retrieval and a New Benchmark](https://dl.acm.org/doi/10.1145/3664647.3681715) [[1]](#Reference)

![Dataset](./datasets-ciyun.png)

## Introduction
>***The currently published dataset is an optimized version of the dataset in the paper[1]. It is significantly different from the results in the original paper[1]. The latest experimental results on this dataset will be published in the >current project soon.***
To make up for the lack of experimental data for Text-to-Video Person Retrieval (TVPR) tasks, we construct a large-scale dataset and name it the Text-to-Video Person Re-identification (TVPReid) dataset. Our dataset consists of 6559 pedestrian videos from three existing person re-identification datasets: PRID-2011 [[2]](#Reference), iLIDS-VID [[3]](#Reference), and DukeMTMC-VideoReID [[4]](#Reference). These source data contain image data of different pedestrians from surveillance videos. We first aggregate them into the video form required by the task. For image data from the same pedestrian in the same time period and the same viewpoint, we use OpenCV to integrate them into a video. After integrating the three complete person re-identification datasets and performing data cleaning, we obtain a total of 6559 unique pedestrian videos. We then annotate each pedestrian video with two different sentence descriptions, for a total of 13118 sentences. The sentence descriptions are in a natural language style and contain rich details about the pedestrian's appearance, actions, and environmental elements that the pedestrian interacts with. The average sentence length of the TVPReid dataset is 30 words, and the longest sentence contains 83 words. The TVPReid dataset is divided into training set, validation set and test set with a ratio of 0.8125:0.0625:0.125, which is based on the division method of the MSRVTT [[5]](#Reference) dataset. The details of each sub-dataset are shown in the following table, among which TVPReid-PRID has 2268 sentence descriptions, TVPReid-iLIDs has 1200 sentence descriptions, and the largest sub-dataset TVPReid-Duke has 9650 sentence descriptions.
### Details for three sub-datasets in TVPReid dataset
|    |  TVPReid-PRID  |  TVPReid-iLIDs  |  TVPReid-Duke |
|:-------:|:-------:|:-------:|:-------:|
| Train | 921 | 488 | 3920 |
| Validate | 71 | 37 | 302 |
| Test | 142 | 75 | 603 |
| Total | 1134 | 600 | 4825 |


## Dataset Access

### Google Drive
Link: https://drive.google.com/drive/folders/1lmLik5zEPckDGrwakWcAM9XpQQ7Q8NmW?usp=sharing

### Baidu Netdisk
Link: https://pan.baidu.com/s/1cKOqq_RJb1zcT3DsJIqy1A?pwd=9jpd
Password: 9jpd

### Folder structure of the dataset
As shown in the structure below, `TVPReid_dataset` contains three sub-datasets. Taking `TVPReid-Duke/` as an example, the sub-dataset folder contains `captions/` and `videos/`. `captions/` contains the complete text description of the sub-dataset: `TVPReid-Duke.json`, and the partition files: `train.csv`, `test.csv`, `val.csv`, which store the video ID. The folder structure of `TVPReid-iLIDs/` and `TVPReid-PRID/` is consistent with that of `TVPReid-Duke/`.
```shell
TVPReid_dataset
├── TVPReid-Duke
│   ├── captions
│   │   ├── train.csv
│   │   ├── test.csv
│   │   ├── val.csv
│   │   └── TVPReid-Duke.json
│   └── videos
│       ├── person0001.mp4
│       ├── person0002.mp4
│       ...
│
├── TVPReid-iLIDs
│
└── TVPReid-PRID
```

## Note
Using this project will download third-party open source datasets. Please check the license terms of these open source dataset projects before use.

## Citation
If you find TVPReid dataset useful in your work, you can cite the following paper[[1]](#Reference):
```shell
@inproceedings{zhang2024tvpr,
  title={TVPR: Text-to-Video Person Retrieval and a New Benchmark},
  author={Zhang, Xu and Ni, Fan and Dong, Guan-Nan and Zhu, Aichun and Wu, Jianhui and Ni, Mingcheng and Liu, Hui},
  booktitle={Proceedings of the 32nd ACM International Conference on Multimedia},
  pages={10105--10113},
  year={2024}
}
```

## Reference
[1] Zhang X, Ni F, Dong G N, et al. TVPR: Text-to-Video Person Retrieval and a New Benchmark[C]//Proceedings of the 32nd ACM International Conference on Multimedia. 2024: 10105-10113.

[2] Hirzer M, Beleznai C, Roth P M, et al. Person re-identification by descriptive and discriminative classification[C]//Image Analysis: 17th Scandinavian Conference, SCIA 2011, Ystad, Sweden, May 2011. Proceedings 17. Springer Berlin Heidelberg, 2011: 91-102.

[3] Wang T, Gong S, Zhu X, et al. Person re-identification by video ranking[C]//Computer Vision–ECCV 2014: 13th European Conference, Zurich, Switzerland, September 6-12, 2014, Proceedings, Part IV 13. Springer International Publishing, 2014: 688-703.

[4] Wu Y, Lin Y, Dong X, et al. Exploit the unknown gradually: One-shot video-based person re-identification by stepwise learning[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2018: 5177-5186.

[5] Xu J, Mei T, Yao T, et al. Msr-vtt: A large video description dataset for bridging video and language[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2016: 5288-5296.
