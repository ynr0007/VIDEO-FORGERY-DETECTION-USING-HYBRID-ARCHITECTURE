# 🎥 VIDEO-FORGERY-DETECTION-USING-HYBRID-ARCHITECTURE

In the age of digital media, video manipulation has become alarmingly easy and increasingly difficult to detect with the naked eye. This project introduces a **hybrid architecture** designed to tackle the complex challenge of video forgery detection by combining deep learning with traditional forensic techniques.

Our system intelligently analyzes spatial and temporal inconsistencies, motion patterns, and noise artifacts to flag tampered video frames—delivering a robust solution for ensuring video authenticity in critical fields such as journalism, surveillance, and legal evidence.

📚 **Interested in our follow-up research?**  
Check out the article published in the *4th International Conference on Latest Trends in Engineering and Management (ICLTEM), 2023.*

🔗 **[Read the Article (PDF)](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://iferp-in-docs.s3.ap-south-1.amazonaws.com/conf-proceedings/2023/ICLTEM-23-Proceeding.pdf)**

---

## 🗂️ Dataset

This project utilizes a publicly available dataset designed for deepfake detection, hosted on Kaggle.

📁 **[Access the Dataset on Kaggle](https://www.kaggle.com/code/krooz0/deep-fake-detection-on-images-and-videos#About-the-dataset)**

### Contents:

- **`train_sample_videos.zip`**:  
  Contains a curated subset of training videos along with a `metadata.json` file that includes the forgery labels.

- **`test_videos.zip`**:  
  A small set of videos used as a public validation set.

- **`sample_submission.csv`**:  
  Example submission file demonstrating the expected format for model predictions.

🔍 For detailed dataset structure, access methods, and full training data, refer to the Kaggle notebook’s *Getting Started* section.

This dataset is a rich resource for training and evaluating models that can detect tampered content across various video formats and compression levels.

---

## 📁 Project Repository Structure

Below is the structure of the project repository for **VIDEO-FORGERY-DETECTION-USING-HYBRID-ARCHITECTURE**:

```
VIDEO-FORGERY-DETECTION-USING-HYBRID-ARCHITECTURE/
│
├── VFD.ipynb           # Main working notebook with preprocessing, training, and evaluation logic
├── kaggle.json         # Kaggle API token (used to access datasets programmatically)
├── metadata.csv        # Supplementary metadata file for managing dataset labels or results
├── readme.md           # Project documentation
```

### Key File Descriptions

- **`VFD.ipynb`**:  
  Core notebook developed in Google Colab. Contains the entire pipeline — from loading data and preprocessing to training the hybrid model and evaluating its performance.

- **`kaggle.json`**:  
  Used to authenticate and access datasets directly from Kaggle via API.

- **`metadata.csv`**:  
  Stores additional information or labels linked to video samples, useful for training or evaluation.

- **`readme.md`**:  
  This file! It documents the project's purpose, setup, dataset details, and usage instructions.

---
## 📊 Metadata Description

The `metadata.csv` file provides detailed annotations for the video samples used in the project. This metadata is critical for training, validation, and evaluation phases.

### 📁 Columns:

| Column Name | Description |
|-------------|-------------|
| **filename** | Name of the video file. Example: `video123.mp4` |
| **label**    | Indicates whether the video is `REAL` or `FAKE` |
| **original** | If the video is `FAKE`, this field contains the filename of the original (authentic) source video |
| **split**    | Denotes the dataset split. For this project, the value is always `"train"` |

This metadata enables the model to distinguish between genuine and manipulated videos, and supports traceability between fake videos and their originals.

---

## ▶️ How to Run

This project is developed in Google Colab using a Jupyter Notebook. Follow the steps below to run the full pipeline from data access to model training and evaluation.

### 🛠️ 1. Clone the Repository

```bash
git clone https://github.com/your-username/VIDEO-FORGERY-DETECTION-USING-HYBRID-ARCHITECTURE.git
cd VIDEO-FORGERY-DETECTION-USING-HYBRID-ARCHITECTURE
```

### 📁 2. Set Up Kaggle Access (Optional)

If you're using Google Colab and accessing the dataset directly from Kaggle:

1. Go to your Kaggle account → Account → Create API Token.
2. Upload the downloaded `kaggle.json` file to your Colab session.
3. In the notebook, run:

```python
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```

4. Then download the dataset:

```python
!kaggle datasets download -d krooz0/deep-fake-detection-on-images-and-videos
```

### 🚀 3. Open and Run the Notebook

1. Launch **`VFD.ipynb`** in Google Colab or Jupyter Notebook.
2. Follow each section in the notebook:
   - Data loading and preprocessing
   - Feature extraction
   - Model definition and training
   - Evaluation and visualization

### ✅ 4. Output

The notebook will:
- Classify videos as `REAL` or `FAKE`
- Output model performance metrics (accuracy, precision, recall, etc.)
- Optionally save predictions in a submission format

---
## 📚 Citation

If you use this work in your research or applications, please cite the following paper:

> Pandey R, Singh Kushwaha Alok, Yerragondu Nikhil, Ram Tarak;  
> **"An Analysis of Video Forgery Detection Techniques"**;  
> *4th International Conference on Latest Trends in Engineering and Management*;  
> Institute for Research and Publication; ISBN: 978-93-92105-61-6;  
> Pune, India; pp: 42, 2023.

---

## 📝 License

This project is licensed under the **MIT License**.

You are free to use, share, and modify this work for any purpose, provided that the original authors are credited.

