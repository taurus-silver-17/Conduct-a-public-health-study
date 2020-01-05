# Prerequisite
For this project, you will have to know how to manipulate the basics of the R or Python language, and how to use Dataframes type objects in these languages (objects native to the R language, and available in the Pandas library of Python. This project will make you work - via dataframes - on the concepts of relational algebra, which it is good to master. You will also have to master the basics of the SQL language, notably SQL queries of the SELECT type. If you are already familiar with this type of query, then you are probably unknowingly familiar with the concepts of relational algebra necessary for this project. Finally, you will need to know how to install and query (in SQL) a database management system of your choice (indications are given in the statement).


# Setting in situation
You are part of a new team of researchers at the Food and Agriculture Organization of the United Nations (FAO), one of the UN's constituent bodies whose goal is to "help build a world free from hunger".

Your team is charged with carrying out a major study on the theme of undernutrition in the world.

The problem of hunger is complex and can have multiple causes, which differ from country to country. The preliminary stage of this study will therefore be to establish a "state of the art" of the research already published, but also to conduct a statistical study designed to direct research towards specific countries, and to highlight different causes of hunger. Thus, a handful of data analysts (including you!) have been selected to carry out this preliminary step. During the first meeting, you were designated to set up the database that your team could request (in SQL) at will to carry out this statistical study.

# The data
The data are available on the FAO website at http://www.fao.org/faostat/fr/#data .

Based on the needs expressed below in this statement, it will be up to you to choose which data to download. However, the following sections will be useful to you:

# Competencies assessed
- Mastering the basics of Python
- Perform complex SQL queries
- Applying relational Python algebra
- Use technical documentation
- Retrieve data from an identified source
- Using Specialized Libraries for Data Science

# Food balance sheets
Food Safety, then in this section, Food Safety Data .
This section contains many indicators, but here we will focus only on the indicator Number of undernourished people.
Your mission
Are you ready? Then let's do it! :sun:
Download the data.
You can select the types of data you wish to download from the CAM site interface. As the volume of these data is large, the interface allows a first filtering according to countries (or groups of countries and regions of the world), years, elements, products (and groups of products: cereals, animal products, etc.).

FAO separates its data into two distinct food categories: animal and plant products.

Create a dataframe containing population information for each country. Calculate the total number of humans on the planet. Criticize your result. If there are any anomalies, analyze and make the necessary corrections.

# Question 1: 
Give the result of your calculation for the year 2013, as well as for the last year available on the day you carry out this project.

Among the Food Balance Sheets documents you have downloaded, there is redundant information. Indeed, for a given country, some of this information can be calculated from others:

Production (Production)
Imports (Import Quantity)
Exports (Export Quantity)
Change in inventory (Inventory Change)
Domestic supply
Seed
Loss (Waste)
Food, also known as Food Supply.
Animal feeds (Feed)
Processing (Traitement)
Autres utilisations (Other uses)

# Question 2 : 
Identify these redundancies, giving your answer as a mathematical formula (no need to code here :sun: ). It is a 3 term equation of type \(a_1 + a2 + [...] = b_1 + b_2 + [...] = c_1 + c_2 + [...]\) ) involving each of the 11 quantities given above.

Illustrate this equation with the example of wheat in France. For a hint, click on "Definitions and Standards" on the data download page.

# Question 3 : 
Calculate (for each country and each product) the food availability in kcal and then in kg of protein.

You will do this from this information:

Population of each country;
Food Supply given for each product and for each country in kcal/person/day.
Protein supply quantity given for each product and for each country in g/person/day.

# Question 4 :

From this last information, and from the weight of food availability (for each country and each product), calculate for each product the "energy/weight" ratio, which you will give in kcal/kg. You can check the consistency of your calculation by comparing this ratio to the data available on the internet, for example by looking up the caloric value of an egg.

Note: Food availability in kcal/person/day is calculated by the FAO by multiplying the amount of Food by the energy/weight ratio (in kcal/kg), then dividing it by the country's population and then by 365. Here you are just asked to find the energy/weight ratio that the FAO used in its calculation.

Following the same methodology, also calculate the percentage of protein in each product (for each country). This percentage is obtained by calculating the ratio "weight of protein/total weight" (pay attention to the units used). You can check the consistency of your calculation by comparing this ratio to the data available on the internet, for example by looking for the protein content of oats.

# Question 5 :
Name 5 of the 20 most caloric foods, using the energy-to-weight ratio.
Surprisingly, this ratio can be different from country to country. Therefore, for each food, you will have to make an average for the different countries. You will therefore create a new table by aggregating. Be careful to remove the values equal to 0 so as not to distort the calculation of the average.
Name 5 foods among the 20 foods richest in proteins.

To deepen the reflection, it is important to learn more about protein quality, especially the PDCAAS index. Here are the corresponding Wikipedia articles: French, English. This aspect is not requested in the defense, it is just for general knowledge.

- Give the results of questions 6 to 14 for the year 2013 as well as for the latest year available in FAO data.

# Question 6: 
Calculate, for plant products only, the world domestic availability expressed in kcal.

# Question 7: 
How many humans could be fed if all the world's domestic availability of plant products were used for food? Give the results in terms of calories, then protein, and then express these 2 results as a percentage of the world's population.

Find out about the recommendation (from the FAO if possible) concerning the number of calories as well as the number of proteins per day necessary for a human being (Go zoo, we search on the internet ! ;) ).

# Question 8 : 
How many humans could be fed if all available plant food (Food), plant feed (Feed) and plant waste (Waste) were used for food? Give the results in terms of calories, then protein, and then express these 2 results as a percentage of the world's population.

# Question 9 : 
How many humans could be fed with the world's food supply? Give the results in terms of calories, then protein, and then express these 2 results as a percentage of the world's population.

# Question 10 : 
Using the downloaded data on undernutrition, answer this question: What proportion of the world's population is considered undernourished?

List the products (and their codes) that are considered cereals according to the FAO.

Locate information about cereals in your data (for example, by creating a Boolean column called "is_cereal").

# Question 11 : 
Taking into account only cereals intended for food (human and animal), what proportion (in terms of weight) is intended for animal feed?

Select from the food balance sheet data the information for the countries in which FAO counts undernourished people, for a selected year.

Identify the 15 most exported products from this group of countries in the selected year.

From the global food balance sheet data, select the 200 largest imports of these products (1 import = a quantity of a given product imported by a given country in the selected year).

Group these imports by product, so that you have a table containing 1 row for each of the 15 products. Then, calculate the following 2 quantities for each product:

the ratio between the quantity for "Other uses" (Other uses) and domestic availability.
the ratio between the quantity intended for animal feed and the quantity intended for food (animal + human)

# Question 12: 
Give the 3 products that have the highest value for each of the 2 ratios (you will then have 6 products to quote).

# Question 13:
How many tonnes of cereals could be released if the US cuts its production of animal products by 10%?

# Question 14:
In Thailand, what proportion of cassava is exported? What is the proportion of undernourished people?

Enter your data in a relational database
Well, no more mathematical calculations :'(, let's move on to the technical, the real thing !)

Transform your data into a format suitable for the use desired by the end users, who will use your database via the SQL language. Once the data is properly formatted, you will integrate it into a database.

Your database should contain these different tables:

A table called population, containing the population of each country for each year between 2012 and the last year available on the date you visited the FAO site. It should contain 4 columns: country, country_code, year, population.

# Question 15:
Propose a relevant primary key for this table.

A table called dispo_alim containing for each country, for each product, and for each year between 2012 and the last available year, the following information:
the nature of the product (two possible values: "animal" or "vegetable")
food availability in tonnes
food availability in Kcal/person/day
dietary availability of protein in g/person/day
dietary availability of fat in g/person/day
It should contain these columns: country, country_code, year, product, product_code, origin, availability_alim_tonnes, availability_alim_kcal_p_d, availability_prot, availability_mat_gr .
Question 16: Propose a relevant primary key for this table.

A table called equilibre_prod containing for each country, for each product, and for each year between 2012 and the last available year, the following quantities :
domestic availability
pet food
seeds
losses
processed
food
other purposes
It should contain these columns: country, country_code, year, product, product_code, availability, alim_ani, seeds, losses, transfo, food, other_uses.

# Question 17:
Propose a relevant primary key for this table.

A table called under_nutrition, containing the number of undernourished people for each country and for each year between 2012 and the latest year available. It should contain 4 columns: country, country_code, year, nb_persons.
Question 18: As you can imagine... propose once again a relevant primary key for this table!

# Question 19:
Write the SQL queries to know...

- The 10 countries with the highest food availability/capita ratio in terms of protein (in kg) per capita, then in terms of kcal per capita.
- For each year available, the 10 countries with the lowest food availability/capita ratio in terms of protein (in kg) per capita. The number of rows in the table returned will therefore be equal to 10 times the number of years available.
The total amount (in kg) of products lost per country per year. The returned table will therefore contain one line per couple (country, year).
- The 10 countries with the highest proportion of undernourished people.
- The 10 products for which the ratio of other uses/domestic availability is the highest.

# Question 20:
for some of the products identified in this last SQL query, suppose what are these possible "other uses" (search on the internet!).

Enrich your analysis
In your presentation, you will present the tracks studied so far using FAO data. In reality, you are not the first to study this phenomenon (fortunately!). So make sure you confirm your intuitions through internet research: your mentor will provide you with sources.

For a good analysis, the data analyst must understand the field he/she is studying. This is called "business knowledge". From the sources provided by your mentor, you will therefore also be asked to cite other causes of hunger, and to enrich your analysis with new figures. If you are motivated, you can even check some of the figures quoted in the sources against FAO data ;)
In particular, look for answers to these questions:

How many people die from the causes of hunger?
What are the world population forecasts in 2050? 


