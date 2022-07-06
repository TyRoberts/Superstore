# Super-Store
#### This project is based on the Superstore dataset that comes with every Tableau download. I was originally inspired to do this project after seeing a Tableau Viz of the Day created by Idris Akilapa. I really liked the format of the view but didn't like the color scheme and saw some errors with the data and functionality, so I decided to redesign it. My main objective was to improve my Tableau skills by redesigning this view. I learned a plethora of new Tableau skills and successfully redesigned the view with my own aesthetics and corrected discount data.
#### After completing the Tableau portion I turned to PostgreSQL to write the queries to match since Tableau Public doesn't support SQL integration. After creating the table for and importing the Superstore dataset, I quickly decided to make some changes. The original dataset consisted of one table with a significant amount of redundant data which normalization could easily solve. I came across a few problems while normalizing the data. The first was while creating the address table, during my initial import of the dataset I got an error for NULL values in the postal code column. I made the decision to remove the NOT NULL constraint for this column and deal with the issue later. Upon further investigation all of the NULL values were for Burlington, Vermont, because I had no other way to find the actual postal code for these I just used one of the postal codes for the area. The next problem came when I was creating the products table, 33 of the product ID's had two products referencing them. To remedy this, I changed one of the products to the next sequential ID, if it was available. The last issue I had was creating the products table, in the original dataset the values I used to come up with price and cost went out to four decimal places. I could have, and possibly should have, kept these decimals and just rounded my cost column whenever it was included in results. Instead, I decided to round cost in my table creation which created slight variances when profit was calculated. This was my first time creating a database where I had to normalize the data, I learned quite a few things in the process and look forward to using them in other projects. 
#### For the most part the queries were straight forward with the main challenge being how to group the results. I ultimately decided to keep the results as close to the Tableau view as I could. The results match the view with a few divergences, when the result data was diminutive I decided to group the regions. To do this I used PostgreSQL's crosstab (pivot) function. This was the first time I used crosstab but I believe it will become a staple in my querying going forward. This project provided me with a great deal of opportunities to advance my knowledge in Tableau, SQL, and data analytics. I look forward to using this knowledge and obtaining more in future projects.
#### <a href="https://public.tableau.com/app/profile/tyrell.roberts/viz/SuperStore_16567889241470/RegionalOverview"> View Tableau Dashboard Here!</a>
[Orders.csv](https://github.com/TyRoberts/Super-Store/files/9050876/Orders.csv)
