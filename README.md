### Student Exam Performance Predictor<br>

- Project Overview:<br>
The Student Exam Performance Predictor is an end-to-end machine learning project designed to predict student's math scores based on various factors such as reading and writing scores, gender, race/ethnicity, parental education level, lunch type, and test preparation course. The project follows a modular approach, ensuring scalability, maintainability, and ease of deployment.<br>

- Key Features:<br>
  - Graphical User Interface: The project contains a user-friendly interface (GUI) that allows users to input student data and obtain grade predictions through an interactive and intuitive interface.
  - Data Processing Pipeline: Automates data ingestion, transformation, and model training.<br>
  - Multiple Regression Models: Trains models like Random Forest, Decision Tree, Gradient Boosting, XGBoost, CatBoost, AdaBoost, and Linear Regression.<br>
  - Best Model Selection: Uses R² score to choose the most accurate model.<br>
  - Custom Exception Handling: Implements structured error handling for debugging.<br>
  - Modular Code Design: Separates components for easy maintenance.<br>
  - Scalable & Reproducible: Easily extendable for new data and model improvements.<br>

- Steps performed by code:Student Exam Performance Predictor is a tool that uses multiple regression models like Random Forest, Decision Tree, Gradient Boosting, XGBoost, CatBoost, AdaBoost, and Linear Regression to predict the Maths grade of a student based on various features like reading and writing scores, gender, race/ethnicity, parental education level, lunch type, and test preparation course. The model is trained on a dataset containing student information, and the user can input values for above features through an interactive Graphical User Interface (GUI) to obtain the predicted Maths grade for a new student.<br>

The predictor uses one-hot encoding for categorical variables and is trained on a dataset that is preprocessed to handle missing values or categorical variables.<br>

  1.  Data Loading: The code reads the "notebook\data\stud.csv" file, which contains the student data, using the pandas library. The data is loaded into a DataFrame for further processing. Refer "src\components\data_ingestion.py" for relevant code.<br>

  2.  Data Preprocessing: The dataset may have missing values or categorical variables that need handling. Refer "src\components\data_transformation.py". The code preprocesses the data, converting categorical variables into numerical form using one-hot encoding. This transformation is necessary because most machine learning algorithms, including Linear Regression, require numerical inputs.<br>

  3.  Data Splitting: The data is split into training and testing sets using the train_test_split() function from sklearn. This ensures that the model is trained on a subset of the data and evaluated on unseen data to assess its generalization performance.<br>

  4.  Model Training: Data is trained using multiple models stated above using the fit() method. Refer "src\components\model_trainer.py" Also, hyperparameter tuning is done to optimize the performance of a machine learning model by finding the best set of hyperparameters using GridSearchCV(). The model aims to learn the relationships between the features and the target variable (Maths grade).<br>

  5.  Model Evaluation: After training, the model's performances are evaluated using the test data using R-squared (R2). R2 indicates how well the model explains the variance in the target variable. Best model is chosen based on bigger R2. Refer "src\components\model_trainer.py" & "src\utils.py"<br>

  6.  Example Prediction with GUI: The code features an interactive GUI that allows users to input above features for a new student. The best suited model will then predict their Maths score based on these inputs, providing a convenient and user-friendly way to utilize the predictor.<br>

- Dataset Information:<br>
  - Kaggle Link: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977<br>
  - Feature	Description-<br>
      - gender: Gender of the student<br>
      - race_ethnicity: Ethnic group of the student<br>
      - parental_level_of_education:	Parent's highest education level<br>
      - lunch:	Type of lunch (standard/free)<br>
      - test_preparation_course:	Whether the student completed a prep course<br>
      - math_score:	(Target Variable) Student's math test score<br>
      - reading_score:	Student's reading test score<br>
      - writing_score:	Student's writing test score<br>

- Tools and Technologies:<br>
  - Tools: Visual Studio Code, GitHub
  - Programming Languages: Python, HTML, CSS
  - Libraries: Numpy, Pandas, scikit-learn, 
  - Framework: Flask

