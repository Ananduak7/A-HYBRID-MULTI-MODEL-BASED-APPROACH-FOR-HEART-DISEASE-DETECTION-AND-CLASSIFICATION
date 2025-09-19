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
  <img src="https://github.com/user-attachments/assets/bbb2f416-0bf0-496b-8665-8f5323fc3fd0" alt="App Screenshot" width="100%">
</p>
    
   ### 🚀 User Interface Video
   
   https://github.com/user-attachments/assets/ed198f7b-32d7-4a57-9298-7fa7144f970c

   ### 🚀 Starting Backend 

   ![Image](https://github.com/user-attachments/assets/c5014288-6344-4c36-9472-43d8d5777917)

   ### 🌐 Frontend Input

   ![Image](https://github.com/user-attachments/assets/88888667-dc1c-4ab0-90ab-febbff4c48c8)

   ### After clicking "Predict":
   ### 📤 Backend Output

   ![Image](https://github.com/user-attachments/assets/153c1f93-d2b1-44c2-8a4e-9978d76578c8)

   ### 🔎 Frontend Output

   ![Image](https://github.com/user-attachments/assets/a60c5484-a2f6-402a-9bc6-e65c2929ffc2)
  
   ### 📊 Each Model Accuracy 
   
   | Signal Type | Model Used                          | Accuracy                                  |
   |-------------|-------------------------------------|-------------------------------------------|
   | ECG         | CNN                                 | 93.32%                                    |
   | PPG         | Random Forest                       | 96%                                       |
   | PCG         | BiLSTM                              | 96%                                       |

   

<p align="center">!!! THANK YOU !!!</p>
