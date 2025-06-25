# Robustness of a Face Recognition System to Adversarial Attacks

## 📌 Overview

This project aims to **evaluate the security and robustness of a face recognition-based access control system** when subjected to adversarial attacks with limited intensity. It also explores and analyzes possible defense strategies to improve the resilience of such systems in real-world scenarios.

The workflow covers dataset preparation, model evaluation, adversarial example generation, transferability tests to other classifiers, defense mechanisms, and a comprehensive experimental report.

## 🎯 Purpose

- 🛡️ Assess the robustness of a face recognition network (**NN1**) against different types of adversarial attacks
- 🔄 Test the transferability of attacks to a second classifier (**NN2**)
- 🧪 Experiment with at least one defense mechanism
- 📝 Document the entire process and experimental results

---

## 🧰 Tech Stack

| ⚙️ Tool / Library                    | 🔍 Purpose                                 | 💻 Version / Note               |
|:-------------------------------------|:-------------------------------------------|:--------------------------------|
| Python                               | Core programming language                  | >= 3.7 (rec. 3.10.16)           |
| TensorFlow / PyTorch                 | Face recognition models                    |                                 |
| Adversarial Robustness Toolbox (ART) | Adversarial attack generation & evaluation |                                 |
| numpy, pandas, scikit-learn          | Data manipulation & ML utilities           |                                 |
| matplotlib                           | Data visualization                         |                                 |
| Jupyter Notebook                     | Experiment workflow & reporting            |                                 |
| conda                                | Isolated/reproducible env management       |                                 |

---

## 🗂️ Dataset

- **VGG-Face2:** a large-scale face recognition dataset with over 3 million images of 9,131 identities.
- **Train set:**
    - 100 randomly selected identities, listed in [training_identities.csv](training_identities.csv)
    - 20 images per identity, for a total of 2,000 images, organized in the [train](train) directory by `ClassID`

---

## 📁 Repository Structure

- `Face-Recognition-Model.ipynb` – Main notebook with the entire workflow
- `training_identities.csv` – Selected identities for the test set
- Support folders: `datasets/`

---

## 🔧 Environment Setup

To avoid polluting your system, it is **strongly recommended** to use a dedicated conda environment.

### 1. Clone the repository

```bash
git clone https://github.com/Lucass282/AI4cybersecurity.git
cd AI4cybersecurity
```

### 2. Create a conda environment

```bash
conda create -n face_recognition_env python=3.10
conda activate face_recognition_env
```

### 3. Install required packages

```bash
pip install -r requirements.txt
```

### 4. Download the VGG-Face2 dataset
You can download the VGG-Face2 dataset from [here](https://www.robots.ox.ac.uk/~vgg/data/vgg_face2/). Follow the instructions to download and extract the dataset into the `datasets/` folder
> See the [notes](#-notes) section.

### 5. Run the Jupyter Notebook

```bash
jupyter notebook Face-Recognition-Attacks.ipynb
```

---

## 🧪 Experimental Workflow
1. **Dataset Preparation**: Load the VGG-Face2 dataset and prepare the training set with 100 identities
2. **Model Evaluation**: Train a face recognition model (NN1) on the training set and evaluate its performance
3. **Adversarial Attack Generation**: Use the Adversarial Robustness Toolbox (ART) to generate adversarial examples against NN1
4. **Transferability Tests**: Test the transferability of the generated adversarial examples to a second classifier (NN2)
5. **Defense Mechanisms**: Implement at least one defense mechanism to improve the robustness of the face recognition system
6. **Experimental Report**: Document the results of the experiments, including model performance, attack success rates, and defense effectiveness
7. **Analysis and Discussion**: Analyze the results, discuss the implications of adversarial attacks on face recognition systems and suggest potential improvements
8. **Conclusion**: Summarize the findings and provide recommendations for future work in this area
9. **Future Work**: Suggest areas for further research, such as exploring more advanced defense mechanisms or testing additional adversarial attacks

---

## 📌 Notes
- Ensure you have sufficient disk space for the VGG-Face2 dataset, as it is quite large
- The project is designed to be modular, allowing you to easily add new attacks or defenses as needed
- Feel free to modify the notebook to suit your specific requirements or to add additional experiments
- The project is intended for educational purposes and to demonstrate the robustness of face recognition systems against adversarial attacks. It is not intended for production use

---

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details

---

## 👤 Authors
- [Luca Concilio](https://github.com/Lucass282)
- [Emanuele Relmi](https://github.com/Kirito-Emo)
- [Francesco Quagliuolo](https://github.com/quagliofranci)
- [Giuseppe Alfonso Mangiola](https://github.com/PeppeMangiola)