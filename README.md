# Malaria_Image_Diagnosis_CNN_SVM_ML_2023
This repository contains the code, data, and result files for the project " Enhancing Malaria Diagnosis: Comparative Analysis of CNN and SVM Models for P. vivax Cell Detection" developed as a final project in the course Data Mining, Machine Learning, and Deep Learning at the Copenhagen Business School.

## Course Description
The course aimed to teach students about the fundamental challenges of machine learning, such as model selection and model complexity, and the underlying mathematical relationships within and across machine learning algorithms. Students were also taught to characterize the strengths and weaknesses of various machine learning approaches and algorithms, design, implement, analyze, and apply different data mining, machine learning techniques, and deep learning techniques for big/business datasets in organizational contexts and for real-world applications. The course also covered the application areas, trends, and challenges in data mining and machine learning. The students were required to complete a project and report that reflected on their critical awareness of methodological choices and written skills to accepted academic standards.

## Authors
Konstantin Kleffke
Linda Schombach
Mira Metzger

## Folder Structure

The folders are structured as follows:

```bash
.
├── Code
│   ├── 1_data_preparation.ipynb
│   ├── 2_training.ipynb
│   ├── 3_testing.ipynb
│   └── 4_scores_test_statistics.ipynb
├── README.md
└── Report.pdf
```

## Notebooks

To reproduce the results of this project, execute the notebooks in the folder /Code. The notebooks are numbered based on the stage in the workflow.

**1_data_preparation.ipynb**:
* Preprocess the raw data file, generate the training and test sets, and stores resulting CSV files in a /Data folder. The test set is generated in a way so that it contains the same data for all three relevant dialects, i.e. GR, BE and VS.

**2_training.ipynb**:
* This notebook is run to add a new language to the model and finetune it on the SwissDial training dataset. This notebook is executed with a T4 GPU in Google Colab. The model used for training is the [facebook/nllb-200-distilled-600M](https://huggingface.co/facebook/nllb-200-distilled-600M) from Hugging Face. 

**3_testing.ipynb**:
* Generates translations for the synthetic test set and SwissDial test set between the source language (BE) and the target language (DE) using five different models trained on distinct embedding strategies. The fine-tuned models for Swiss German dialects GR, VS and BE can be found [here](https://drive.google.com/drive/folders/1Vfe1fAmGQdUWecqt2HKNxUkObRbRqfFo?usp=sharing).

**4_scores_test_statistics.ipynb**: 
* Notebook to calculate the BLEU, CHRF and TER scores as well as test statistics.


## Data

* The dataset [BBBC041](https://bbbc.broadinstitute.org/BBBC041) is obtained from the Broad Bioimage Benchmark Collection (BBBC) and holds 1.228 images that were manually created from P. vivax parasite infected humans in Manaus, Brazil, and Thailand with theire labels (infected or uninfected)
