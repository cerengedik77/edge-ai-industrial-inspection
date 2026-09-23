# Bottle Cap Defect Detection

Fine-tuned YOLO11n to detect bottle-cap condition from a public dataset.

Python · YOLO11 · Ultralytics · OpenCV

## Result

| Metric | Value |
|---|---|
| Precision | 82.6% |
| Recall | 82.9% |
| mAP50 | 81.6% |
| Inference | 13.8 ms on Tesla T4 |
| Model | YOLO11n, 5.2 MB |

## Pipeline

Image → YOLO11n → defect / good / loos-cap / no-cap / ring-missing

## Data

Public dataset: Roboflow Universe, bottle-cap-defect-2, version 8.
1435 training images, 107 validation images.
The images were not collected by me.

## Training

40 epochs, image size 640, batch 16, pretrained YOLO11n, Tesla T4.
Weights: models/bottle-cap-yolo11n.pt
