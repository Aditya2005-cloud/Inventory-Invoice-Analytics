# Inventory Invoice Analytics

An end-to-end analytics project for vendor invoice intelligence. The app combines two machine learning workflows:

- Freight cost prediction
- Invoice risk flagging for manual review

## Features

- Predict expected freight cost from invoice inputs
- Flag invoices that look unusual or risky
- Streamlit dashboard for interactive use
- Trained model artifacts saved for inference

## Project Structure

```text
.
|-- app.py
|-- freight_cost_prediction/
|-- inference/
|-- invoice_flagging/
|-- models/
|-- notebooks/
|-- images/
|-- requirements.txt
|-- README.md
```

## Requirements

- Python 3.11+
- Streamlit
- pandas
- numpy
- scikit-learn
- plotly

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Run the App

```bash
streamlit run app.py
```

## Inference Scripts

You can also test the models directly:

```bash
python inference/predict_freight.py
python inference/predict_invoice_flag.py
```

## Training

If you want to rebuild the models:

```bash
python freight_cost_prediction/train.py
python invoice_flagging/train.py
```

## Notes

- `inventory.db` contains the source SQLite data used by the project.
- Model files in `models/` are used by the Streamlit app and inference scripts.

## Author

Ayushi Mishra

