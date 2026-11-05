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
(table: Accuracy and F1 for Baseline CNN, Improved CNN, DINOv2)

## Demo video
(link to the video)

## Authors
Akniet, Zhibek

