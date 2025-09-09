# CyberFusion  

Hybrid ransomware detection for small businesses: fast static screening plus selective dynamic analysis.  

## Architecture  
- Stage 1: Static PE metadata → Random Forest trigger → benign or suspicious  
- Stage 2: Sandbox API calls → BiLSTM classifier for ransomware behavior  
- Optional fusion: static features + dynamic sequence embedding → CNN + BiLSTM head  

## Key Features  
- Lightweight design suitable for small business infrastructure  
- Modular pipeline: easily swap static or dynamic models  
- High accuracy and interpretability via Random Forest feature importances  

## Reproduce in Colab  
[Open the main notebook in Colab](https://colab.research.google.com/github/REU2024/CyberFusion/blob/main/notebooks/CyberFusion.ipynb)  

## Environment  
Install from `requirements.txt`:  

```bash
pip install -r requirements.txt
