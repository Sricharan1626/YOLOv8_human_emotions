# YOLOv8_human_emotions
---

## To Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/Sricharan1626/YOLOv8_human_emotions.git
cd YOLOv8_human_emotions
```

---

## Install Requirements

First, make sure you have Python 3.8+ installed.  
To install all required packages, run:

```bash
pip install -r requirements.txt
```
---

## Download the Trained Model

The trained model file is named `my_model.pt`.  
If it's not already in the repo, you can download it (replace the URL with your actual download link if needed):

```bash
wget https://github.com/Sricharan1626/YOLOv8_human_emotions/my_model/my_model.pt
```

Or, if already downloded the repo, you don’t need to download.

---

## Using the Trained Model for Emotion Detection

Here’s an example script to use the model and detect emotions:

```python
from ultralytics import YOLO

# Load the trained model
model = YOLO('my_model.pt')

# Run inference on an image
results = model('your_image.jpg')
results.show()
```

Replace `'your_image.jpg'` with the path to your image.

---

## Training Graphs

All the graphs related to model training and evaluation can be found in the `my_model/train` directory.

---

## Training Your Own Model

The `data` folder contains labeled data for YOLOv8.  
To train your own model, run:

```bash
yolo task=detect mode=train model=yolov8n.pt data=data/data.yaml epochs=50 imgsz=640
```

- `model=yolov8n.pt` can be changed to any YOLOv8 variant.
- `data=data/data.yaml` points to your custom dataset config.
- `epochs=50` is the number of training epochs (adjust as needed).

---

## Additional Information

- The model (`my_model.pt`) is trained to detect human emotions, with a focus on girls' facial expressions.
- The `data` folder contains labeled images and a `data.yaml` file suitable for YOLOv8 training.
- You can use the provided model for inference or retrain using your own data.

---

If you need more help, check the official [Ultralytics YOLOv8 documentation](https://docs.ultralytics.com/).
