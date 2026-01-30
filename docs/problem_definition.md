# Problem Definition – Patient Digital Twin for Heart Disease

## 1. Prediction Target
The objective of this project is to predict the **risk trajectory of a heart disease event** for an individual patient over time, rather than making a single static prediction.

Specifically, the digital twin outputs a **probability of a cardiovascular event occurring within the next 6 months**, updated at regular intervals as new patient data becomes available.

---

## 2. Time Horizon
- Observation window: Past **12 months** of patient data
- Prediction window: **Next 6 months**
- Update frequency: **Monthly updates** to the digital twin state

The digital twin is refreshed each time new clinical or lifestyle data is observed.

---

## 3. Inputs (Patient Data)
The digital twin consumes longitudinal patient data grouped as follows:

### Static Inputs
- Age
- Sex
- Family history of heart disease

### Time-Varying Inputs
- Vitals: blood pressure, heart rate
- Laboratory values: cholesterol levels, blood glucose
- Lifestyle factors: smoking status, physical activity (if available)
- Medications: ongoing heart-related prescriptions

Static inputs remain constant, while time-varying inputs are updated at each timestep.

---

## 4. Outputs (Digital Twin Predictions)
At each timestep, the digital twin produces:
- A **risk probability** of a heart disease event within the next 6 months
- A **risk trajectory**, showing how the patient’s risk evolves over time

These outputs allow clinicians to observe trends rather than isolated predictions.

---

## 5. Interventions
The digital twin supports simulation of clinical and lifestyle interventions, including:
- Initiation or discontinuation of heart-related medication
- Smoking cessation
- Improved physical activity levels

Computationally, interventions are modeled as changes in future input sequences, allowing the twin to simulate how altered inputs affect future risk trajectories.

---

## 6. Baseline vs Digital Twin Comparison

### Baseline Model
- Uses a single snapshot of patient data
- Produces one static risk prediction
- Ignores temporal progression and interventions

### Digital Twin Model
- Maintains a continuously updated patient state
- Produces time-dependent risk predictions
- Enables forward simulation of interventions

The digital twin provides decision support rather than one-time risk scoring.

---

## 7. Success Metrics

### Baseline Model Metrics
- ROC-AUC
- Precision-Recall
- Calibration score

### Digital Twin Metrics
- ROC-AUC over time
- Trajectory prediction error
- Risk trend consistency across timesteps

The digital twin is evaluated on both predictive accuracy and temporal reliability.

---

## 8. Intended Use
This system is designed as a **clinical decision-support and research tool**, not as a diagnostic system. Its purpose is to assist in understanding disease progression and intervention impact over time.
