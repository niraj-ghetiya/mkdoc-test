# Installation

Follow these steps to install YOLO-ONNX.

## Prerequisites
- Python 3.8 or higher
- pip

## Install via pip
```bash
pip install yolo-onnx

## Install from Source
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/yolo-onnx.git
   cd yolo-onnx
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Install the package:
   ```bash
   pip install -e .
   ```

## Verify Installation
```python
import yolo_onnx
print(yolo_onnx.__version__)  # Should print: 0.1.0
```
```

### docs/getting-started/quickstart.md
A quickstart guide to demonstrate basic usage.

```markdown
# Quickstart

Get started with YOLO-ONNX in just a few steps.

## Step 1: Install YOLO-ONNX
```bash
pip install yolo-onnx
```

## Step 2: Prepare a Model
Export a YOLO11 model to ONNX format using Ultralytics:
```bash
yolo export model=yolo11n.pt format=onnx
```

## Step 3: Run Inference
```python
from yolo_onnx import YOLOONNX

# Load model
model = YOLOONNX("yolo11n.onnx")

# Run inference
image_path = "image.jpg"
results = model.predict(image_path, conf=0.25, iou=0.7)

# Display results
results[0].show()
```

## Next Steps
- Explore advanced usage in [Running Inference](usage/inference.md).
- Check out [Examples](usage/examples.md) for more use cases.
```
