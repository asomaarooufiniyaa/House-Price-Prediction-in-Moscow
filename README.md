# House Price Prediction in Moscow

This project aims to predict house prices in Moscow using Linear and Polynomial Regression. The dataset contains various features such as apartment type, region, renovation status, number of rooms, area, and metro station proximity.

## Dataset
The dataset (`data.csv`) contains:
- **Categorical features**: Apartment type, Region, Renovation, Metro station
- **Numerical features**: Minutes to metro, Number of rooms, Area, Living area, Kitchen area, Floor, Number of floors, Price

## Steps
1. **Data Cleaning & Preprocessing**
   - Removed duplicate rows
   - Checked for missing values
   - Encoded categorical variables using `LabelEncoder`
   - Created a new feature `Metro_Target` (average price per metro station)
   - Rearranged columns for better readability
   
2. **Exploratory Data Analysis (EDA)**
   - Used a heatmap to visualize correlations between features
   - Calculated Variance Inflation Factor (VIF) to detect multicollinearity
   - Plotted histogram for house prices

3. **Model Training & Evaluation**
   - **Linear Regression**
     - Trained a model using `Area` and `Metro_Target` as features
     - Evaluated using Mean Squared Error (MSE) and R-squared (R²) score
   - **Polynomial Regression (Degree=2)**
     - Transformed features using `PolynomialFeatures`
     - Trained a regression model and evaluated performance
   
4. **Results Visualization**
   - Scatter plots comparing actual vs. predicted prices for both models

## Requirements
To run the project, install the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```
##Usage

Run the Jupyter Notebook to preprocess the data, train models, and visualize results:

```bash
jupyter notebook moscow.ipynb
```

# Results
Polynomial regression showed better performance compared to linear regression in predicting house prices.

The correlation heatmap indicated a strong relationship between **Metro_Target** and **Price**.

# Future Improvements
Use more features for training (e.g., Living area, Kitchen area, Floor, etc.)

Experiment with other regression techniques like Decision Trees and Random Forest

Tune hyperparameters to improve prediction accuracy

# License
This project is licensed under the MIT License. See the **LICENSE** file for details.

Author: Aso  Maarooufiniyaa
