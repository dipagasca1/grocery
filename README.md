# Grocery App (Flask + SQLite)

This project presents a grocery inventory management application built using the **Grocery Inventory dataset**.  
The workflow includes data preprocessing, database creation, and the development of a Flask-based web application for visualizing and searching grocery items.

The application allows users to:
- Search grocery items by name.  
- View details such as category, supplier, stock quantity, and price.  
- Access clean and structured data stored in an integrated SQLite database.



## Dataset Information

![Grocery Logo](website/static/logogrocery.png)

Dataset Source (Kaggle):  
**[Grocery Inventory Dataset](https://www.kaggle.com/datasets/willianoliveiragibin/grocery-inventory?utm_source)**


### Step 1: Data Preprocessing

 **Corrected a Mistyped Column Name**  
 - Issue: The original dataset included a column labeled **‘Category’** with incorrect spelling.  
 - Action: Corrected the spelling to **‘Category’**.

 **Removed Null Values**  
 - Action: All rows containing null values were removed to ensure data consistency.

 **Saved the Updated Dataset**  
 - Output file created: `grocery_inventory.csv`


### Step 2: Database Creation

 The cleaned dataset is processed by `dataload.py` and
 loads the data into an SQLite database stored as `grocery.db`.


### Step 3: Developing the Web Application

 The Flask framework is used in `app.py` to build the web application.  
 The app includes the following routes:

 Note: `about.html` is the default landing page.

- **`/grocery`** - Opens the `search_grocery.html`, which provides a search button with product name.  
- **`/data`** - Opens the 'data.html' page with data that has been retrieved from the SQLite database.('grocery.db')

## HTML Pages Overview

### `about.html`
1. Header: **"Welcome to the Grocery App"**.  
2. Navigation buttons to **Grocery Search** and **Grocery Table**.  
3. Clickable URL link to the Kaggle dataset.
4. A description table explaining each data type and description of dataset.  

### `search_grocery.html`
1. Displays the header **"Grocery List"**.  
2. Includes a search bar and button allow users to quickly look up specific grocery items.
4. Provides a “Back to Home” navigation button.  

### `data.html`
1. Displays the header **"Grocery Table"**.  
2. Provides a “Back to Home” navigation button.  
3. Contains a full table of grocery records with all data.

## How to Run the Project

### 1. Set Up Your Environment
- Make sure Python is installed on your computer.
- run the requirements.txt
   ```python
   pip install -r requirements.txt
   ```

### 2. Start the Web Application
- Open a terminal or command prompt.
- Run the application with:
  ```python
  python website/app.py
  ```

### 3. Open in Your Browser
- After the server starts, go to:
http://127.0.0.1:5000/ or http://localhost:5000/ 


## Team Members

| Name                 | Role                      | Responsibilities                                                |
|----------------------|---------------------------|-----------------------------------------------------------------|
| **Diana Paola Gasca Duran**| Frontend Developer| Designed HTML templates, UI layout, search interface|
| **DongJu Ko** | Data Preprocessing & Documentation | Prepared and load data and README, structured project documentation |

Now enjoy exploring our ‘Grocery App’ web application. If you have any questions or problems, we’re here to help.🙂  
