# 🐶🐱 Dog vs Cat Classification using VGG16 Transfer Learning

This project implements a **Dog vs Cat image classifier** using **Transfer Learning** and **Fine-Tuning** with the pretrained **VGG16** model in TensorFlow/Keras.

The model was developed and trained entirely in **Google Colab** using GPU acceleration.

---

## 🚀 Project Highlights

* ✅ Transfer Learning using pretrained **VGG16**
* ✅ Fine-Tuning of deeper convolutional layers
* ✅ Data Augmentation to improve generalization
* ✅ Implemented in **Google Colab**
* ✅ Binary classification: **Dog 🐶 vs Cat 🐱**

---

## 🛠 Technologies Used

* Python
* TensorFlow
* Keras
* Google Colab
* NumPy
* Matplotlib

---

## 📂 Dataset

The model was trained on the popular **Dogs vs Cats** dataset containing images of dogs and cats.

The dataset was loaded and processed using Keras data generators with real-time data augmentation.

---

## 🏗 Model Architecture

### Base Model

* **VGG16**
* Pretrained on **ImageNet**
* `include_top=False`

### Transfer Learning

Initially, all convolutional layers were frozen and only the custom classification head was trained.

### Fine-Tuning

Later, the deeper layers of VGG16 were unfrozen and retrained with a very small learning rate to improve performance.

### Classification Head

* GlobalAveragePooling2D
* Dense Layer with ReLU activation
* Output Layer with Sigmoid activation

---

## 🔄 Data Augmentation

The following augmentation techniques were used:

* Rotation
* Zoom
* Horizontal Flip
* Shear Transformation

This helped reduce overfitting and improved validation performance.

---

## ⚙️ Training Configuration

| Parameter         | Value               |
| ----------------- | ------------------- |
| Input Size        | 150 × 150           |
| Optimizer         | RMSprop             |
| Learning Rate     | 1e-5                |
| Loss Function     | Binary Crossentropy |
| Output Activation | Sigmoid             |

---

## 📈 Results

The model achieved high classification accuracy on the validation set while leveraging significantly fewer trainable parameters compared to training a CNN from scratch.

---

## 📁 Repository Structure

```text
Dog-Cat-Transfer-Learning/
│
├── Transfer_Learning_Fine_Tuning.ipynb
└── README.md
```

---

## ▶️ Running the Project

1. Open the notebook in **Google Colab**.
2. Enable GPU:

   * `Runtime → Change Runtime Type → GPU`
3. Run all cells sequentially.

---

## 🎯 Future Improvements

* Experiment with EfficientNet and DenseNet architectures.
* Use callbacks such as EarlyStopping and ReduceLROnPlateau.
* Deploy the model using Flask or Streamlit.
* Convert the model into a web application.

---

## 👨‍💻 Author

**Tushar Biswas**
BTech CSE (Data Science)
Machine Learning and Deep Learning Enthusiast
