

#MOVIE RECOMMENDER SYSTEM

This repository contains a simple Movie Recommender System developed using a Content-Based Filtering approach.

The project is structured into two main parts: the machine learning model development and the web application interface.

CORE TECHNOLOGIES

Python

Data Processing and Model Building: Pandas, Numpy, Scikit-learn 

Web Application: Streamlit

Data Source: TMDB 5000 Movie Dataset

PROJECT COMPONENTS

MOVIE RECOMMENDER SYSTEM DOT IPYNB
This Jupyter Notebook contains all the steps for developing the content-based recommendation model.

Data Collection and Merging: Merging movie metadata and credits.

Feature Engineering and Preprocessing: Extracting relevant features like genres keywords cast and director. Data cleaning and stemming are applied to create a unified 'tags' feature.

Model Training: Using Cosine Similarity on vectorized data to calculate the closeness between movies based on their tags. This produces the similarity matrix used for recommendations.

Persistence: The processed movie data dictionary and the similarity matrix are saved as pickle files (movie_dict and similarity.pkl) for use in the web application.

APP DOT PY
This Python script uses Streamlit to create an interactive web application for the recommender system.

Functionality: Users can select a movie from a dropdown list.

Recommendation: When the 'Recommend' button is clicked the app uses the precomputed similarity matrix to suggest the top 5 similar movies.

External API Integration: The app uses the TMDB API to fetch and display the official movie posters for the recommendations.

HOW TO RUN THE PROJECT

The model development is fully contained in the notebook. To run the web application locally you will need the generated pickle files.

Install Dependencies: Install the necessary Python packages including streamlit pandas and scikit-learn.

Run the App: Execute app dot py using streamlit run app dot py in your terminal.

Access the App: The application will open in your web browser where you can test the recommender system.
