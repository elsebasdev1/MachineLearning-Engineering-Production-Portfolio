\# Academic Performance Prediction



!\[Python](https://img.shields.io/badge/Python-3.8%2B-blue)

!\[License](https://img.shields.io/badge/License-MIT-green)

!\[Status](https://img.shields.io/badge/Status-Research-orange)



\## 📄 Overview



This repository hosts the implementation of the \*\*Orthogonal Risk Filtering\*\* framework, a novel architecture designed for \*\*Educational Data Mining (EDM)\*\*.



Unlike traditional models that prioritize raw accuracy, our approach specifically targets the "accuracy paradox" found in unbalanced educational datasets. By integrating \*\*Principal Component Analysis (PCA)\*\* as a noise filter mechanism to decouple multicollinearity, combined with a \*\*Class-Weighted Random Forest\*\*, this model provides robust predictions for at-risk students.



\## 🚀 Key Features



\* \*\*Orthogonal Risk Filtering:\*\* A two-stage pipeline that first orthogonalizes features to remove noise and multicollinearity.

\* \*\*Imbalance Handling:\*\* Utilizes class-weighted ensemble methods to prioritize sensitivity towards the minority class (at-risk students).

\* \*\*Robust Metrics:\*\* Focuses on F1-Score, Precision, and Recall rather than misleading Accuracy metrics.

\* \*\*Comparative Analysis:\*\* Includes benchmarks against standard SVM and unweighted Random Forest models.



\## 🛠️ Architecture



The framework operates in three main phases:



1\.  \*\*Data Preprocessing:\*\* Cleaning and normalization of behavioral and demographic data.

2\.  \*\*Dimensionality Reduction (PCA):\*\* Projects data into orthogonal components to isolate signal from noise.

3\.  \*\*Classification (Weighted RF):\*\* Applies a Random Forest with cost-sensitive learning to handle class imbalance.



\## 📦 Installation



1\.  \*\*Clone the repository:\*\*

&nbsp;   ```bash

&nbsp;   git clone \[https://github.com/your-username/orthogonal-risk-edm.git](https://github.com/your-username/orthogonal-risk-edm.git)

&nbsp;   cd orthogonal-risk-edm

&nbsp;   ```



2\.  \*\*Create a virtual environment (optional but recommended):\*\*

&nbsp;   ```bash

&nbsp;   python -m venv venv

&nbsp;   source venv/bin/activate  # On Windows use `venv\\Scripts\\activate`

&nbsp;   ```



3\.  \*\*Install dependencies:\*\*

&nbsp;   ```bash

&nbsp;   pip install -r requirements.txt

&nbsp;   ```



\## 💻 Usage



To replicate the study or train the model on new data:



1\.  Place your dataset in the `data/` directory (see `data/README.md` for format).

2\.  Run the main analysis notebook:

&nbsp;   ```bash

&nbsp;   jupyter notebook notebooks/01\_Analysis\_and\_Modeling.ipynb

&nbsp;   ```

3\.  Or execute the training script directly:

&nbsp;   ```bash

&nbsp;   python src/train.py --input data/students.csv --components 10

&nbsp;   ```



\## 📊 Results Snapshot



| Model | Accuracy | Precision | Recall | F1-Score |

|-------|----------|-----------|--------|----------|

| Standard SVM | 0.89 | 0.65 | 0.40 | 0.49 |

| Random Forest (Baseline) | 0.92 | 0.78 | 0.55 | 0.64 |

| \*\*Orthogonal Risk Filtering (Ours)\*\* | \*\*0.91\*\* | \*\*0.82\*\* | \*\*0.88\*\* | \*\*0.85\*\* |



\*> Note: While accuracy is comparable, our framework significantly improves Recall, ensuring at-risk students are correctly identified.\*



\## 📝 Citation



If you use this code or framework in your research, please cite our work:



```bibtex

@article{yourname2025,

&nbsp; title={Orthogonal Risk Filtering: Addressing the Accuracy Paradox in EDM},

&nbsp; author={Sinchi, Sebastian and \[Co-authors]},

&nbsp; journal={Journal Name},

&nbsp; year={2025}

}



