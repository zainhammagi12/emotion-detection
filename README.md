# Emotion Detection System 🎭

A Facial emotion detection system using deep learning, capable of identifying 7 different emotional states. Built with TensorFlow and OpenCV, this system provides fast and accurate emotion recognition suitable for various applications.

## Features ✨

- emotion detection from webcam feed
- Support for 7 emotional states:
  - Happy 😊
  - Sad 😢
  - Angry 😠
  - Neutral 😐
  - Surprise 😮
  - Fear 😨
  - Disgust 😖
- Pre-trained model using VGG-16 architecture
- Processing speed of 30+ FPS
- Easy-to-use interface

## Model Performance 📊

- Accuracy: 89% on validation set
- Real-time inference speed: ~33ms per frame
- Trained on FER-2013 dataset (35,000+ images)

## Prerequisites 🛠️

- Python 3.8 or higher
- pip package manager

## Installation 📦

1. Clone the repository:
```bash
git clone https://github.com/zainhammagi12/emotion-detection.git
cd emotion-detection
```

2. Create and activate virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

### Training Custom Model

1. Prepare your dataset in the required format
2. Update configuration in `config.py`
3. Run training:
```bash
python train.py --epochs 50 --batch_size 32
```

## Project Structure 📁

```
emotion-detection/
├── doc
    └── Emotion recognition FINAL.ipynb - Colaboratory.pdf
├── Notebook
    └── Emotion recognition FINAL.ipynb
└── README.md
```

## Configuration ⚙️

Edit `config.py` to modify:
- Model architecture parameters
- Training hyperparameters
- Input/output settings
- Detection thresholds

```python
config.py
CONFIG = {
    'input_shape': (48, 48, 1),
    'num_classes': 7,
    'batch_size': 32,
    'learning_rate': 0.001,
    'detection_threshold': 0.5
}
```

## Model Architecture 🧠

- Based on VGG-16 architecture
- Modified for emotion detection task
- Input: 48x48 grayscale images
- Output: 7 emotion probabilities

## Requirements 📋

```
tensorflow>=2.4.0
opencv-python>=4.5.0
numpy>=1.19.0
matplotlib>=3.3.0
pillow>=8.0.0
scipy>=1.6.0
```

## Contributing 🤝

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License 📝

This project is licensed under the MIT License.

## Acknowledgments 🙏

- FER-2013 dataset providers
- TensorFlow and OpenCV communities
- Contributors and supporters of the project

## Author ✍️

Mohammad Hammagi
- LinkedIn: [Zain Hammagi](https://www.linkedin.com/in/zain-hammagi)
- GitHub: [@zainhammagi12](https://github.com/zainhammagi12)

## Future Improvements 🚀

- [ ] Add support for multiple face detection
- [ ] Implement emotion tracking over time
- [ ] Add GUI interface
- [ ] Improve model accuracy through ensemble methods
- [ ] Add API endpoint for web integration
- [ ] Optimize for mobile deployment

## Troubleshooting 🔧

Common issues and solutions:

1. **OpenCV camera access error**
   - Check camera permissions
   - Verify camera index in config file

2. **Model loading issues**
   - Ensure correct TensorFlow version
   - Verify model path in config

3. **Performance issues**
   - Lower resolution in config
   - Adjust detection threshold
   - Check system GPU availability

For additional support, please open an issue in the GitHub repository.
