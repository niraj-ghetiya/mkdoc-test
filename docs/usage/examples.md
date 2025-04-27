# Examples

Explore practical examples to learn how to use YOLO-ONNX.

## Demo Script
Run the demo script included in the repository:
```bash
python examples/demo.py
```
See [examples/demo.py](https://github.com/your-username/yolo-onnx/blob/main/examples/demo.py) for the source code.

## Jupyter Notebook
Check out the interactive notebook:
- [demo.ipynb](https://github.com/your-username/yolo-onnx/blob/main/examples/demo.ipynb)

## Custom Use Case
Create your own script:
```python
from yolo_onnx import YOLOONNX

model = YOLOONNX("yolo11n.onnx")
results = model.predict("custom_image.jpg")
results[0].save("custom_output.jpg")
```