# TVPReid-Dataset
TVPReid Dataset for our arvix paper [TVPR:Text-to-Video Person Retrieval and a New
Benchmark](https://arxiv.org/pdf/2307.07184.pdf) [1].

![Dataset](highword.png)

## Introduction
To fill the limitation in the dataset, we build a large-scale benchmark for text-to-video person retrieval, termed as Textto-Video Person Re-identification (TVPReid) dataset. Our
dataset comprises 6559 person videos collected from three existing person re-identification datasets: PRID-2011 [2], iLIDS-VID [3], and DukeMTMC-VideoReID [4]. For PRID-2011, there are 1134 person videos with 2268 descriptions. iLIDS-VID consists of 600 person videos with
1200 descriptions. DukeMTMC-VideoReID has 4825 videos with 9650 descriptions. Since the data in these datasets are all video tracklets, we use OpenCV to synthesize the video tracklets of the same pedestrian under the same camera perspective at the same time into a video. After removing similar samples, we obtain 6559 unique person videos. To accurately describe
these videos, each video is annotated with two different sentence descriptions, totaling 13118 sentences that provide rich details about the person’s appearance, actions, and interactions with environment. The sentence descriptions are generally long and use a diverse vocabulary, with 404,580 words and 1982 unique words in our dataset. The average sentence
length in TVPReid dataset is 30 words, with the longest sentence containing 83 words. The figure illustrates some example thumbnails of person video and high-frequency words in the proposed TVPRrid dataset.

## Dataset Access

### Google Drive
Link:   [https://drive.google.com/drive/folders/1svo07n548Hb18m9bVgpS62s4AaM36f3C?usp=drive_link](https://drive.google.com/drive/folders/1svo07n548Hb18m9bVgpS62s4AaM36f3C?usp=drive_link)

### Baidu Netdisk
Link:   [https://pan.baidu.com/s/12cy0o2AN7XCwfbqDhiAL3w?pwd=tvpr](https://pan.baidu.com/s/12cy0o2AN7XCwfbqDhiAL3w?pwd=tvpr)

Password:tvpr

## Reference
[1] Ni F, Zhang X, Wu J, et al. TVPR: Text-to-Video Person Retrieval and a New Benchmark[J]. arXiv preprint arXiv:2307.07184, 2023.

[2] Hirzer M, Beleznai C, Roth P M, et al. Person re-identification by descriptive and discriminative classification[C]//Image Analysis: 17th Scandinavian Conference, SCIA 2011, Ystad, Sweden, May 2011. Proceedings 17. Springer Berlin Heidelberg, 2011: 91-102.

[3] Wang T, Gong S, Zhu X, et al. Person re-identification by video ranking[C]//Computer Vision–ECCV 2014: 13th European Conference, Zurich, Switzerland, September 6-12, 2014, Proceedings, Part IV 13. Springer International Publishing, 2014: 688-703.

[4] Wu Y, Lin Y, Dong X, et al. Exploit the unknown gradually: One-shot video-based person re-identification by stepwise learning[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2018: 5177-5186.
