## Overview
This project fine-tunes a YOLOv5 model for traffic sign detection using a custom dataset from Kaggle. Dataset: [Traffic Sign Detection Dataset (Kaggle)](https://www.kaggle.com/datasets/pkdarabi/cardetection)
The pipeline includes data preprocessing, model training, evaluation, and performance analysis.

## Model
This project uses the official YOLOv5 PyTorch implementation by Ultralytics.
- Base architecture: YOLOv5m
- Framework: PyTorch
- Transfer learning from COCO pretrained weights

## Training
The YOLOv5 model was fine-tuned on a custom traffic sign dataset using the following configuration:
- Image size: 415
- Batch size: 16
- Epochs: 20
- Pretrained weights: yolov5m.pt
- Dataset config: dataset.yaml

## Results
- Best model saved at: runs/train/exp/weights/best.pt
- Sample qualitative results shown below.

Training command:
```bash
python train.py \
  --img 415 \
  --batch 16 \
  --epochs 20 \
  --data dataset.yaml \
  --weights yolov5m.pt \
  --cache
