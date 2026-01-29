**DESCRIPTION**

This repository contains the implementation of an explainable deep learning framework
for automatic classification of breast thermographic images into benign and malignant
classes. The framework integrates multi-channel image preprocessing, transfer learning
using DenseNet121, hyperparameter ablation analysis, and Grad-CAM-based explainability
to improve transparency and reproducibility in thermographic computer-aided diagnosis.

**DATASET INFORMATION**

The thermographic images used in this study are obtained from the publicly available
Database for Mastology Research – Infrared (DMR-IR), curated by the Universidade Federal
Fluminense (UFF), Brazil.


**Dataset name:** Database for Mastology Research – Infrared (DMR-IR)

**Source URL:** https://visual.ic.uff.br/dmi/

**Data type:** Infrared breast thermograms

**Classes:** Benign (Healthy) and Malignant

**Number of images used:** 863

**Class distribution:** Affected – 689, Healthy – 174


The dataset is not redistributed in this repository and must be downloaded directly
from the official source in accordance with its usage policy.

**CODE INFORMATION**

The repository includes Python scripts and Jupyter notebooks implementing:
- Image preprocessing (grayscale normalization, Prewitt and Roberts edge detection)
- Three-channel image construction
- DenseNet121-based transfer learning model
- Custom classifier head design
- Hyperparameter ablation study
- Grad-CAM visualization and aggregation
- Performance evaluation and plotting

**USAGE INSTRUCTIONS**

**1. Clone the repository:**
   git clone https://github.com/Ramyasundhar/Explainable-AI.git

**2. Download the DMR-IR dataset from:**
   https://visual.ic.uff.br/dmi/

**3. Organize the dataset into training and validation folders:**

   **dataset
   
        train
        
              benign
              
              malignant
              
         val
         
               benign
               
               malignant**
                         

4. Open the main Jupyter notebook or Python script in Google Colab or a local environment.

5. Run preprocessing, training, and evaluation cells sequentially.

**REQUIREMENTS**

- Python 3.8+
- TensorFlow / Keras
- NumPy
- OpenCV
- Scikit-learn
- Matplotlib
- Scikit-image

**Recommended environment:** Google Colab with GPU support.

**METHODOLOGY**

1. Normalize thermographic images to [0,1].
2. Apply Prewitt and Roberts operators for edge enhancement.
3. Stack grayscale, Prewitt, and Roberts outputs into a three-channel input.
4. Extract features using ImageNet-pretrained DenseNet121.
5. Train a custom classifier with ablation over learning rates and FC layer sizes.
6. Generate Grad-CAM heatmaps for model interpretability.
7. Perform aggregated explainability and error analysis.

**CITATIONS**

If you use this code or dataset, please cite:
- The DMR-IR dataset source: https://visual.ic.uff.br/dmi/
- The corresponding research article describing this framework.

**LICENSE & CONTRIBUTIONS**

This code is provided for academic and research purposes.
Users are encouraged to cite the original authors.
Contributions and issues can be submitted via GitHub.
