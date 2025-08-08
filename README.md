# StepAhead

<b>First Dataset name: </b> 2020 Brooks Running Shoes <br>
<b>Company: </b> Found on Kaggle, created by user Hannah Collins. Includes data obtained from Brooks (https://www.brooksrunning.com/en_us) <br>
<b>Download link: </b> https://www.kaggle.com/datasets/hannahcollins/2020-brooks-running-shoes <br>
<b>Date of Access: </b> 3/20/25

<br>

<b>Second Dataset name: </b> BrooksCustomers <br>
<b>Company: </b> Created by Justin Davis and Thompson Morgan on Mockaroo (https://www.mockaroo.com/)  <br>
<b>Download link: </b> Available to download as a csv file in this repository <br>
<b>Date of Access: </b> 4/17/25

<br>

-  Data Source: The first dataset is from a dataset created by Hannah Collins on Kaggle. The data was first uploaded around five years ago, according to Kaggle. The data is a csv file. The second dataset was randomly generated for the purposes of this project on Mockaroo. The data is a csv file. <br><br> Collins, H (2020). <i>2020 Brooks Running Shoes.</i> Kaggle. Data accessed 3/20/25. Available from: https://www.kaggle.com/datasets/hannahcollins/2020-brooks-running-shoes. <br><br>

-  Collection Method: The first dataset was scraped off of Brook's website by Hannah Collins before it was uploaded to Kaggle. The second dataset was randomly generated using the website Mockaroo (https://www.mockaroo.com/). The customers requested a maximum budget, and for the rest of the variables all of the options were given to be randomly selected from.

-  Extraction Method: ​ The first dataset was exported from https://www.kaggle.com/datasets/hannahcollins/2020-brooks-running-shoes as a .csv file. The second dataset was randomly generated on Mockaroo (https://www.mockaroo.com/).

-  Data Cleaning and Manipulation: ​ After downloading the data, the .csv file was read into a JupyterLab notebook and cleaned using python. The column names were changed to lowercase with no spaces or special characters to use SQL in the future. Unnecessary columns about specific shoes were dropped. For the two missing values in the midsole_drop_mm column, they were obtained by us from the Brooks website and entered manually into our new dataframe. The remaining missing values in the arch level columns were all filled in with 'No' because they were originally left blank if the answer was not 'Yes'. We then decided to convert all of these 'Yes' and 'No' values into booleans.

-  Data Units: The units for all price values are USD, the midsole drop units are in millimeters (mm), and the weight units are in grams (g).

-  Data Formulas: Our formula for assigning a shoe a match score for a specific customer looks at the customer's gender, price range (max budget), support, and arch type. We decided on weighing these values in the order of gender > price > support > arch type. Specifically, on a normalized scale ranging from zero to one, we classified gender as 0.4, price as 0.3, support as 0.2, and arch type as 0.1. The sum of these values is equal to the match score of that shoe for that customer.

-  Data Validation: All of the categorical data was checked using the unique function to make sure everything was case-sensitive to ensure consistency in the entries.

-  Data Columns for first dataset:
    - name: object, states the name of the shoe
    - gender: object, states if a shoe is Men's, Women's, or Unisex
    - price: float64, lists the price of the shoe in USD
    - support: object, states if a shoe has max support, basic support, or neutral support 
    - experience: object, states if a shoe is made for speed, cushioning, energizing, or connecting
    - surface: object, states if a shoe is made for roads or trails
    - midsole_drop_mm: float, lists how many millimeters the midsole drop of the shoe is
    - weight_g: float, lists how heavy the shoe is in grams
    - high_arch: boolean, states if a shoe is available with a high arch
    - medium_arch: boolean, states if a shoe is available with a medium arch
    - flat_arch: boolean, states if a shoe is available with a flat arch

- Data Columns for second dataset:
    - customer_id: int64, lists the customer's unique ID number
    - price_range: int64, lists the customer's budget in USD
    - customer_support: object, states if the customer prefers max support, basic support, or neutral support
    - run_type: object, states if the customer is looking for a shoe made for roads or trails
    - arch_type: object, states if the customer is looking for a shoe with a high, medium, or flat arch
    - customer_gender: object, states if the customer is looking for a Men's or Women's shoe

-  Data Usage: ​ Both of our datasets are intended for public access and use.
