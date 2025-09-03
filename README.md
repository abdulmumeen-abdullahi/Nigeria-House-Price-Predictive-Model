# Nigeria House Price Predictive Model
## Overview of the Problem

The rapid growth of the luxury real estate market in Nigeria has created significant challenges for realtors in determining the right pricing for houses. Various factors such as house type, location (state), number of bedrooms, bathrooms, toilets, and parking spaces play a crucial role in shaping the house's value. Mispricing properties can result in lost revenue or decreased sales.
This project aims to develop a predictive model that estimates house prices accurately, enabling realtors to make informed pricing decisions and optimize revenue opportunities.

## Data Used

The dataset used in this project represents the pricing details of houses in Nigeria, sourced from a dataset of Nigerian housing data on [Kaggle](https://www.kaggle.com/datasets/abdullahiyunus/nigeria-houses-and-prices-dataset). The dataset includes the following columns: <br/>
•	Bedrooms: Number of bedrooms in the house. <br/>
•	Bathrooms: Number of bathrooms in the house. <br/>
•	Toilets: Number of toilets in the house. <br/>
•	Parking Space: Number of parking spaces available. <br/>
•	Title: The type of house (e.g., Detached Duplex, Semi-Detached Duplex, etc.). <br/>
•	State: State where the house is located. <br/>
•	Price: Price of the house in NGN (Nigerian Naira), measured in millions. <br/>
For this project, the dataset was preprocessed to scale price values by a factor of 1,000,000, which converts the prices into millions of NGN.

## Methodology

### 1.	Data Preprocessing <br/>
o	The dataset was loaded into a pandas DataFrame and unnecessary columns were removed. <br/>
o	A new column, price_millions, was created by dividing the price column by one million. <br/>
o	The dataset was filtered to include houses with a price between 10 and 300 million NGN, with specific apartment types (Detached Duplex, Semi-Detached Duplex, etc.), and excluding houses from Anambra state.

### 2.	Exploratory Data Analysis (EDA) <br/>
o	A correlation matrix was computed to analyze relationships between the numerical features and the target variable (price_millions). <br/>

![download](https://github.com/user-attachments/assets/802edbaa-9aba-4a7f-91d4-1ad127d48a94)

o	A heatmap was generated to visualize these correlations, with bedrooms having the strongest correlation with price (0.44), followed by toilets (0.39), bathrooms (0.35), and parking spaces (0.12).

### 3.	Model Training <br/>
o	The data was split into training (80%) and testing (20%) sets. <br/>
o	A baseline model was established by calculating the mean value of price_millions and using it as a prediction for all test data points. The Mean Absolute Error (MAE) was calculated as the benchmark. <br/>
o	Categorical columns (house type and state) were encoded using OneHotEncoder.

### 4.	Model Selection and Evaluation <br/>
Several machine learning models were trained and evaluated, including: <br/>
	Random Forest Regressor (chosen for its robustness and accuracy). <br/>
	Linear Regression. <br/>
	Decision Tree Regressor. <br/>
	Hyperparameter tuning was applied, and the MAE was calculated for each model. The Random Forest Regressor achieved the lowest MAE, outperforming other models with an error of 38.1 Million NGN.

![download](https://github.com/user-attachments/assets/3495c24c-fa6d-4a29-a9b7-72ac302f4b30)

### 5.	Feature Importance <br/>
•	Extracted and visualized the top 5 features using a bar chart. <br/>
•	Insights: bathrooms emerged as the most critical predictor.

### 6.	Interactive Dashboard <br/>
1.	An interactive dashboard was created using ipywidgets, allowing users to input various house attributes (e.g., apartment type, state, number of bedrooms, etc.) through sliders and dropdown menus. <br/>
2.	The predict_price function was used to return the predicted price based on user inputs, offering a user-friendly interface to explore the model’s predictions.

![Nigeria House Price Predictive Model](https://github.com/user-attachments/assets/c749c965-b94d-4122-b45a-6eb3404fdcab)

## Results <br/>
•	Benchmark (Baseline) Model: The baseline model, which predicts the mean value of the target variable, had an MAE of 50.23 Million NGN. <br/>
•	Random Forest Regressor: The Random Forest model achieved an MAE of 38.1 Million NGN, outperforming the baseline by 12.13 Million NGN, indicating its superior performance.

## How the Model Can Help Businesses <br/>
This house price prediction model can significantly assist realtors and investors in optimizing their pricing strategies. By leveraging this model, businesses can: <br/>
•	Make data-driven pricing decisions. <br/>
•	Reduce inventory costs by ensuring accurate pricing. <br/>
•	Improve customer trust with transparent and reliable price estimates. <br/>
•	Identify market trends and minimize financial risks. <br/>
By adopting this predictive tool, real estate companies can stay ahead of the competition, increase profitability, and provide exceptional customer service.

## Conclusion
This project demonstrates how machine learning models, such as Random Forest Regressor, can effectively predict house prices in Nigeria based on various features like apartment type, state, and amenities. Though the model serves as a personal project to showcase data science skills, it holds potential for businesses to optimize pricing strategies in the real estate sector. <br/>
For more robust and tailored predictions, feel free to contact me for personalized services.

Abdullahi Olalekan Abdulmumeen <br/>
Applied Data Scientist <br/>
Olalekanabdulmumeen3@gmail.com <br/>
