# Web Scraping using Python – Beautiful Soup 

Web scraping is a phrase used to particularise the use of an algorithm to pluck and process large amounts of data from the web. Are you a data scientist, engineer, or anybody who investigates large amounts of datasets? The ability to irritate data from the web is a useful experience to have. Say you locate data from the web, and there is no immediate way to download it, web scraping using Python with bs4 is a craft you can use to extract the data into a useful form that can be imported.

Data Source:	
https://www.hubertiming.com/

Url we used: Results tab:
https://www.hubertiming.com/results/2019Y2K

We are using this article to get:
- Data extraction from the web using Python's Beautiful Soup
- Data manipulation and cleaning using Python's Pandas library'''


![Import Liabraries](https://user-images.githubusercontent.com/48548134/58807726-45dd5580-8636-11e9-82b1-49b783cb2943.PNG)

# Import required module to get started 
- Use Modules

  **urllib.request module is used to open URLs**
 
  *For More Reading https://docs.python.org/3/library/urllib.request.html*

  **BeautifulSoup to extract Data, we are using Beautiful Soup Version 4**
  
  *For More Reading https://pypi.org/project/beautifulsoup4/*
  
![Importing BS4](https://user-images.githubusercontent.com/48548134/58809689-0153b900-863a-11e9-8291-247b7953bdf5.PNG)

After importing you will open **Url "https://www.hubertiming.com/results/2019Y2K"**

![Url Open](https://user-images.githubusercontent.com/48548134/58810006-a7072800-863a-11e9-917a-a92ae8bb3ee5.PNG)

As we can see above the type for soup is BS4 & ready for extraction the simple way to check the html is captured in soup. The Beautiful Soup package is used to parse the html, that is, take the raw html text and break it into Python objects. 

# Example of Title Extraction

To extract data from html in python (Notebook), basic understanding must be required before you start working with any webpage.  Showing you how you can extract title of webpage present in page source under <title> </title>
![Page Source](https://user-images.githubusercontent.com/48548134/58810993-9fe11980-863c-11e9-995b-ae840ec70b43.PNG)

![Titlle in Python](https://user-images.githubusercontent.com/48548134/58811265-1bdb6180-863d-11e9-9e41-49c8f2774311.PNG)
**More Practice**, Extract all data for more absolute links <a href =

![find all a](https://user-images.githubusercontent.com/48548134/58811526-94422280-863d-11e9-854b-60004c8061b4.PNG)

**Iterate “href” & just get links under <a href = “ ”</a>**

![Iterarte](https://user-images.githubusercontent.com/48548134/58811713-f0a54200-863d-11e9-9ad5-8d4da2aadb6c.PNG)

If you visit webpage results, there are 10K data point in tabular format our aim is to extract all of the data through html & BeautifulSoup further cleaning the data with useful python modules/lib. 

*Please find the screen short below.*

![Webtable](https://user-images.githubusercontent.com/48548134/58811911-585b8d00-863e-11e9-9a4c-4be9adf8a80e.PNG)

# Let’s roll the cuff,

To print out table rows only, pass the 'tr' argument in soup.find_all(). & lets print first 10 rows: 

![Extracting 10 rows](https://user-images.githubusercontent.com/48548134/58812325-3a425c80-863f-11e9-8388-9bd5bd20b81c.PNG)

**Appending data in List data frame for Easy Evaluation**

Further steps, we will extract all <td></td> & append the value in list data frame as for evaluation we required all data to be gathered & collected again in tabular format. Let’s do it.

![Append List](https://user-images.githubusercontent.com/48548134/58812466-93aa8b80-863f-11e9-9f2f-9038934c668c.PNG)

You are doing fabulous job, keep the list_row in data frame, let’s do it. In, Screen short below you bring the data in DataFrame with [Row, Column] let’s split the data in individual columns as you can see data is separated by (‘ , ’)

![Data Frame](https://user-images.githubusercontent.com/48548134/58812735-129fc400-8640-11e9-919d-a3f6ec999557.PNG)

# Cleaning with Python Libraries:

As we can see the data is separated with by ‘,’ at 0 column, simple coding locating the column:

**Splitting & Stripping**

![Split](https://user-images.githubusercontent.com/48548134/58813090-b4bfac00-8640-11e9-8ad9-a0e86973e1fe.PNG)

![Strip](https://user-images.githubusercontent.com/48548134/58813184-d9b41f00-8640-11e9-842f-e5ef69a4b9ce.PNG)

**What else left? , Be patient! More than 65% of time actually goes with cleaning...otherwise you will come across multiple errors while evaluating, take a break & enjoy coding in python.**

*Do we need to add header to find the data belong to which feature or variable as you observed in actual table on the web page. If you go to page source of webpage the table heading is under <th></th>, let’s code in same fashion what you did earlier but now for table heading.*

![Column Name](https://user-images.githubusercontent.com/48548134/58813429-64951980-8641-11e9-90f7-00d4799d1c44.PNG)

*So, you have two Dataframes , let’s concat now.*
![Concat](https://user-images.githubusercontent.com/48548134/58813705-f69d2200-8641-11e9-91e6-3253675ca211.PNG)

Identify, now what else is left, still we need to place column name currently, as if now it is just “one more row”.

![ColumnNameupdate](https://user-images.githubusercontent.com/48548134/58814176-eb96c180-8642-11e9-861a-c8e26a785f7c.PNG)

Now we need to drop ‘0’ row, & drop NA value, you can find the description of Dataframe with describe & shape as well, Try matching original data set/table. 

![Drop Na](https://user-images.githubusercontent.com/48548134/58814261-1aad3300-8643-11e9-9853-b25ecbefbe04.PNG)

Seems, the table is looking fine for now, except few more changes keep evaluating.
If you, closely evaluate few more removal important to evaluate data, ‘ [‘ ‘]’  , Columns rename, You can observe same as we did in coding below

![Final Cleaning](https://user-images.githubusercontent.com/48548134/58814474-69f36380-8643-11e9-8247-c282719bcb16.PNG)

Data is cleaned now for further evaluation using Numpy , Matplotlib & sns.
In future article, using same data set, you will bring best with your evaluation.

# Enjoy Happy Coding!  


