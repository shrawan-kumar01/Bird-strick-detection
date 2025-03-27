Bird Strike Detection
This project is designed to predict the damage caused by bird strikes in aviation based on various input parameters. It leverages machine learning to analyze historical data and predict the likelihood of damage based on flight and bird strike details. The application is built using Python, Streamlit, scikit-learn, and pandas.

Table of Contents
Overview

Technologies Used

Project Structure

How to Run the Application

Model Details

Data Description

License

Overview
The project includes a machine learning model that predicts the damage caused by bird strikes using a variety of input features. The goal is to provide an easy-to-use web application where users can input flight details and receive a prediction of potential damage from bird strikes.

The project consists of the following components:

Machine Learning Model: A Random Forest Classifier built to predict bird strike damage based on historical data.

Streamlit Application: A user-friendly interface that allows users to enter bird strike details and receive predictions in real-time.

Data Preprocessing and Model Evaluation: Code for training, evaluating, and tuning the model to ensure accuracy.

Technologies Used
Python: Programming language used for building the model and the Streamlit app.

Streamlit: Framework for creating the interactive web application.

Pandas: Library for data manipulation and cleaning.

scikit-learn: Machine learning library used for building and training the predictive model.

Matplotlib and Seaborn: Libraries used for plotting feature importance and other visualizations.

Label Encoding: Used to convert categorical data into numerical format for model training.

Project Structure
Here is the directory structure for the project:

bash
Copy code
/birdstrickDetection
    /notebooks
        ModelBuilder.py       # Contains the BirdStrikeModelBuilder class for model building and evaluation
    Bird_strikes.csv           # Dataset containing historical bird strike data
    app.py                    # Streamlit application file for user input and predictions
    requirements.txt          # Contains the list of dependencies required for the project
Key Files
ModelBuilder.py:

Contains the BirdStrikeModelBuilder class that is responsible for building, training, and evaluating the machine learning model.

The class uses Random Forest Classifier from scikit-learn to make predictions on bird strike damage.

Bird_strikes.csv:

The dataset containing historical bird strike data with various features such as AircraftType, AirportName, Altitude, WildlifeSpecies, etc.

The target variable is Damage, which is what the model is trained to predict.

app.py:

The main Streamlit app that takes user inputs, processes them, and makes predictions using the trained model.

It allows the user to input different parameters of a bird strike and provides a prediction for the damage based on the trained model.

requirements.txt:

Lists the dependencies required to run the application. It includes libraries like Streamlit, scikit-learn, pandas, etc.

How to Run the Application
To run the Streamlit app locally on your machine, follow these steps:

1. Clone the repository:
bash
Copy code
git clone <repository_url>
2. Set up a virtual environment:
Create and activate a virtual environment:

bash
Copy code
python -m venv venv
On Windows:

bash
Copy code
venv\Scripts\activate
On macOS/Linux:

bash
Copy code
source venv/bin/activate
3. Install dependencies:
Once the virtual environment is activated, install the required dependencies:

bash
Copy code
pip install -r requirements.txt
4. Run the Streamlit app:
Start the Streamlit app by running the following command:

bash
Copy code
streamlit run app.py
This will open a new browser window with the Streamlit app where you can input the parameters and get a prediction of the damage caused by bird strikes.

Model Details
The model used in this project is a Random Forest Classifier. It is trained on historical bird strike data to predict the damage caused by bird strikes in various aviation scenarios. The model is trained on the following features:

Aircraft Type

Airport Name

Altitude Bin

Make and Model

Number of Birds Struck

Effect of the Strike

Flight Date

Flight Phase (e.g., takeoff, cruise, landing)

Conditions such as precipitation, sky conditions, and more

The model predicts the level of damage caused by a bird strike based on the input parameters.

Data Description
The dataset used for training the model (Bird_strikes.csv) contains several columns of information regarding bird strikes, including:

RecordID: Unique identifier for the record.

AircraftType: Type of the aircraft involved in the strike.

AirportName: Name of the airport where the strike occurred.

AltitudeBin: Altitude range where the strike occurred.

MakeModel: Make and model of the aircraft.

NumberStruck: Number of birds struck.

Effect: The effect of the bird strike (e.g., engine damage, windshield break).

FlightDate: Date of the flight.

Engines: Number of engines on the aircraft.

Operator: Operator of the aircraft (e.g., airline name).

OriginState: State where the flight originated.

FlightPhase: Phase of the flight when the strike occurred.

ConditionsPrecipitation: Precipitation conditions at the time of the strike.

RemainsCollected?: Whether the remains of the bird were collected.

Damage: The target variable representing the level of damage caused by the strike (i.e., the variable that the model aims to predict).
