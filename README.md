# ML Production Scaffold

This repository provides a scaffold for deploying Machine Learning models into production, including project structure, APIs, and deployment pipelines.

## Repository Structure

```
ml_production_scaffold/
│-- regression_model/
│   │-- config/   # General configurations
│   │-- datasets/ # Model input data
│   │-- processing/  # Model definition
│   │-- trained_models/  # Trained Models
│   │-- config.yml  # General configurations
│   │-- pipeline.py  # Preprocessing pipeline
│   │-- predict.py  # Inference code
│   │-- train_pipeline.py  # Training script
│   │-- VERSION 
│-- requirements/
│   │-- requirements.txt  # Requirements file
│   │-- test_requirements.txt  # Requirements to test environment
│-- tests/ # Unit tests
│-- setup.py  # setup project
│-- MANIFEST.in
│-- pyproject.toml  # Project dependencies
│-- tox.ini  # Project dependencies
│-- README.md  # Project documentation
```

## Requirements

Ensure you have Python 3.8+ installed and run:
```sh
pip install -r requirements.txt
```

## Model Training

To train the model:
```sh
python src/train.py
```

## Running the API

To start the API using FastAPI:
```sh
uvicorn api.main:app --host 0.0.0.0 --port 8000
```

## Testing

To run the tests:
```sh
pytest tests/
```

## Deployment with Docker

To build and run the container:
```sh
docker build -t ml_model .
docker run -p 8000:8000 ml_model
```
