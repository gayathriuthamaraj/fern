# Fern - Experimentation-based machine learning platform

Web-based machine learning platform for training, evaluating, and managing ML models through a no-code interface. Built with React, TypeScript, FastAPI, and Scikit-learn.

---

## Overview

Lazy Machine Learning provides an interactive environment for:
- dataset upload and preprocessing
- configurable model training
- real-time metric visualization
- trained model persistence and download

The platform focuses on simplifying experimentation workflows while exposing configurable ML parameters through a clean UI.

---

## Features

### Machine Learning Workflows
- Linear Regression
- Logistic Regression
- Ridge Regression
- Lasso Regression
- K-Nearest Neighbors
- Support Vector Machine
- Random Forest

### Platform Capabilities
- Interactive dataset upload
- Configurable hyperparameter selection
- Real-time metric visualization
- User authentication
- Saved model management
- Downloadable trained models

### Evaluation Metrics
- R² Score
- RMSE
- MAE

---

## Tech Stack

### Frontend
- React
- TypeScript
- TailwindCSS
- Plotly.js
- Vite

### Backend
- FastAPI
- Pandas
- Scikit-learn
- Joblib

---

## System Architecture

```text
Frontend (React + TypeScript)
        ↓
FastAPI Backend
        ↓
ML Training Pipeline
        ↓
Model Persistence Layer
````

---

## Project Structure

```text
lazy_machine_learning/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── models/
│   └── metadata/
├── src/
│   ├── models/
│   ├── components/
│   ├── api/
│   ├── layout/
│   └── App.tsx
├── public/
├── package.json
└── vite.config.ts
```

---

## Running the Project

### Backend

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

Backend runs on:

```text
http://localhost:8000
```

### Frontend

```bash
npm install
npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## API Endpoints

### Authentication

* `POST /auth/signup`
* `POST /auth/login`

### Models

* `POST /train`
* `GET /models`
* `GET /models/{model_id}`
* `GET /download/{model_id}`

---

## Dataset Requirements

Uploaded CSV datasets must:

* contain a `target` column
* include feature columns
* use valid headers and formatting

Example:

```csv
feature1,feature2,feature3,target
1.2,3.4,5.6,10.5
2.1,4.3,6.5,12.3
```
