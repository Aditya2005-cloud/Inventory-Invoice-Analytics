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


pip install altair==6.2.2 anyio==4.14.2 attrs==26.1.0 blinker==1.9.0 cachetools==7.1.4 certifi==2026.6.17 charset-normalizer==3.4.9 click==8.4.2 colorama==0.4.6 GitPython==3.1.51 gitdb==4.0.12 h11==0.16.0 httptools==0.8.0 idna==3.18 itsdangerous==2.2.0 Jinja2==3.1.6 joblib==1.5.3 jsonschema==4.26.0 jsonschema-specifications==2025.9.1 MarkupSafe==3.0.3 narwhals==2.24.0 numpy==1.24.4 packaging==26.2 pandas==1.5.3 pillow==12.3.0 plotly==6.9.0 protobuf==7.35.1 pyarrow==24.0.0 pydeck==0.9.3 python-dateutil==2.9.0.post0 python-multipart==0.0.32 pytz==2026.2 referencing==0.37.0 requests==2.34.2 rpds-py==2026.6.3 scikit-learn==1.2.2 scipy==1.10.1 six==1.17.0 smmap==5.0.3 starlette==1.3.1 streamlit==1.59.2 tenacity==9.1.4 threadpoolctl==3.6.0 toml==0.10.2 typing_extensions==4.16.0 tzdata==2026.3 urllib3==2.7.0 uvicorn==0.51.0 watchdog==6.0.0 websockets==16.1
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


