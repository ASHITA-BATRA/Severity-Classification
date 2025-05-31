# Dataset with Stuttering Severity Labels

This repository contains preprocessing scripts and documentation related to assigning **stuttering severity labels** to speakers using the **AS-70: A Mandarin stuttered speech dataset for automatic speech recognition and stuttering event detection**. Severity thresholds were determined based on the stuttering rate (SR) calculated from the dataset.

---

## 📌 Description

We use the **AS-70** dataset to assign stuttering severity labels (Mild, Moderate, Severe) to each speaker. The severity labeling helps in downstream tasks such as speech recognition robustness evaluation, fluency analysis, and personalized therapy applications.

---

## 🧮 How Severity is Calculated

Stuttering severity is computed based on the **Stuttering Rate (SR)**:

> **SR = (Number of stuttering events) / (Number of non-stuttering characters in the transcription)**

Based on the SR, we define severity thresholds as follows:

| Stuttering Rate (SR)       | Severity Label |
|----------------------------|----------------|
| SR < 7%                    | Mild           |
| 7% ≤ SR < 12%              | Moderate       |
| SR ≥ 12%                   | Severe         |

---

## 📂 Datasets Used

- **AS-70 Dataset** (primary source for severity computation)
- **FluencyBank Time Stamped**:  
  [Download ZIP](https://talkbank.org/fluency/derived/TimeStamped.zip)
- **LibriStutter**:  
  [GitHub Repository](https://github.com/hhzhang16/LibriStutterData.git)

---

## 🛠️ Technologies

- Python (3.8+)
- Pandas / NumPy
- Custom parsing scripts for transcription and event tagging

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/stuttering-severity-labels.git
cd stuttering-severity-labels
