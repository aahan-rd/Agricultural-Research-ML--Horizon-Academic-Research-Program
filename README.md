# Agricultural Prediction  
### A Machine Learning-Based Advisory Platform for Farmers  

**Horizon Academic Research Program | May 2024 – July 2024**  
Mentored by Dr. Maria Konte, Research Professor, Georgia Institute of Technology  

---

## Project Overview

This project develops a data-driven agricultural advisory platform designed to assist farmers in making informed decisions about crop selection and yield expectations.

The system integrates machine learning models into a Flask-based web interface that allows users to input farm-specific parameters and receive:

- Crop recommendations  
- Yield predictions  
- Access to historical agricultural visualizations  

The objective is to provide accessible decision-support tools for farmers, particularly in developing markets where access to agricultural analytics may be limited.

---

## Core Functionality

The platform implements two machine learning models.

### 1. Crop Recommendation Model  
**Model Type:** Decision Tree Classifier  

**Input Features:**
- Nitrogen (N)  
- Phosphorus (P)  
- Potassium (K)  
- Temperature  
- Humidity  
- Rainfall  

**Output:**
- Recommended crop type  

The decision tree model was selected for its interpretability and ability to capture nonlinear relationships between environmental factors and crop suitability.

---

### 2. Yield Prediction Model  
**Model Type:** Linear Regression  

**Input Features:**
- Soil nutrient composition  
- Temperature  
- Humidity  
- Rainfall  

**Output:**
- Predicted crop yield (continuous value)  

Linear regression was used to model quantitative relationships between environmental variables and expected yield.

---

## Datasets Used

### Global Agricultural Production Data
- Area harvested  
- Yield  
- Production  
- Import/export quantities and values  
- Year and country identifiers  

Source: Food and Agriculture Organization (FAOSTAT)  
https://www.fao.org/faostat/en/#data  

---

### India Crop Production Dataset
- State  
- District  
- Season  
- Crop type  
- Land used  
- Amount produced  

Source:  
https://www.kaggle.com/datasets/abhinand05/crop-production-in-india  

---

### Climate Data
- Annual and seasonal temperature data  
- Rainfall  
- Humidity  

Sources:
- https://data.gov.in  
- https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data  

---

### Soil and Nutrient Dataset
- Nitrogen  
- Phosphorus  
- Potassium  
- pH  
- Crop label  

Source:  
https://www.kaggle.com/code/ashwanikumar07/crop-recommendation/notebook  

---

## Data Analysis and Visualization

The platform includes visual analytics for exploratory data analysis and model evaluation, including:

- Time series plots of crop production across years  
- Boxplots summarizing yearly production distributions  
- Import vs. export comparisons  
- Country-level production overlays  
- Correlation plots between environmental variables and yield  
- Predicted vs. actual comparison graphs  
- ROC curve visualization for classifier performance  
- Confusion matrix and classification report outputs  

Visualization tools used:
- Pandas  
- Matplotlib  
- Plotly  

---

## Model Evaluation

### Decision Tree Classifier
- Confusion Matrix  
- Classification Report  
- ROC Curve  

### Linear Regression
- Predicted vs. Actual Plot  
- Error analysis  
- Model accuracy metrics  

---

## Technology Stack

### Programming and Machine Learning
- Python  
- Pandas  
- NumPy  
- scikit-learn  
- matplotlib  
- Plotly  

### Web Framework
- Flask  
- HTML templates  

---

## Implementation Details

The workflow consists of:

1. Data collection and cleaning  
2. Exploratory data analysis  
3. Model training and validation  
4. Performance evaluation  
5. Integration into a Flask web application  

The models are trained offline and exposed through a web interface for user interaction.

---

## Challenges and Resolutions

### Low Decision Tree Accuracy
Initial model performance was poor due to dataset inconsistency and class imbalance.

**Resolution:**
- Switched to a cleaner dataset  
- Analyzed class distribution  
- Applied class-balanced train/test splitting  

This significantly improved classification performance.

---

### Extracting Targeted Data from Large Datasets
Filtering country-specific and crop-specific records required structured selection methods.

**Resolution:**
- Advanced Pandas filtering  
- Conditional indexing  
- Vectorized operations instead of nested loops  

---

## Limitations

- Decision tree occasionally produces ambiguous outputs for closely related crop classes.  
- Some visualizations currently open in separate windows rather than being fully embedded in the web interface.  
- Real-time environmental data integration is not yet implemented.  

---

## Future Work

- Integration of both ML models into a conversational interface  
- Deployment as a cloud-hosted public application  
- WhatsApp-based advisory interface for broader accessibility  
- Real-time climate API integration  
- Enhanced UI/UX refinement  

---

## How to Run the Project

1. Install Python (latest version recommended).  
2. Install required libraries:

