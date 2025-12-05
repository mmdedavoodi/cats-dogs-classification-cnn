
# Cats vs Dogs Classification – Custom CNN (PyTorch)

This repository contains a clean and reproducible implementation of a Convolutional Neural Network trained to classify **cats** and **dogs** from the *Cats and Dogs Filtered* dataset using **PyTorch**.  
The model is built from scratch (no pretrained networks), trained with custom augmentations, and evaluated on a separate validation set.

---

## 🚀 Features

- Custom PyTorch CNN (no transfer learning)
- Supports GPU acceleration
- Strong data augmentation pipeline (jitter, crop, rotation, flip)
- Clean training loop with progress bars (tqdm)
- Training/validation loss & accuracy plots
- Lightweight and reproducible setup

---

## 📁 Project Structure

```
Cats_CNN.ipynb        # Main notebook containing full training pipeline
requirements.txt      # Dependencies
.gitignore            # Common ignored files for a clean repo
LICENSE               # MIT License
README.md             # This file
```

Dataset **is not included** in the repository.

---

## 📦 Dataset

This project uses the **Cats and Dogs Filtered Dataset** from TensorFlow.

Colab automatically downloads it using:

```python
!gdown 1IcAf8TmM2T7HB_jvb-cKela94_ZIPuqP
!unzip cats_and_dogs_filtered.zip
```

If running locally, download the dataset manually or use the same `gdown` command.

---

## 🔧 Installation

Install dependencies:

```bash
pip install -r requirements.txt
```

If running in Jupyter Notebook outside Colab, ensure `jupyter` is installed.

---

## ▶️ Running the Model

1. Open the notebook:

```bash
jupyter notebook Cats_CNN.ipynb
```

2. Run all cells  
3. The notebook will:
   - Download and extract the dataset  
   - Create custom PyTorch datasets  
   - Build and train the CNN  
   - Evaluate performance  
   - Display accuracy/loss plots  

---

## 🧠 Model Architecture

The model is a custom-built CNN:

- BatchNorm2d  
- Conv2d → ReLU  
- Conv2d → ReLU  
- MaxPool2d  
- BatchNorm2d  
- (Repeated block with more filters)  
- Flatten  
- Linear → Sigmoid  

Output layer predicts **cat (1)** or **dog (0)**.

---

## 📊 Results

Typical performance after ~30 epochs:

- **Training accuracy:** ~95–98%  
- **Validation accuracy:** ~90–95%  
- Loss curves and metric plots appear at the end of the notebook.

Results vary depending on GPU, augmentations, and initialization.

---

## 🔄 Data Augmentation

Training transforms include:

- RandomCrop  
- HorizontalFlip  
- Rotation  
- ColorJitter  
- Normalization  
- Resize  

These augmentations help avoid overfitting due to the small dataset.

---

## 📝 License

This project is licensed under the **MIT License**.  
Feel free to use, modify, and distribute.

---

## ⭐ Contribution

Contributions, suggestions, and improvements are welcome.  
Submit a pull request or open an issue.

---

## 🙌 Acknowledgments

- Dataset originally provided by TensorFlow  
- Implementation built fully in **PyTorch**  
- Notebook developed and tested in Google Colab

---
