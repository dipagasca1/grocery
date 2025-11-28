
# Grocery App (Flask + SQLite)
This project showcases a grocery inventory management page using the *Grocery Inventory dataset*. The workflow includes data preprocessing, database creation, and developing a web application for data visualization. It allows users to:

-	Search grocery items by name.
-	View item details such as category, supplier, stock quantity, and price.
-	Access clean and structured data through an integrated SQLite database.


## Dataset Information 

![Grocery Store Logo](https://images.seeklogo.com/logo-png/38/1/grocery-store-logo-png_seeklogo-384031.png)

The dataset used for this project can be found on Kaggle: [Grocery Inventory]( https://www.kaggle.com/datasets/willianoliveiragibin/grocery-inventory?utm_source). 


**Step 1: Data Preprocessing**

1. Cabin Column Removed:  

 Reason: In original dataset category was mistyped as ‘Category’.  
 Action: Revised as ‘Category’ from dataset.

2. Null values dropped:  

 Action: The dataset's remaining null values were eliminated. 

3. Made an updated CSV:  

 Name of the file: "grocery_inventory.csv" 

**Step 2: Database Creation** 

The cleaned data is read from 'grocery.csv' by the 'dataload.py' script, which then loads it into an SQLite database.  

 
**Step 3: Developing Web Application** 

The Flask framework is used by the 'app.py' script to build a web application with two routes: 

path **/grocery**: The 'grocery.html' page is rendered by this. Features a button to jump to the dataset. 
path **/grocery_table**: Opens the 'grocery_table.html' page with data that has been retrieved from the SQLite database ('grocery.db'). 

## HTML Pages 

**'Grocery search.html'** 
1. Header: The page displays a clear title, "Grocery List".
2. Search Function: A search bar and button allow users to quickly look up specific grocery items.
3. Navigation: A “Back to Home” button lets users return to the main page easily. 

**'Grocery data.html'**  
1. Header: The page includes a main title, "Grocery Table", which introduces the full dataset.
2. Navigation: A “Back to Home” button helps users move back to the homepage.
3. Data Table: The page features a full table view. Each row shows one record, and each column displays a specific attribute from the dataset.

## How to Run the Project

### 1. Set Up Your Environment
- Make sure Python is installed on your computer.
- run the requirements.txt
   ```python
   pip install -r requirements.txt
   ```

### 2. Start the Web Application
- Open a terminal or command prompt.
- Move to the directory where app.py is located.
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
