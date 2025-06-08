# DeepFake Generation and Detection

This project implements a DeepFake generation and detection system using deep learning. The generation module uses a Variational Autoencoder (VAE) to create synthetic face images, while the detection module uses a Convolutional Neural Network (CNN) to classify images as real or fake. A Flask-based web interface allows users to upload images for detection or generate DeepFakes.

## Features
- Generate synthetic face images using a VAE.
- Detect DeepFake images using a CNN classifier.
- Web interface for easy interaction.
- Modular design with separate scripts for generation and detection.

## Requirements
- Python 3.8+
- TensorFlow 2.5+
- Flask
- NumPy
- OpenCV
- Pillow
- See `requirements.txt` for a complete list.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/deepfake_project.git
   cd deepfake_project
   ```
2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Ensure the `models/` directory contains pretrained weights (`vae_encoder.h5`, `vae_decoder.h5`, `detector.h5`). Note: These are placeholders; train the models or download pretrained weights.

## Usage
1. Start the Flask application:
   ```bash
   python app.py
   ```
2. Open a browser and navigate to `http://localhost:5000`.
3. Use the web interface to:
   - Upload an image for DeepFake detection.
   - Generate a synthetic face image.
4. Alternatively, run scripts directly:
   - Generate DeepFake: `python generate_deepfake.py`
   - Detect DeepFake: `python detect_deepfake.py --image path/to/image.jpg`

## Project Structure
```
deepfake_project/
├── app.py                    # Flask web application
├── generate_deepfake.py      # DeepFake generation script
├── detect_deepfake.py        # DeepFake detection script
├── models/                   # Pretrained model weights
├── static/                   # Static files (CSS, uploads)
├── templates/                # HTML templates
├── requirements.txt          # Dependencies
├── README.md                 # This file
└── docs/                     # Detailed documentation
```

## Documentation
See `docs/documentation.md` for detailed information on the project, including model architectures, training, and deployment.

## Notes
- Pretrained model weights are not included due to size constraints. Train the models using provided scripts or download compatible weights.
- This is a simplified implementation for educational purposes. Real-world DeepFake systems require large datasets and complex models.
- Ensure ethical use of DeepFake technology.

## License
MIT License. See `LICENSE` file for details.
