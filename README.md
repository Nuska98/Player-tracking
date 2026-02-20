Player Detection using YOLO

1. Introduction

This project focuses on detecting cricket players from video footage using a YOLO-based object detection model. Frames were extracted from a cricket video and manually annotated using LabelImg. The trained model was then used to detect players in video frames.

2. Dataset Description

Frames extracted from cricket video

Bounding boxes annotated using LabelImg

Classes used: Batsman, Bowler, Keeper, Fielder, Umpire

Dataset split into training and validation sets

3. Model Used

YOLOv8 (Ultralytics)

Trained for 20 epochs

Input: Annotated video frames

Output: Bounding box detection of players

4. Performance Metrics

Final training results (Epoch 20):

| Metric              | Value  |
| ------------------- | ------ |
| Precision           | 0.9415 |
| Recall              | 0.4629 |
| mAP@50              | 0.5636 |
| mAP@50–95           | 0.4696 |
| Train Box Loss      | 0.7905 |
| Validation Box Loss | 0.7823 |


5. Performance Analysis

Precision (94.15%)

High precision indicates that when the model predicts a player, it is usually correct. There are very few false positives.

Recall (46.29%)

Recall is moderate. This means the model misses some players in certain frames. Improvements can be made to increase recall.

mAP@50 (56.36%)

The model performs reasonably well at detecting players at IoU threshold 0.5.

Loss Curves

Both training and validation losses decrease over epochs, indicating stable learning without major overfitting.

6. Discussion
Strengths

High precision

Stable training behavior

Successful detection on video frames

Limitations

Moderate recall (missed detections)

Small dataset size

Limited class diversity (only player class)

Model may struggle with occlusion and fast movement

8. Conclusion

The YOLO-based model successfully detects cricket players from video frames. While precision is high, recall can be improved with a larger and more diverse dataset. The system demonstrates the feasibility of automated player detection in sports analytics.
