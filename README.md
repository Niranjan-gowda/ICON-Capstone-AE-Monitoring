# Automated Adverse Event (AE) Monitoring

This project implements a pipeline to **extract, normalise, and report adverse events (AEs)** from FDA FAERS narrative text using biomedical NLP techniques. It was developed as part of the ICON Capstone project at UCD Smurfit in collaboration with ICON plc.

---

## Folder Structure
```
ICON-Capstone-AE-Monitoring/
├── data/
│   └── Asprin_trial.xlsx        # sample dataset
│
├── notebooks/
│   └── ICON_Capstone.ipynb      # main analysis notebook
│
├── reports/
│   └── Icon_Report.pdf          # detailed report
│
├── requirements.txt
├── README.md
```

---

## Features
- **Text Preprocessing** – cleans and normalises raw FAERS narratives.  
- **NER with SpaCy/SciSpaCy** – extracts biomedical entities.  
- **Negation Detection (NegSpaCy)** – removes false positives.  
- **Brand → Generic Mapping** – fuzzy matching & synonym resolution.  
- **Zero-Shot Classification** – BART/BioBERT/DistilBERT for AE tagging.  
- **Confidence Filtering** – default threshold: `0.96`.  
- **Export** – results in CSV, DOCX, PDF.  
- **Streamlit UI** – optional interactive dashboard.  
- **Ngrok support** – share dashboard via secure public URL.  

---

## Installation
Clone and install dependencies:
```bash
git clone https://github.com/Niranjan-gowda/ICON-Capstone-AE-Monitoring.git
cd ICON-Capstone-AE-Monitoring
pip install -r requirements.txt
```

---

## Usage
Run via notebook:
```bash
jupyter notebook notebooks/ICON_Capstone.ipynb
```

To share with ngrok:
```bash
ngrok http 8501
```

---

## Requirements
See `requirements.txt` for the full list. Includes:
- pandas, numpy, requests  
- spacy, scispacy, negspacy, textblob  
- transformers, torch  
- pyngrok, streamlit, plotly  
- python-docx, PyMuPDF, reportlab  
- and more for PDF/report exports.  

---

## Data & Ethics
- Input data: FAERS datasets (sample: `data/Asprin_trail.xlsx`).  
- Research/analysis only. Not for clinical decision support.  

---

## Acknowledgements
Developed as part of the MSc Business Analytics Capstone with **ICON plc** and **UCD Smurfit**.
