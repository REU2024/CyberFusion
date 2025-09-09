# CyberFusion  

**CyberFusion** is a hybrid ransomware detection framework designed for **small businesses**.  
It combines fast **static screening** with selective **dynamic analysis**, achieving both **efficiency** and **high accuracy** in detecting ransomware threats.

---

## Data Policy  

**Do not commit raw samples.**  
Only include metadata or synthetic examples in the `data/` directory.

---

## Results (Summary)  

- **Static RF Trigger**:  
  ~99.97% accuracy on **benign vs malicious** classification (with high recall)

- **Hybrid Fusion Model**:  
  ~99.5% overall accuracy with **strong calibration**

---

## Disclaimer  

This project is intended for **research and educational purposes only**.  
**Never run unknown binaries** outside of a secure and isolated environment.

---

## Architecture  

- **Stage 1**: Static PE metadata → **Random Forest** trigger → _benign or suspicious_  
- **Stage 2**: Sandbox API calls → **BiLSTM** classifier for ransomware behavior  
- **Optional Fusion**: Static features + dynamic sequence embedding → **CNN + BiLSTM head**

---

## Datasets Used

This project utilizes curated and publicly available datasets, including:

- `MarauderMap`: Dynamic ransomware/malware behavior logs  
  [https://github.com/THU-WingTecher/MarauderMap](https://github.com/THU-WingTecher/MarauderMap)

- `DikeDataset`: API call sequences for dynamic analysis  
  [https://github.com/iosifache/DikeDataset](https://github.com/iosifache/DikeDataset)

- `BODMAS`: Benchmarking dataset for behavior-based malware analysis  
  [https://github.com/whyisyoung/BODMAS](https://github.com/whyisyoung/BODMAS)

- `Benign-NET`: Benign Windows executables for contrastive learning  
  [https://github.com/bormaa/Benign-NET](https://github.com/bormaa/Benign-NET)

---

## Reproduce in Colab  

[🔗 Open the main notebook in Colab](https://colab.research.google.com/github/REU2024/CyberFusion/blob/main/notebooks/CyberFusion.ipynb)

---

##  Environment Setup  

Install dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
