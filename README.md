# ETH3D Two-View Evaluation Program #

This tool is used for evaluating two-view reconstruction methods in the [ETH3D benchmark](https://www.eth3d.net/).

Usage:

```
ETH3DTwoViewEvaluation \
    reconstruction.pfm \
    ground-truth.pfm \
    nocc-mask.png \
    [optional: visualization_directory \
               (create_training_visualizations ? true : false)]
```

If you use the dataset for research, please cite our paper:

T. Schöps, J. L. Schönberger, S. Galliani, T. Sattler, K. Schindler, M. Pollefeys, A. Geiger, "A Multi-View Stereo Benchmark with High-Resolution Images and Multi-Camera Videos", Conference on Computer Vision and Pattern Recognition (CVPR), 2017. \[[Bibtex](https://www.eth3d.net/data/schoeps2017cvpr.bib)\]\[[PDF](https://www.eth3d.net/data/schoeps2017cvpr.pdf)\]\[[Supplementary](https://www.eth3d.net/data/schoeps2017cvpr-supp.pdf)\]