# MRI Tumor Detection 



This repository contains a Jupyter/Google Colab notebook that trains and evaluates a brain MRI tumor detection model.
**There is no web UI or frontend included** — this project is notebook-first and runnable in Colab or locally.

---

## Files
- `brain_tumor_training.ipynb` — Main notebook (training, evaluation, plots, and `model.h5` export)
- `model.h5` *(optional)* — Saved Keras model (if provided)
- `requirements.txt` *(optional)* — Python dependencies (if provided)

---

## Dataset
The notebook expects your MRI images to be available in Google Drive at:
```
/content/drive/MyDrive/MRI Images/Training/
 /content/drive/MyDrive/MRI Images/Testing/
```
Each class should be a subfolder inside `Training` and `Testing` (e.g. `glioma`, `meningioma`, `pituitary`, `notumor`).

---

## How to run (Google Colab)
1. Upload `brain_tumor_training.ipynb` to Google Colab.
2. Mount Google Drive when prompted (the notebook contains `drive.mount('/content/drive')`).
3. Ensure your dataset is in the Drive paths above.
4. Run cells top-to-bottom. The notebook will:
   - Load and augment images
   - Build and fine-tune a VGG16-based model
   - Train and display training curves
   - Produce classification report, confusion matrix, and ROC curves
   - Save the trained model as `model.h5`

---

## How to run (locally)
1. Install dependencies (example):
```bash
pip install tensorflow pillow scikit-learn matplotlib seaborn jupyter
```
2. Place your dataset in any folder and update the notebook paths accordingly.
3. Launch Jupyter Notebook / Jupyter Lab and open `brain_tumor_training.ipynb`.
4. Run all cells.

---

## Notes
- This repository intentionally contains **no UI**. If you later want a Flask frontend (`main.py`, `templates/index.html`), ask and it can be added.
- Training can be slow on CPU — use Colab GPU for faster results.
- The notebook saves the final model to `model.h5`. Move it to your app folder if you add a UI later.


## Contact
Author: **Kavya**

