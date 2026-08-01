# Tomato Leaf Diseases Detection - Flask App

A Flask-based web application for detecting common tomato leaf diseases from uploaded images or videos using a YOLO model.

## Features

- Upload an image or video of tomato leaves
- Run real-time disease detection using YOLO
- Detects the following diseases:
  - Early blight
  - Late blight
  - Leaf Miner
  - Mosaic virus
  - Septoria
  - Spider mites
  - Yellow Leaf Curl Virus
- Preview detection results in the browser

## Demo

- Front page and upload flow

![Front Page](https://github.com/shafin201/FaskApp-Tomato-Leaf-Diseases-Detection/blob/main/project%20_ss/Picture1.png?raw=true)

- Detection result preview

![Detection Result](https://github.com/shafin201/FaskApp-Tomato-Leaf-Diseases-Detection/blob/main/project%20_ss/Picture2.png?raw=true)

## Prerequisites

- Python 3.8+
- `pip`
- `weights/best.pt` model file

## Installation

1. Clone the repository:

```bash
git clone https://github.com/shafin201/FaskApp-Tomato-Leaf-Diseases-Detection.git
cd flaskApp-tomato-leaf-diseases-detection
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

3. Install required Python packages:

```bash
pip install flask flask-wtf opencv-python ultralytics
```

## Running the App

1. Start the Flask application:

```bash
python flaskapp.py
```

2. Open your browser and go to:

```text
http://127.0.0.1:5000/
```

3. Navigate to `File Upload`, choose an image or video, and submit the form.

## Project Structure

- `flaskapp.py` - main Flask application and routes
- `YOLO_Detection.py` - detection logic using the Ultralytics YOLO model
- `templates/index.html` - home page template
- `templates/projectnew.html` - upload page and detection preview
- `static/files/` - upload destination for files
- `static/images/` - project UI images and assets
- `weights/best.pt` - trained YOLO model weights
- `weights/last.pt` - alternate model checkpoint

## Notes

- The app stores uploads in `static/files`
- The detection stream is served from `/detect`
- The current configuration uses `app.run(debug=True)`, which is suitable for development only

## Suggested Improvements

- Add a `requirements.txt`
- Add validation for supported file types
- Add graceful error handling for invalid uploads
- Add support for batch uploads or webcam input

## License

This project is provided as-is for demonstration and research purposes.
