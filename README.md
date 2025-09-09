
# Brain Tumor Classification

Check out my project [here]( https://vtu23089-braintumor-classification.hf.space/?__theme=system)!



This is a **Deep Learning-based Brain Tumor Classification** application built with **Keras**, **TensorFlow**, and **Gradio**. It classifies MRI images into one of four categories:

- Glioma
- Meningioma
- No Tumor
- Pituitary Tumor

The  uses a **ResNet50-based CNN** model trained on a custom dataset of brain MRI images.

---

## Features

- Upload an MRI image and get instant prediction.
- Shows **probability for each class**.
- Preprocessing includes noise reduction and color mapping for MRI images.
- Data augmentation was applied during training to improve model generalization.



## Usage

1. Open the app interface.
2. Upload an MRI image.
3. View the predicted class and probabilities.

Example:

| Input Image | Prediction   |
| ----------- | ------------ |
| MRI Scan    | Glioma (95%) |

---

## Confusion Matrix

The model was evaluated on the test dataset, and the confusion matrix shows how well it performed:

![Confusion Matrix](confusion_matrix.png) *(optional: include if saved as image)*

Classification metrics:

* Accuracy
* Precision
* Recall
* F1-score

---

## Model

* **Architecture:** ResNet50 (pretrained on ImageNet) + custom classification head
* **Input size:** 150x150 (preprocessed)
* **Output:** Softmax probabilities for 4 classes
* **Training:** Data augmentation applied, EarlyStopping, ReduceLROnPlateau callbacks used
* **Saved model:** `best_brain_tumor_model.keras`

---

## Dataset

* Custom brain MRI dataset split into:

  * Training
  * Validation
  * Testing
* Classes: `glioma`, `meningioma`, `notumor`, `pituitary`
* MRI preprocessing: bilateral filter + bone color map + resizing

---

## Deployment

* Can be deployed directly on **Hugging Face Spaces** with `app.py` and `best_brain_tumor_model.keras`.
* Uses **Gradio** interface for interactive predictions.

