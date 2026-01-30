# Dataset Decision – Patient Digital Twin for Heart Disease

## 1. Dataset Chosen
The dataset selected for this project is the **UCI Heart Disease Dataset**, obtained from the UCI Machine Learning Repository.

This dataset was chosen over clinical EHR datasets such as MIMIC because it does not require special access approval, is significantly easier to preprocess, and allows completion of an end-to-end deployed system within a limited daily time budget. Given the constraint of working one hour per day, this dataset provides the best balance between realism, feasibility, and execution quality.

---

## 2. What the Dataset Contains
The UCI Heart Disease dataset contains approximately **300 patient records**, each describing clinical and demographic attributes related to cardiovascular health.

Key features include:
- Age and sex
- Resting blood pressure
- Serum cholesterol
- Fasting blood sugar
- Maximum heart rate achieved
- Chest pain type
- Electrocardiographic results

The target variable indicates the **presence or absence of heart disease**, which can be interpreted as a cardiovascular risk indicator.

---

## 3. Why This Dataset Can Support a Digital Twin
Although the dataset is not natively longitudinal, it can be adapted to a digital twin framework by **synthetically modeling time**.

Each patient record is treated as a baseline health state. Temporal progression is simulated by generating multiple timesteps per patient, where clinical variables evolve according to medically plausible trends and noise assumptions. This allows the creation of a patient-specific risk trajectory rather than a single static prediction.

Interventions such as medication initiation, smoking cessation, or lifestyle improvement are simulated by modifying future input values and observing changes in predicted risk. While synthetic, this approach enables demonstration of the core digital twin concepts: state evolution, intervention simulation, and temporal risk modeling.

---

## 4. Limitations
- The dataset does not contain real longitudinal measurements, so temporal progression is simulated rather than observed.
- Intervention effects are assumed rather than derived from real treatment-response data.
- The small dataset size limits population-level generalization and requires careful evaluation.

These limitations are explicitly acknowledged and framed as trade-offs for feasibility and end-to-end deployment.

---

## 5. Justification Summary
The UCI Heart Disease dataset is the correct choice for this project because it enables a complete, deployable patient digital twin system within strict time constraints. While less realistic than ICU-scale EHR data, it allows clear demonstration of digital twin principles, interpretable modeling, and intervention simulation, which are the primary goals of this project.
