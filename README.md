![Screenshot (919)](https://github.com/moodle12/odoo_hackathon_2024/assets/103280407/affb5a9e-fb08-49a2-925f-ebdef1687964)
![Screenshot (921)](https://github.com/moodle12/odoo_hackathon_2024/assets/103280407/e29df6fb-a730-4bb6-b94b-e2241fd71f58)

# Diet Recommendation System


## A diet recommendation web application using content-based approach with Scikit-Learn, FastAPI and Streamlit.

## Model developement
The recommendation engine is built using Nearest Neighbors alogrithm which is an unsupervised learner for implementing neighbor searches. It acts as a uniform interface to three different nearest neighbors algorithms: BallTree, KDTree, and a brute-force algorithm based on routines in sklearn.metrics.pairwise. For our case, we used the brute-force algorithm using cosine similarity due to its fast computation for small datasets.


## Dataset
We used Food.com kaggle dataset Data with over 500,000 recipes and 1,400,000 reviews from Food.com. Visit this [kaggle](https://www.kaggle.com/datasets/irkaal/foodcom-recipes-and-reviews?select=recipes.csv) link for more details.

## Backend Developement
The application is built using the FastAPI framework, which allows for the creation of fast and efficient web APIs. When a user makes a request to the API (user data,nutrition data...) the model is used to generate a list of recommended food similar/suitable to his request (data) which are then returned to the user via the API.

## Frontend Developement
The application's front-end is made with Streamlit. Streamlit is an open source app framework in Python language. It helps to create web apps for data science and machine learning in a short time. It is compatible with major Python libraries such as scikit-learn, Keras, PyTorch, SymPy(latex), NumPy, pandas, Matplotlib etc.
For our case the front-end is composed of three web pages. The side bar on the left allows the user to navigate too the automatic diet recommendation page and the custom food recommendation page.
In the diet recommendation page the user can fill information about his age,weight,height.. and gets a diet recommendation based on his information. Besides, the custom food recommendation allows the user to specify more his food preferency using nutritional values.

## Deployement using Docker
Why Docker?
By using Docker, we can ensure that the environment in which the application is exactly the same as the environment in which it was built, which can help prevent unexpected issues and improve model performance.
Additionally, Docker allows for easy scaling and management of the deployment, making it a great choice for larger machine learning projects.

## Docker-Compose
Our project is composed of different services (frontend,API). Therefore, our application should run on multiple containers.
With the help of Docker-compose we can share our application using the yaml file that define the services that runs together.


## Technologies
The project is created with:

Python: 3.10.8

fastapi 0.88.0

uvicorn 0.20.0

scikit-learn 1.1.3

Pandas: 1.5.1

Streamlit: 1.16.0

streamlit-echarts 1.24.1

Numpy: 1.21.5

beautifulsoup4 4.11.1
