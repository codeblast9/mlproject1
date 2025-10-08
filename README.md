Student Exam Performance Prediction
This is an end-to-end Machine Learning project that predicts a student's performance in their Math exam based on a number of social and academic factors. The project includes a full data processing and model training pipeline, and a web application built with Flask to serve the model's predictions.

Features
Data Ingestion & Transformation: A robust pipeline for cleaning and preparing the data for training.

Model Training: Trains a regression model to predict math scores and saves the model artifacts.

Prediction Pipeline: Loads the saved model to make predictions on new, unseen data.

Web Interface: A user-friendly web application built with Flask and Bootstrap that allows users to input student details and receive a real-time prediction.

Project Structure
The project follows a modular structure to ensure scalability and maintainability.

├── artifacts/              <-- Stores the trained model and preprocessor files
│   ├── model.pkl
│   └── preprocessor.pkl
├── src/                    <-- Source code for the project
│   ├── components/         <-- Code for each stage of the pipeline (ingestion, training, etc.)
│   ├── pipeline/           <-- Manages the training and prediction pipelines
│   ├── exception.py        <-- Custom exception handling
│   └── utils.py            <-- Utility functions (e.g., loading objects)
├── templates/              <-- HTML files for the web application
│   └── home.html
├── app.py                  <-- Flask application script
└── requirements.txt        <-- Required Python libraries

How to Run
Follow these steps to set up and run the project on your local machine.

Step 1: Clone the Repository
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name

Step 2: Create a Virtual Environment and Install Dependencies
It is highly recommended to use a virtual environment.

# Create the environment
python -m venv venv

# Activate it (Windows)
venv\Scripts\activate

# Activate it (macOS/Linux)
source venv/bin/activate

# Install the required libraries
pip install -r requirements.txt

Step 3: Run the Training Pipeline
This is a critical first step. You must train the model before you can run the prediction server. This command will generate the artifacts folder with your trained model.

python src/pipeline/train_pipeline.py

After this command finishes, you should see model.pkl and preprocessor.pkl inside a new artifacts folder.

Step 4: Run the Flask Application
Once the model artifacts are created, you can start the web server.

python app.py

Open your web browser and navigate to http://127.0.0.1:5000 to see the application live.

Technologies Used
Backend: Flask

ML/Data Science: Pandas, NumPy, Scikit-learn

Frontend: HTML, Bootstrap
