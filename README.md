**1.	WHAT IS THE OVERALL TREND IN TECH LAYOFFS FOR THE DIFFERENT COUNTRIES AND HOW DO PERCENTAGE LAYOFFS FLUCTUATE OVER THE YEARS?
**
In the query, I selected the relevant columns i.e. country, year. Next, to discern the trend over the years, I calculated the average of laid off staff per year using the AVG function. Similarly, I used the AVG function to calculate the average percentage. To filter out null values, I utilized the IS NOT NULL condition in the WHERE statement. Subsequently, I grouped aggregated values by country and year then ordered by year in DESC order to rank the output from most recent.
The results indicate that the USA, Sweden, Argentina, Germany, India, Indonesia have the highest tech layoffs compared to the rest of the countries.
They also indicate fluctuations in both average percentage and average layoff. This pattern of initial decline followed by an increase and ultimately another decline is indicative of changing conditions over time.

**2.	HOW DOES THE COMPANY SIZE BEFORE AND AFTER LAYOFFS CORRELATE WITH THE LAID-OFF PERCENTAGES, AND ARE THERE INDUSTRIES OR STAGES MORE PRONE TO SIGNIFICANT WORKFORCE REDUCTIONS?
**
The query used the AVG function to establish the laid off average. By doing this I was able to then compare it against company size before layoffs and company size after layoffs. 
The graph above depicts that as company size before and after increases so does the laid off average which indicates a positive linear correlation. A separate query to validate the first query was run and it gave the following results. The correlation coefficient between average size before lay off and average lay off is 0.694 and the correlation between average size after lay off and average layoff is 0.673. These positive values therefore prove that the correlation is indeed a positive one albeit a weak one.

**3.	CAN WE IDENTIFY ANY PATTERNS IN TOTAL NUMBER OF LAYOFF’S BASED ON INDUSTRY AND STAGE?
**
In the query, i selected the relevant columns then using the SUM function I computed the total number of laid off which I grouped by industry and stage. Lastly I ordered by total number of laid off in DESC order and applied a LIMIT of 50.
In the tree map, it can be observed that consumer and retail are the industries with the highest tech layoffs while media and data are the lowest.
In the bar chart, Post IPO stage is by far the stage with the highest layoffs followed far behind by unknown, acquired and series B.

**4.	HOW HAS THE TOTAL AMOUNT OF MONEY RAISED BY TECH COMPANIES EVOLVED OVER THE YEARS, AND IS THERE A RELATIONSHIP BETWEEN FUNDRAISING SUCCESS AND LAYOFF OCCURRENCES?
**
The query utilized the CASE function to perform conditional logic. In this scenario, I included an extra category called revenue greater than $50M. The specified conditions were, WHEN money raised in millions is greater than $50M then high revenue, WHEN money raised in millions is greater than $20M then revenue moderate ELSE revenue low. 
Netflix takes the lead in terms of High Revenue, followed by Meta and Uber with moderate revenue and finally Cruise, Delivery Hero, Grab, Rivian, Twitter and We Grab with low revenue.
In the category called Stage, post IPO leads in terms of money raised followed by Series H and Acquired which both fall into the low revenue categorization.
In the category called Industry, Media, Consumer and Transportation fall in the high revenue category while food and real estate fall in the low revenue category. Notably, consumer and transportation also feature in the low revenue category.

**5.	WHAT IS THE AVERAGE SIZE AFTER LAYOFFS AND WHICH COMPANIES ARE OPERATING 50% BELOW THAT THRESHOLD?
**
The query consisted of an ‘inner query’ that first calculated the average size after layoffs. Subsequently, the WHERE command of the ‘outer query’ filtered the rows based on the condition that company size after layoff should be less than 50% of the average size after lay off. Lastly, i ordered the company size after layoff in DESC order and applied a LIMIT of 10. This was because, prior to applying it, the query returned 1,128 companies operating 50% below average. 
From the visualization it can be observed that all the companies have an average workforce of 1,600 staff post layoff. 
It should be noted that the initial average was 3,299. I then applied a condition of 50% * the initial average which reduced the threshold to 1,649. After running the query, it returned 1,128 values which were exceedingly high. Therefore, to make the visualization possible, I limited the output to 10. 











