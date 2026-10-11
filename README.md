# Mental Health Prediction: ME/CFS & Depression

An interactive machine learning application that explores predicted categories related to Myalgic Encephalomyelitis/Chronic Fatigue Syndrome (ME/CFS), depression, or both, using user-provided health and lifestyle information.

## Live Application

**[Launch the Mental Health Prediction App](https://mental-health-predictions.streamlit.app/)**

## 1. Project Overview

Mental health and chronic health conditions can involve overlapping symptoms, including fatigue, sleep disturbances, difficulty concentrating, pain, and changes in daily functioning.

This project demonstrates how machine learning can be used to explore patterns in health-related data. It provides an interactive interface where users can enter selected health and lifestyle indicators, choose a trained machine learning model, and view the model's predicted category and associated probabilities.

The application is built with Python and deployed using Streamlit.

## 2. Understanding the Conditions

### Myalgic Encephalomyelitis / Chronic Fatigue Syndrome (ME/CFS)

ME/CFS is a complex, chronic illness that can substantially affect daily functioning. A characteristic feature is post-exertional malaise (PEM), in which symptoms worsen following physical, cognitive, or emotional exertion. People may also experience unrefreshing sleep, cognitive difficulties, pain, and severe fatigue.

### Depression

Depression is a mental health condition that can affect mood, interest or pleasure, energy, sleep, concentration, and everyday activities. Its presentation and severity vary from person to person.

### Why Explore Both?

Some symptoms, such as fatigue, sleep problems, and difficulty concentrating, may occur in multiple conditions. Exploring these indicators together can help demonstrate how predictive models identify patterns in structured data.

However, overlapping symptoms alone cannot establish a diagnosis, and a model's output cannot determine whether someone has either condition.

## 3. Project Objectives

- Build an interactive machine learning application using Python.
- Allow users to enter health-related and lifestyle information.
- Compare predictions from multiple trained classification models.
- Display predicted categories and their associated model probabilities.
- Demonstrate the deployment of a machine learning application using Streamlit.

## 4. Input Features

The application collects the following inputs:

| Category | Features |
|---|---|
| Demographics | Age, gender |
| Sleep | Sleep quality index, hours of sleep |
| Cognitive and physical symptoms | Brain fog level, physical pain score, fatigue severity |
| Mental well-being | Stress level, depression PHQ-9 score |
| Post-exertional symptoms | PEM presence, PEM duration |
| Daily functioning | Work status, social activity level |
| Lifestyle | Exercise frequency, meditation or mindfulness |

These inputs are assembled into a structured data frame before being passed to the selected model.

## 5. Machine Learning Models

The application provides three model options:

- **Logistic Regression:** Estimates class probabilities using a statistical classification approach.
- **Decision Tree Classifier:** Uses learned decision rules to assign a predicted category.
- **Random Forest Classifier:** Combines predictions from multiple decision trees.

The application loads the trained models from saved `.pkl` files. It does not retrain the models each time a user submits new inputs.

The selected model produces a predicted category and class probabilities. These probabilities represent the model's estimates for the available categories, not the clinical probability that a person has a particular condition.

## 6. How the Application Works

1. The user opens the Streamlit application.
2. The user selects one of the three trained models.
3. The user enters the requested health and lifestyle information.
4. The application encodes categorical inputs and prepares a data frame.
5. The selected model generates a prediction and class probabilities.
6. The application displays the predicted category and a probability bar chart.

## 7. Technologies Used

- **Python** — Application logic and data processing
- **Pandas** — Structuring input data in data frames
- **Scikit-learn** — Machine learning model interfaces
- **Pickle** — Loading previously trained model objects
- **Streamlit** — Interactive web interface and deployment

## 8. Repository Structure

```text
Wellness-Analytics-Prediction/
├── README.md
├── app (1).py
├── dt.pkl
├── lr.pkl
├── rf.pkl
├── mental_health.jpg
└── requirements.txt
```

- `app (1).py` — Main Streamlit application
- `dt.pkl` — Saved Decision Tree model
- `lr.pkl` — Saved Logistic Regression model
- `rf.pkl` — Saved Random Forest model
- `mental_health.jpg` — Image used in the interface
- `requirements.txt` — Python dependencies

## 9. Run the Project Locally

### Prerequisites

Install Python and Git on your computer.

### Step 1: Clone the repository

```bash
git clone https://github.com/Harshitb101/Wellness-Analytics-Prediction.git
cd Wellness-Analytics-Prediction
```

### Step 2: Create a virtual environment (recommended)

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Launch the application

```bash
streamlit run "app (1).py"
```

Streamlit will provide a local URL where you can access the application in your browser.

## 10. Limitations

- The application is dependent on the quality and representativeness of the data used to train its models.
- Model accuracy, generalizability, and clinical validity should not be assumed without appropriate evaluation.
- Predictions may be affected by incorrect, incomplete, or out-of-distribution inputs.
- The model's displayed probabilities are not equivalent to medically validated risk estimates.
- No clinical conclusions should be drawn from this demonstration alone.

## 11. Responsible Use Disclaimer

**This project is for educational and demonstration purposes only. It is not a medical diagnostic tool and must not be used to diagnose, screen, or make treatment decisions for ME/CFS, depression, or any other health condition.**

The predictions are generated by machine learning models and may be inaccurate or biased. Anyone experiencing health concerns should consult a qualified healthcare professional.

## 12. Future Improvements

- Evaluate models using appropriate metrics such as precision, recall, F1-score, and a confusion matrix.
- Document the dataset source, sample size, class distribution, and preprocessing methodology.
- Add model comparison results and explain the limitations of each model.
- Improve input validation and error handling.
- Add clearer explanations of model outputs and responsible-use guidance.

## Author

**Harshit B.**

[GitHub Repository](https://github.com/Harshitb101/Wellness-Analytics-Prediction) | [Live Streamlit Application](https://mental-health-predictions.streamlit.app/)
