# 🖼️ Image Caption Generator (CNN + LSTM)

A complete end-to-end Deep Learning project that automatically generates descriptive captions for images. It uses a **Convolutional Neural Network (CNN)** to extract visual features and a **Long Short-Term Memory (LSTM)** network to generate natural language sequences.

The project includes a Jupyter Notebook for training on the Flickr8k dataset and a user-friendly **Streamlit web application** for real-time inference.

-----

## ✨ Features

  * **Deep Learning Architecture**: Combines state-of-the-art image feature extraction with recurrent neural networks for sequence modeling.
  * **Interactive Web Interface**: A clean, easy-to-use Streamlit GUI that allows users to upload any image and get an instant caption.
  * **Custom Trained**: Model trained from scratch on the widely used Flickr8k dataset.
  * **Visual Results**: Displays the uploaded image alongside the generated caption in a neat Matplotlib/Streamlit integration.

-----

## 🛠️ Tech Stack

  * **Language:** Python
  * **Deep Learning Framework:** TensorFlow / Keras
  * **Web Framework:** Streamlit
  * **Data Processing:** NumPy, Pandas
  * **Image Processing:** Pillow (PIL), Matplotlib

-----

## 📁 Project Structure

```text
├── models/
│   ├── model.keras              # The trained captioning model (CNN+LSTM)
│   ├── feature_extractor.keras  # The pre-trained CNN feature extractor
│   └── tokenizer.pkl            # Pickle file containing the text tokenizer
├── flickr8k-image-captioning-using-cnns-lstms.ipynb  # Training notebook
├── main.py                      # Streamlit application script
├── requirements.txt             # Project dependencies
└── README.md                    # Project documentation
```

-----

## 🚀 Getting Started

Follow these instructions to run the project on your local machine.

### 1\. Clone the repository

```bash
git clone https://github.com/HARSH-GOHIL-git/image-caption-generator.git
cd image-caption-generator
```

### 2\. Install dependencies

It is recommended to use a virtual environment.

```bash
pip install -r requirements.txt
```

*(If you don't have a `requirements.txt`, you will need: `tensorflow`, `streamlit`, `numpy`, `matplotlib`, `pillow`)*

### 3\. Add the Model Files

Ensure that your trained models and tokenizer are placed inside a `models/` directory in the root folder, exactly as named in the project structure above.

### 4\. Run the Streamlit App

```bash
streamlit run main.py
```

The application will launch in your default web browser at `http://localhost:8501`.

-----

## 🧠 How It Works

1.  **Feature Extraction**: When an image is uploaded, it is resized to $224 \times 224$ pixels and passed through the `feature_extractor` (a CNN) to create a dense representation of the image.
2.  **Sequence Generation**: The LSTM model takes these image features and a `startseq` token to begin predicting the caption word by word.
3.  **Decoding**: The predicted word indices are converted back to readable text using the saved `tokenizer.pkl` until an `endseq` token is generated or the maximum length is reached.

-----

## 📊 Dataset

This model was trained using the **Flickr8k Dataset**, which contains 8,000 images, each paired with 5 different descriptive captions.

  * [Flickr8k Dataset on Kaggle](https://www.kaggle.com/datasets/adityajn105/flickr8k)

-----

## 🤝 Contributing

Contributions, issues, and feature requests are welcome\! Feel free to check the [issues page](https://github.com/HARSH-GOHIL-git/image-caption-generator/issues).

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.