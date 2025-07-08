
# NYC Airbnb Price Prediction Project

## 📄 Project Overview

This project focuses on analyzing and predicting Airbnb listing prices in New York City using machine learning. The dataset was sourced from [Inside Airbnb](http://insideairbnb.com/get-the-data/) and includes information such as listing locations, room types, availability, and more. Our goal is to:

* Clean and prepare the data for modeling
* Build and evaluate an ML model (XGBoost)
* Visualize predicted vs. actual prices on an interactive map
* Provide business insights, such as pricing trends by borough or neighborhood

---

## 📊 Dataset
### 🗂️ Data Used

* `listings.csv`: Contains listing-level data (host, price, neighborhood, room type, etc.)
* `calendar.csv`: Availability and pricing data per day per listing
* `reviews.csv`: Reviews and their timestamps

---

## 📚 Project Workflow

### 1. **Data Cleaning**

* Removed unnecessary columns (e.g., IDs, URLs)
* Handled missing values in columns like price, bedrooms, bathrooms
* Removed outliers (e.g., listings with price > \$10,000 or bedrooms > 50)
* Converted relevant columns to numeric data types

### 2. **Feature Engineering**

* Selected useful features: `latitude`, `longitude`, `neighbourhood_group`, `room_type`, `availability_365`, `number_of_reviews`, `minimum_nights`
* One-hot encoded categorical variables like room type and borough

### 3. **Model Preparation**

* Defined the target variable: `price`
* Performed a train/test split (80/20)

### 4. **Model Training: XGBoost**

* Used the XGBoost Regressor model
* Tuned parameters like `max_depth`, `learning_rate`, and `subsample`
* Evaluated using metrics:

  * Mean Absolute Error (MAE)
  * Root Mean Squared Error (RMSE)
  * R-squared (R^2)

### 5. **Interactive Map**

* Used `folium` to create an interactive NYC map
* Each marker displays:

  * Actual price
  * Predicted price
  * Room type
  * Borough
* Clustering used to reduce clutter

---

## 📈 Highlights & Business Insights

* Accurately predicted Airbnb prices based on neighborhood, room type, and availability
* Identified price inconsistencies and potential under/overpriced listings
* Showed pricing distribution across boroughs (e.g., Manhattan vs. Brooklyn)
* Map can help hosts, guests, or analysts better understand local price trends

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy, Matplotlib
* Scikit-learn
* XGBoost
* Folium (interactive maps)
* Jupyter Notebook

---
## Project Visualizations

Perfect! You've uploaded the images correctly to your GitHub repo. Now here’s the exact Markdown code to paste at the **end of your `README.md`** so that both screenshots display inline:

---

### 📊 Visualizations

#### 🏙️ Predicted vs Actual Airbnb Prices in NYC

![Predicted Prices](https://github.com/munalen123/ML-Airbnb-project-1-/blob/main/Screenshot%202025-07-06%20164134.png-predict%20price.png?raw=true)

#### 📌 Airbnb Listing Density Across NYC

![Listing Amount](https://github.com/munalen123/ML-Airbnb-project-1-/blob/main/Screenshot%202025-07-06%20164200.png-listamount.png?raw=true)

---

✅ **Make sure to include the `?raw=true` at the end** so GitHub renders the images in the README file.

Let me know once it's added and I can check how it looks!

---

## 🙌 Acknowledgements

* Dataset: [Inside Airbnb](http://insideairbnb.com/get-the-data/)
* Inspired by the NYC Open Data community and Airbnb analytics projects
