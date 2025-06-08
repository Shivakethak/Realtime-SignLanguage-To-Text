


---

# Sign Language to Text Converter

This repository contains the files for my project **Sign Language to Text**.

---

## Project Description

A simple project to convert hand signs (sign language) into text using computer vision and a trained model. The project involves collecting your own dataset, training a model, and running real-time predictions using your webcam.

---

## Dataset Collection

You can create your own dataset of hand signs.

### Steps:

1. Run the file: `Datacollection.py`.

2. Before running:

   * Create a folder structure to store the images, for example:

     ```
     Data/
     ├── A/
     ├── B/
     ├── C/
     └── D/
     ```

   * In `Datacollection.py`, set the target folder:

     ```python
     folder = "Data/D"  # Example: for capturing images for 'D' sign
     ```

3. Now run the file:

   ```bash
   python Datacollection.py
   ```

4. Your webcam will open.

   * Show your hand in front of the camera.
   * Press the **'s'** key on your keyboard to capture pictures.
   * The pictures will be saved to the selected folder.

---

## Testing

To test the trained model:

1. Open `test.py`.

2. Update the following line with your saved model and labels:

   ```python
   classifier = Classifier(
       "C:/Users/shivakethak/PycharmProjects/PythonProject/.venv/HandSignDetection/Model/keras_model.h5",
       "C:/Users/shivakethak/PycharmProjects/PythonProject/.venv/HandSignDetection/Model/labels.txt"
   )
   ```

3. Run `test.py`:

   ```bash
   python test.py
   ```

4. The webcam will open.

   * You will see the **predicted sign** displayed above your hand in the video feed.

---

## Notes

* Ensure you have all required dependencies installed (OpenCV, TensorFlow, etc.).
* Adjust the model path and labels path as per your project structure.
* You can retrain the model with your own dataset for better accuracy.

---

## Optional Section: Requirements

```txt
opencv-python
tensorflow
numpy
```

---

