# 🧠 Student Mental Health Signal — Wellness Analytics

A machine learning powered web application that predicts a student's **mental health score from 0–10** using lifestyle, academic, social-media usage, physical activity, sleep, and perceived stress-related inputs.

> **Note:** This project is for informational and educational purposes only. It is **not a clinical or medical assessment**.

## 📌 Overview

**Student Mental Health Signal** is a web-based ML application where users enter information about their daily habits and lifestyle. The data is sent from the frontend to a **FastAPI backend**, validated using **Pydantic**, and passed to a saved machine learning model for prediction.

The predicted mental health score is then displayed on the web interface.

## ✨ Features

* Predicts a mental health score from **0–10**
* Simple and interactive web interface
* FastAPI backend for prediction
* Pydantic validation for user input
* Machine learning model loaded using Joblib
* REST API endpoint for predictions
* CORS enabled for frontend-backend communication
* Lifestyle and social-media related input analysis

## 🛠️ Tech Stack

### Frontend

* HTML
* CSS
* JavaScript

### Backend

* Python
* FastAPI
* Pydantic
* Pandas
* Joblib

### Machine Learning

* Pre-trained machine learning model
* Saved model file: `Mental_Health_Model.pkl`

## 🔄 How It Works

```text
User Input
    ↓
HTML / CSS / JavaScript
    ↓
POST /predict
    ↓
FastAPI
    ↓
Pydantic Validation
    ↓
Mental_Health_Model.pkl
    ↓
Predicted Mental Health Score
    ↓
Web Interface
```

## 📋 Input Features

The application collects the following information:

* Age
* Gender
* Country
* Academic Level
* Most Used Platform
* Purpose of Use
* Average Daily Usage Hours
* Daily Phone Unlocks
* Study Hours
* Physical Activity Hours
* Sleep Hours Per Night
* Perceived Stress Level

## 🚀 API

### `POST /predict`

The `/predict` endpoint accepts student information and returns the predicted mental health score.

### Response

```json
{
  "predicted_mental_health_score": 6.78
}
```

The prediction is returned as a floating-point value rounded to **2 decimal places**.

## 📂 Project Structure

```text
Student-Mental-Health/
│
├── index.html
├── style.css
├── script.js
├── main.py
├── Mental_Health_Model.pkl
└── README.md
```

## 💻 Run Locally

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Student-Mental-Health
```

### 2. Install dependencies

```bash
pip install fastapi uvicorn pandas joblib pydantic
```

### 3. Start the FastAPI server

```bash
uvicorn main:app --reload
```

### 4. Open the frontend

Open `index.html` in your browser and enter the required information.

## 🔐 Input Validation

The backend uses **Pydantic** to validate incoming data.

For example:

* Age is restricted between 10 and 100.
* Usage, study, physical activity, and sleep hours are validated.
* Gender, academic level, platform, purpose, and stress level accept predefined values.

This helps prevent invalid data from being passed to the prediction model.

## 🎯 Project Objective

The objective of this project is to demonstrate how a **machine learning model can be connected to a real web application** using a FastAPI REST API.

It combines:

**Machine Learning + Python Backend + API + Frontend**

## ⚠️ Disclaimer

This application provides an estimated score based on the information entered by the user. The result should **not be considered a medical diagnosis, professional mental-health assessment, or substitute for professional advice**.

## 👩‍💻 Author

**Kajal Verma**

B.Tech — Information Technology
