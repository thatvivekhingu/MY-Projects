# Recipe Gemini App

This project is a web application that recommends recipes based on user-provided ingredients, dietary preferences, course types, and regions. It utilizes the Gemini API to generate image descriptions for the recommended recipes.

## Project Structure

```
recipe-gemini-app
├── models
│   ├── recipe_names.pkl          # Serialized list of recipe names for recommendations
│   ├── tfid_ingredients.pkl      # TF-IDF model for ingredient features
│   ├── tfid_diet.pkl             # TF-IDF model for dietary features
│   ├── tfid_course.pkl           # TF-IDF model for course features
│   ├── tfid_region.pkl           # TF-IDF model for regional features
│   └── input_features.npz        # Sparse matrix of input features for similarity calculations
├── templates
│   └── index.html                # HTML template for the web application's home page
├── static
│   └── style.css                 # CSS styles for the web application
├── app.py                        # Main application file with Flask setup and recipe recommendation logic
├── requirements.txt              # List of dependencies required for the project
└── README.md                     # Documentation for the project
```

## Setup Instructions

1. **Clone the repository:**
   ```
   git clone <repository-url>
   cd recipe-gemini-app
   ```

2. **Install dependencies:**
   It is recommended to use a virtual environment. You can create one using:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
   Then install the required packages:
   ```
   pip install -r requirements.txt
   ```

3. **Run the application:**
   Start the Flask application by running:
   ```
   python app.py
   ```
   The application will be accessible at `http://127.0.0.1:5000/`.

## Usage

- Navigate to the home page of the application.
- Input the ingredients, dietary preferences, course type, and region in the provided form.
- Submit the form to receive recipe recommendations along with generated image descriptions.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.