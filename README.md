# 🍽️ Restaurant Consumer Behaviour & Ratings Analysis Dashboard (Power BI)

## 📌 Project Overview

This Power BI dashboard analyzes restaurant performance, consumer behavior, dining preferences, hospitality services, and customer ratings across multiple cities and states.

The project provides insights into consumer demographics, restaurant facilities, dining preferences, alcohol and smoking policies, and customer satisfaction levels through interactive visualizations.

---

# 📊 Dashboard Pages

## 🏠 Page 1: Home Dashboard

### KPI Cards

* Total Restaurant Count
* Total Cuisines
* Total Consumers
* Total Cities
* Total States

### Visualizations

#### 1. Consumers by City and State

* Chart Type: Clustered Bar Chart
* Y-Axis: State
* X-Axis: Count of Consumer ID
* Legend: City

#### 2. Smoking Rates by City

* Chart Type: Bar Chart
* Y-Axis: City
* X-Axis: Consumer Count
* Legend: Smoking Rate

#### 3. Consumers by Age Group and State

##### Age Group DAX Column

```DAX
Age Group =
SWITCH(
    TRUE(),
    consumers[Age] <= 18, "Children and Adolescents",
    consumers[Age] <= 30, "Young Adults",
    consumers[Age] <= 45, "Adults",
    consumers[Age] <= 60, "Middle-aged Adults",
    "Seniors"
)
```

* Chart Type: Bar Chart
* Y-Axis: State
* X-Axis: Count of Consumers
* Legend: Age Group

#### 4. Parking Availability by Restaurant and City

* Chart Type: Bar Chart
* Y-Axis: City
* X-Axis: Count of Restaurant ID
* Legend: Parking

---

# 🍴 Page 2: Dining Dashboard

### 1. Marital Status Distribution

* Chart Type: Treemap
* Category: Marital Status
* Values: Count of Marital Status

### 2. Franchise Distribution

* Chart Type: Treemap
* Category: Franchise
* Values: Count of Franchise

### 3. Restaurant Price Distribution

* Chart Type: Treemap
* Category: Price
* Values: Count of Price

### 4. Restaurant Parking Analysis

* Chart Type: 100% Stacked Area Chart
* X-Axis: Parking
* Y-Axis: Count of Restaurant ID
* Legend: Price

### 5. Franchise vs Non-Franchise Restaurant Ratings

#### Overall Rating Category

```DAX
Overall Rating Category =
SWITCH(
    TRUE(),
    ratings[Overall_Rating] = 0, "Unsatisfactory",
    ratings[Overall_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

* Chart Type: Pie Chart
* Legend: Overall Rating Category
* Values: Count of Restaurant ID
* Details: Franchise

### 6. Restaurant Distribution by State

* Chart Type: Pie Chart
* Legend: State
* Values: Count of Restaurant ID

### 7. Top Preferred Cuisine by Consumers

* Chart Type: Bar Chart
* X-Axis: Preferred Cuisine
* Y-Axis: Count of Consumer ID

---

# 🍷 Page 3: Hospitality Dashboard

### 1. Alcohol Service by Restaurant and City

* Chart Type: Donut Chart
* Legend: Alcohol Service
* Values: Count of Restaurant ID
* Details: City

### 2. Transportation Preferences by City

* Chart Type: Bar Chart
* X-Axis: Transportation
* Y-Axis: Count of Consumer ID

### 3. Restaurant Smoking Policies

* Chart Type: Treemap
* Category: Smoking Allowed
* Values: Count of Restaurant ID
* Details: State

### 4. Alcohol Service Impact on Ratings

* Chart Type: Column Chart
* X-Axis: Alcohol Service
* Y-Axis: Count of Consumer ID
* Legend: Overall Rating Category

---

# 👥 Page 4: Consumer Behaviour Dashboard

### 1. Occupation of Consumers by State

* Chart Type: Bar Chart
* X-Axis: Count of Consumer ID
* Y-Axis: State
* Legend: Occupation

### 2. Marital Status vs Smoker and Drinker

#### Combined Column

```DAX
Smoker & Drinker =
consumers[Smoker] & "-" & consumers[Drink_Level]
```

* Chart Type: Bar Chart
* X-Axis: Count of Consumer ID
* Y-Axis: Smoker & Drinker
* Legend: Marital Status

### 3. Drink Level by State

* Chart Type: Bar Chart
* X-Axis: Count of Consumer ID
* Y-Axis: State
* Legend: Drink Level

### 4. Occupation vs Budget Levels

* Chart Type: Bar Chart
* X-Axis: Occupation
* Y-Axis: Count of Consumer ID
* Legend: Budget

---

# ⭐ Page 5: Review Dashboard

### 1. Top 5 Restaurants by Food Rating

#### Food Rating Category

```DAX
Food Rating Category =
SWITCH(
    TRUE(),
    ratings[Food_Rating] = 0, "Unsatisfactory",
    ratings[Food_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

* Chart Type: Bar Chart
* X-Axis: Restaurant Name
* Y-Axis: Count of Restaurant ID
* Legend: Food Rating Category

### 2. Top 5 Restaurants by Service Rating

#### Service Rating Category

```DAX
Service Rating Category =
SWITCH(
    TRUE(),
    ratings[Service_Rating] = 0, "Unsatisfactory",
    ratings[Service_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

* Chart Type: Bar Chart
* X-Axis: Restaurant Name
* Y-Axis: Count of Restaurant ID
* Legend: Service Rating Category

### 3. Overall Rating Analysis

#### Overall Rating Category

```DAX
Overall Rating Category =
SWITCH(
    TRUE(),
    ratings[Overall_Rating] = 0, "Unsatisfactory",
    ratings[Overall_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

* Chart Type: Matrix
* Rows: Restaurant Name
* Columns: Overall Rating Category
* Values: Overall Rating

---

# 🛠 Tools Used

* Power BI Desktop
* DAX
* Power Query
* Data Modeling
* Interactive Dashboard Design

---

# 📈 Key Insights

* Consumer demographics vary significantly across states and cities.
* Smoking and drinking habits influence restaurant preferences.
* Franchise and non-franchise restaurants exhibit different rating patterns.
* Alcohol service and parking facilities impact customer satisfaction.
* Food and service ratings help identify top-performing restaurants.

---

## 🚀 Author

**Yash Srivastava**

MBA (Business Analytics) | Data Analyst

Skills: Power BI • SQL • Excel VBA • Python • Salesforce CRM • Data Visualization
