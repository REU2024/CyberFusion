# CyberFusion  

Hybrid ransomware detection for small businesses: fast static screening plus selective dynamic analysis.  

## Architecture  
- Stage 1: Static PE metadata → Random Forest trigger → benign or suspicious  
- Stage 2: Sandbox API calls → BiLSTM classifier for ransomware behavior  
- Optional fusion: static features + dynamic sequence embedding → CNN + BiLSTM head  

## Reproduce in Colab  
[Open the main notebook in Colab](https://colab.research.google.com/github/REU2024/CyberFusion/blob/main/notebooks/CyberFusion.ipynb)  

## Environment  
Install from `requirements.txt`:  
```bash
pip install -r requirements.txt

Data

Do not commit raw samples. Keep only metadata or synthetic examples in data/.

Results (summary)

Static RF trigger: ~99.97% accuracy on benign vs malicious (high recall)

Hybrid fusion: ~99.5% accuracy with strong calibration

Disclaimer

This project is for research and education. Do not run unknown binaries outside an isolated environment.


