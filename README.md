# housepricingpred

### Software and Tools Requirements

1. [Git and Github]

Create a new environment

```
conda create -p venv python==3.13.3 -y

```

# House Pricing Prediction API

This project is a simple Flask API for predicting house prices from given house features. It utilizes a pre-trained regression model and a scaler for data preprocessing.

## Endpoints

### Home Page Endpoint
- **URL:** `/`
- **Method:** GET
- **Description:** 
  - Serves the homepage by rendering the `home.html` template.
- **Response:**
  - HTML content displayed in the browser.

### Prediction API Endpoint
- **URL:** `/predict_api`
- **Method:** POST
- **Description:**
  - Accepts a JSON payload containing house features.
  - Transforms the input using a scaler and returns a prediction from the regression model.
- **Request JSON Format:**
  ```
  {
    "data": {
      "feature1": value,
      "feature2": value,
      "...": "..."
    }
  }
  ```
- **Response:**
  - JSON response with the predicted house price.
- **Example Request:**
  ```
  {
    "data": {
      "square_feet": 1500,
      "bedrooms": 3,
      "bathrooms": 2
    }
  }
  ```
- **Notes:**
  - Input features are scaled using the pre-loaded scaling model (`scaling.pkl`).
  - Predictions are generated using the regression model (`regmodel.pkl`).

## Running the Application

1. Ensure Python and all required packages are installed.
2. Start the Flask server:
   ```
   python app.py
   ```
3. Access the home page at [http://localhost:5000/](http://localhost:5000/).

Happy coding!