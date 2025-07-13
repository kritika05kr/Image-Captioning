# Image Caption Generator using CNN + LSTM

This project is a deep learning-based **Image Captioning System** that generates descriptive captions for uploaded images. It uses **CNNs (Convolutional Neural Networks)** to extract image features and **LSTM (Long Short-Term Memory)** networks to generate human-like captions. The interface is built using **Streamlit** for an interactive web app experience.

---

## Features

- Upload `.jpg`, `.jpeg`, or `.png` images
- Generate image captions using pre-trained models
- Visual display of uploaded image with predicted caption
- Easy-to-use Streamlit interface

---

## Project Structure

```
project/
│
├── models/
│   ├── model.keras                # Trained caption generation model
│   ├── feature_extractor.keras   # CNN model for image feature extraction
│   └── tokenizer.pkl              # Tokenizer object used during training
│
├── app.py                         # Streamlit application code
├── uploaded_image.jpg             # Temporary uploaded image (auto-created)
└── README.md                      # Documentation file
```

---

## Setup Instructions

Follow these steps to run the app on your local system.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/image-caption-generator.git
cd image-caption-generator
```

### 2. (Optional) Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install the Dependencies

If you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

If not, install manually:

```bash
pip install streamlit tensorflow numpy matplotlib
```

### 4. Add the Pre-trained Files

Place the following trained assets inside the `models/` folder:

- `model.keras` – The LSTM model trained for caption generation
- `feature_extractor.keras` – CNN model (e.g., InceptionV3 or VGG16)
- `tokenizer.pkl` – Tokenizer used during training

---

## How to Run the App

After setting up everything:

```bash
streamlit run app.py
```

It will open your browser with the image captioning interface.

---

## Model Details

### 🔹 CNN Encoder

- Pre-trained CNN (e.g., InceptionV3 or MobileNet)
- Extracts a fixed-size feature vector from the image

### 🔹 LSTM Decoder

- Takes image feature vector + partial caption sequence
- Outputs the next word prediction

### 🔹 Tokenizer

- Converts between words and integers for sequence modeling

---

## Dataset Used

- **Flickr8k** Dataset  
  - 8,000 images, each with 5 captions
  - [Dataset Link (register required)](https://forms.illinois.edu/sec/1713398)

---

## Future Improvements

- Use Beam Search instead of Greedy Decoding
- Try COCO dataset for richer captions
- Deploy on platforms like Hugging Face or Streamlit Cloud
- Add image attention for better interpretability

---

## Acknowledgments

- [Flickr8k Dataset](https://forms.illinois.edu/sec/1713398)
- TensorFlow + Keras Tutorials
- Streamlit for effortless UI

---

