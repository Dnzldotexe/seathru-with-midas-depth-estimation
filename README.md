# HOW TO RUN
## Create and activate a python virual environment
```python
python -m venv venv
# source venv/bin/activate # If you're in Linux
# venv\Scripts\activate # If you're in Windows, use .bin if cmd, use .ps1 if powershell
```

## Install dependencies
```sh
pip install -r requirements.txt
```

## Arguments
```sh
# --input: Input image file or directory of images (required)
# --output: Output image file or directory (required)
# --depth-map: Input depth map (optional, overrides MiDaS)
# --midas-model: MiDaS model type: MiDaS_small, DPT_Large, DPT_Hybrid (default='DPT_Large')
# --f: f value (controls brightness) (default=2.0)
# --l: l value (controls balance of attenuation constants) (default=0.5)
# --p: p value (controls locality of illuminant map) (default=0.01)
# --min-depth: Minimum depth value to use in estimations (range 0-1) (default=0.1)
# --max-depth: Replacement depth percentile value for invalid depths (range 0-1) (default=1.0)
# --spread-data-fraction: Require data to be this fraction of depth range away from each other in attenuation estimations (default=0.01)
# --size: Maximum size of the image to process (default=512)
# --output-graphs: Output graphs (action='store_true')
# --monodepth-add-depth: Additive value for monodepth map (default=2.0)
# --monodepth-multiply-depth: Multiplicative value for monodepth map (default=10.0)
# --equalize-image: Histogram equalization for final output (action='store_true')
```

## Sample Usage
```sh
python seathru-with-midas-depth-estimation.py --input raw_images/ --output corrected_images/ --midas-model MiDaS_small --size 5568
```


# ATTRIBUTION
Authors and Contributors of Sea-thru:
- [github.com/hainh/sea-thru/](https://github.com/hainh/sea-thru/)
- [A Revised Underwater Image Formation Model](https://openaccess.thecvf.com/content_cvpr_2018/papers/Akkaynak_A_Revised_Underwater_CVPR_2018_paper.pdf)
- [Sea-thru: A Method For Removing Water From Underwater Images](https://openaccess.thecvf.com/content_CVPR_2019/papers/Akkaynak_Sea-Thru_A_Method_for_Removing_Water_From_Underwater_Images_CVPR_2019_paper.pdf)

Authors and Contributors of MiDaS:
- [github.com/isl-org/MiDaS](https://github.com/isl-org/MiDaS)
- [Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-shot Cross-dataset Transfer](https://arxiv.org/pdf/1907.01341)
- [MiDaS v3.1 – A Model Zoo for Robust Monocular Relative Depth Estimation](https://arxiv.org/pdf/2307.14460)


# LICENSE
MIT License
