# Hobby & Interest Classification (Books / Cosmetics / Flowers)

Assignment 2, Computer Vision, Astana IT University.

## What was done
- Dataset: 324 real photos, 3 classes (books, cosmetics, flowers), split 70/15/15
- SOTA component: DINOv2 (feature extractor) + Logistic Regression
- Comparison with A1: Baseline CNN, Improved CNN, DINOv2
- Explainability: attention heatmap, nearest-neighbors gallery
- Application: Gradio web app

## How to run
1. Open the notebook in Google Colab
2. Runtime -> Change runtime type -> T4 GPU
3. Put the dataset on Google Drive and update the `dataset_path` variable in the notebook
4. Runtime -> Run all
5. At the end, a Gradio link to the app will appear

## Environment
Colab (T4 GPU), transformers, gradio, scikit-learn, random_state=42

## Results
Test set: 51 images (18 books, 17 cosmetics, 16 flowers).

| Model | Accuracy | F1 (weighted) |
|---|---|---|
| A1 Baseline CNN | 0.8235 | - |
| A1 Improved CNN | 0.9412 | 0.9412 |
| A2 DINOv2 + LogReg | 1.0000 | 1.0000 |

Ablation (DINOv2 + LogReg):

| Setting | Accuracy | F1 (weighted) |
|---|---|---|
| No augmentation | 1.0000 | 1.0000 |
| + horizontal flip | 1.0000 | 1.0000 |

Note: the test set is small (51 images), so one error changes accuracy by about 2%.
The ablation shows no difference because DINOv2 features already separate these
three classes perfectly on this test set. The result may be optimistic: near-duplicate
web images could appear in both train and test splits.

## Demo video
(https://drive.google.com/file/d/17BHVrMiDu4LYMatxL4dzt51G2iBimGue/view?usp=drive_link)

## Authors
Akniet, Zhibek

