# Running Inference

Learn how to use YOLO-ONNX to run inference on images.

## Basic Inference
```python
from yolo_onnx import YOLOONNX

# Initialize model
model = YOLOONNX("yolo11n.onnx")

# Run inference
results = model.predict("image.jpg", conf=0.25, iou=0.7)

# Display results
results[0].show()
```

## Customizing Inference
- **Confidence Threshold**: Adjust `conf` to filter detections (e.g., `conf=0.5`).
- **IoU Threshold**: Set `iou` for non-maximum suppression (e.g., `iou=0.6`).
```python
results = model.predict("image.jpg", conf=0.5, iou=0.6)
```

## Saving Results
Save detection results to a file:
```python
results[0].save("output.jpg")
```