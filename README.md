Fake News Detection

Overall Worflow
Phase I - Model Training
1) Use datasets of Real and Fake News to train models with different algorithms:
    Logistic Regression
    Decision Treehem through
    Gradient Boosting
    Random Forest
2) Save the trained models as files, using joblib (a python library). This will allow us to use the models for prediction without having to go through the training part again and again. Also, these would be used in the backend logic, as whenever a user sends a news text to be classfied, it would be quite inefficent to train the model and then generate the response, each time!
3) Once the model files have been generated, we now proceed to using them through a webapp.

Phase II - Web App Creation, Model Integration, and Data Storage
 Our web app is quite simple in terms of functionality:
    i) Take news text and the model to be used as input from the user
    ii) Receive it at the backend
    iii) Pre-processit as required to bne able to feed it as input to the model
    iv) Use the respective pretrained model according to the user's input
    v) Generate the required result and send it to the user
    vi) Save the prediction in the database for future training

Tech Stack:
Frontend - Streamlit (a python based frontend library for creating frontends)
Backend - Flask (a python based framework for making backends)
Database - MongoDB (a NoSQL based Database. It stores data in the form key-value paris, much like the JSON format. Different from SQL based Databases, which store data in the form of tables. Easier to setup, configure, manage and integrate for beginners.)


Project Setup Flow

    Install Conda

    Run the following commands in the root directory of the project:
    conda env create -f environment.yml
    conda activate fake-news


    CD into the frontend folder(to start the frontend server)
    cd Frontend
    streamlit run frontend.py

    In a new terminal, CD into the backend folder (to start the backend server. Also, make sure that the fake-news virtual environemnt is active)
    cd Backend
    python app.py

    The frontend and backend would now be connected
    The database and model part would already be activated once the backend
    
     (Make sure that only one terminal is running corresponding to the Frontend and Backend Servers, as the port numbers are hard-coded. So, if one server is already running on a part, it can't run again in a different terminal unless the previous terminal is killed.)