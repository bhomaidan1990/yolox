# Instance Segmentation

This repo is refactored from the [gdrnpp_bop2022](https://github.com/shanice-l/gdrnpp_bop2022) to include the generic instance segmentation module only.

This work combines [detectron2](https://github.com/facebookresearch/detectron2) with [Yolox](https://github.com/Megvii-BaseDetection/YOLOX) to do instance segmentation.

## Installation

```shell
## create venv
python3 -m venv any_venv
## activate venv
source any_venv/bin/activate
## install requirements
pip3 install -r requirements
```

## Training a Model

```shell
./det/yolox/tools/train_yolox.sh \
# GPUs you have, might be 0,1 etc.
0 \
# Path to the config file
configs/bop_pbr/your_config.py
```
> TODO: write a tutorial on how to write config file

## Testing a Model

```shell
./det/yolox/tools/test_yolox.sh \
# GPUs you have, might be 0,1 etc.
0 \
# Path to the config file
configs/bop_pbr/your_config.py \
./output/bop_pbr/yolox_x_640_augCozyAAEhsv_ranger_30_epochs_hb_pbr_hb_test_primesense_bop19/model_final.pth"
```