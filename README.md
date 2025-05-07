# Deepfake Audio Detection Using Machine Learning

## Project Structure

- `Processed_Features` – Contains the extracted audio features as CSV files.
- `human_vs_ai_samples` – Audio samples used in the human-vs-AI comparison study.
- `saved_models` – Trained machine learning models saved for evaluation.
- `results` – Final evaluation metrics and model predictions.
- `notebooks` – Contains all main Jupyter notebooks used in the project.


## Main Notebooks

- `Data_Preparation.ipynb` – Organises the dataset folder structure for consistency.
- `Feature_Extraction.ipynb` – Extracts audio features and saves them as CSV files.
- `Exploratory_Data_Analysis.ipynb` – Visualises class distributions and feature patterns.
- `Model_Training.ipynb` – Trains five traditional ML models and performs internal validation using the FoR (for-norm) dataset.
- `External_Evaluation_and_Analysis.ipynb` – Evaluates model generalisation on the In-the-Wild dataset and conducts error analysis.
- `Human_Vs_AI.ipynb` – Supports a comparative experiment between human perception and model predictions.


## Datasets

This project uses two datasets:

1. **For-Norm Dataset** – A dataset used for training, validation, and internal testing.
   Availabe from: 
https://www.kaggle.com/datasets/mohammedabdeldayem/the-fake-or-real-dataset

3. **In-the-Wild Dataset** – A dataset used for external evaluation of model generalization.
   Available from:
https://www.kaggle.com/datasets/abdallamohamed312/in-the-wild-dataset

**Note:** In the code, the *In-the-Wild* dataset is referred to as `release_in_the_wild`, which reflects the folder name used when downloaded via the Kaggle API.


## Notes

The full pipeline has already been executed. Feature extraction, model training, and evaluation have been completed, and the outputs are included in the repository.

If you would like to download and re-run the pipeline:

1. Sign in to [Kaggle](https://www.kaggle.com/) and create an API token.
2. Place the `kaggle.json` file in the `~/.kaggle/` directory.
3. Use the Kaggle CLI to download the datasets:
   ```bash
   kaggle datasets download -d [dataset-owner]/[dataset-name]
   unzip dataset-name.zip -d ./data/
- Ensure that the folder names match what the notebooks expect.
