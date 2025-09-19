# 🫀 A HYBRID MULTI-MODEL BASED APPROACH FOR HEART DISEASE DETECTION AND CLASSIFICATION

## 📌 Abstract

Our final year capstone project is centered on the early and precise detection of heart disease through a multi-modal methodology. We utilized three physiological signals — ECG (Electrocardiogram), PCG (Phonocardiogram), and PPG (Photoplethysmogram) — by developing individual machine learning models for each signal and subsequently integrating their outputs to evaluate heart disease risk.

## 🧠 Inspiration

In our literature review, we found that most existing studies concentrated on single-signal analysis, primarily seeking the best-performing model for that particular signal. However, this approach often restricts diagnostic accuracy. To overcome this limitation, we developed a system that harnesses the combined strengths of all three signals, enabling a more comprehensive and dependable evaluation.

## 🛤️ Workflow

1. **Data Collection**: We gathered the necessary datasets for training and validating our models from **Kaggle datasets** and Google.
2. **Model Training (Jupyter Notebook/Colab)**: The **ECG** model was trained using a **Convolutional Neural Network (CNN)** for image processing, the **PPG** model with a **Random Forest Classifier** for time-series data stored in CSV format, and the **PCG** model with a **Bidirectional Long Short-Term Memory (Bi-LSTM)** network for audio classification.
3. **Model Saving**: Once trained, we saved the best-performing models — best_ecg_cnn.pth and ecg_model.h5 for ECG, scaler.pkl and label_encoder.pkl for PPG, and SOUND_LSTM_model.h5 for PCG.
4. **Model Integration**:The saved models were then integrated, and a mathematical algorithm was applied to compute a risk score based on the confidence values from each model. This logic was implemented in Python .py files.
5. **Backend Development (Flask API)**:We built a Flask API within the .py files to load all three models and perform inference. This API also enabled communication with the frontend. User inputs (images, audio, and CSV files) are sent to the backend, processed, and the results are returned to the frontend as a **JSON** response.
6. **Frontend Integration (HTML, CSS, JavaScript)**: A simple user interface was designed where users can upload their data and view the model’s output.

## ⚙️ How to Run the Project

Following steps need to be followed:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/aryansmatte/A-HYBRID-MULTI-MODEL-BASED-APPROACH-FOR-HEART-DISEASE-DETECTION-AND-CLASSIFICATION

2. **Navigate to Frontend_and_Backend folder**

   ```bash
   cd Frontend_and_Backend

3. **Move to app folder which consist of frontend landing page index.html**

   ```bash
   cd app
   
4. **Navigate to INTGRATION folder which has main model code**

   ```bash
   cd INTGRATION

5. **Download virtual environment .venv in this folder**

   ```bash
    python -m venv .venv

6. **Install the requirements file**

   ```bash
   pip install -r requirements.txt

7. **If any error persists for pip**

   ```bash
   pip install --upgrade pip

8. **If any error related to openpyxl**

   ```bash
   pip install openpyxl
   pip install --force-reinstall openpyxl

9. **Activate the virtual environment**

    ```bash
    .venv\Scripts\Activate

10. **Running the backend file may take 2-3 minutes**

    ```bash
    python app.py

11. **In app folder you can start the frontend landing page by clicking on `index.html` and navigate to the Fusion option to access model predictions. (Note: In VS Code, frontend output might not render due to internal preview limitations.)** 

## 🧾 Output and Results 

   ### 🛬 Landing Page Layout

   <p align="center">
  <img width="1899" height="862" alt="Image" src="https://github.com/user-attachments/assets/5cfdb61b-d81e-4bf4-8f5b-1985b0638d28" />
</p>
    
   ### 🚀 User Interface Video
   
   https://github.com/user-attachments/assets/ed198f7b-32d7-4a57-9298-7fa7144f970c

   ### 🌐 Frontend Input

  <img width="1903" height="857" alt="Image" src="https://github.com/user-attachments/assets/69cd2350-8f11-4aaf-bbc1-77c6baa89957" />

   ### After clicking "Predict":
   ### 📤 Backend Output

 <img width="1908" height="611" alt="Image" src="https://github.com/user-attachments/assets/679a6be7-90fe-46ce-9de7-933ec229a1a2" />

   ### 🔎 Frontend Output

   <img width="1912" height="863" alt="Image" src="https://github.com/user-attachments/assets/05da05d6-afbc-4f7f-bb2b-caf7a38e8e02" />
  
   ### 📊 Each Model Accuracy 
   
   | Signal Type | Model Used                          | Accuracy                                  |
   |-------------|-------------------------------------|-------------------------------------------|
   | ECG         | CNN                                 | 93.32%                                    |
   | PPG         | Random Forest                       | 96%                                       |
   | PCG         | BiLSTM                              | 96%                                       |

   

<p align="center">!!! THANK YOU !!!</p>
