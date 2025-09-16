**************PROGRAMMING ASSIGNMENT 2**************
# 1. PROBLEM 1: Using knowledge obtained from the experiment and demonstrations: a. Load the corresponding .csv file into a data frame named cars using pandas b. Display the first five and last five rows of the resulting cars.

    import pandas as pd    // importing pandas
    
    cars = pd.read_csv('cars.csv')    // reads the csv file and and stores in the variable cars
    cars
    
    cars.head()    // dislays the first 5 rows of the DataFrame
    cars.tail()    // displays the last 5 rows of the DataFrame


# 2. PROBLEM 2: Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations. a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars. b. Display the row that contains the ‘Model’ of ‘Mazda RX4’. c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have? d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.
    
    import pandas as pd   // importing pandas
    
    cars = pd.read_csv('cars.csv')    // reads the csv file and and stores in the variable cars
    cars
    
    odd_columns = cars.iloc[:,1::2]   // selects every odd numbered column using iloc
    result = odd_columns.head()      // dislays the first 5 rows of the odd numbered columns
    result
    
    cars[0:1]  // displays the first row of the DataFrame
    
    cars.loc[cars['Model']=='Camaro Z28', ['Model', 'cyl']]    // selects rows where the model and camaro is equal, but displays model and cyl columns only
    
    cars.loc[[1,28,18],['Model', 'cyl', 'gear']]   // selects rows with 1, 28, 18, but displays model, cyl, and gear columns only
