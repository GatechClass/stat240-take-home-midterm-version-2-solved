# stat240-take-home-midterm-version-2-solved
**TO GET THIS SOLUTION VISIT:** [STAT240 Take-Home Midterm Version 2 Solved](https://mantutor.com/product/sp24-stat240-take-home-midterm-version-2-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113613&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;STAT240 Take-Home Midterm Version 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Important notes:

Question 1 is longer and more complex than question 2.

Please KNIT as you go along and CHECK YOUR OUTPUT to ensure there are no errors!

Question 1

This question involves cleaning and exploring a dataset from the United States Department of Agriculture (USDA) Foreign Agriculture Service (FAS) Production, Supply, and Distribution (PS&amp;D) database, source.

Part 1A

Create a new data frame called psd_tidy by performing the following operations IN THE ORDER SPECIFIED!. If you do the operations out of order you WILL get errors! Write all code in the chunk provided below. Check after each step that your data frame matches what is expected by using dim() to get the dimensions.

NOTE: I HIGHLY recommend reading the instructions below in the knitted HTML file instead of in this Rmd file, they’re formatted to be MUCH easier to read in HTML format!

1. First, select just the Commodity_Description , Country_Code , Country_Name , Market_Year , Attribute_Description , and Value .

After step 1, your data frame should have 2,001,791 rows and 6 columns.

2. Next, pivot the data frame to a wider format so that variable names from Attribute_Description are spread out over multiple columns and values from Value are used to fill in the data frame.

We highly recommend adding the argument names_repair=”universal” to your pivot function, which will automatically repair column names by replacing invalid characters with periods

After step 2, your data frame should have 155,338 rows and 75 columns

3. After step 2, you should have a lot more columns with specific commodity details like production, imports/exports, etc. Select just the columns Commodity_Description , Country_Name , Market_Year , Production , Imports , Exports and rename

these as “commodity”, “country”, “year”, “production”, “import”, “export”; also keep Total.Distribution and

Domestic.Consumption , rename these to be lowercase. In addition, please also sort rows by commodity, then country, then year.

After step 3, your data frame should have 155,338 rows and 8 columns

4. Now, remove rows where:

The country is in a list of countries which do not have recent data for a variety of reasons (see chunk below for details)

The commodity is either “Cotton”, “Millet”, or “Mixed Grain” as these are reported inconsistently.

After step 3, your data frame should have 123,186 rows and 8 columns

## This chunk contains the two lists of countries to remove (feel free to use this code)

## countries that no longer exist OR started reporting data together with their parent country:

old_countries = c(“Antigua and Barbuda”, “EU-15”, “EU-25”, “Former Czechoslovakia”, “Former Yugoslavia”, “Fr.Ter.Africa-Issas”, “French Polynesia”, “Gaza Strip”, “German Democratic Republic”, “Germany, Federal

Republic of”, “Gibraltar”, “Gilbert and Ellice Islands”, “Greenland”, “Guadeloupe”, “Martinique”, “Puerto

Rico”, “Serbia and Montenegro”, “St. Lucia”, “Union of Soviet Socialist Repu”, “Virgin Islands of the U.S

.”, “Yemen (Aden)”, “Yemen (Sanaa)”, “Yugoslavia (&gt;05/92)”)

## countries that stopped reporting individual data and instead report as part of “European Union”:

eu_countries = c(“Austria”,”Belgium”,”Bulgaria”,”Croatia”,”Cyprus”,”Czechia”,”Denmark”,”Estonia”,”Finland “,”France”,”Germany”,”Greece”,”Hungary”,”Ireland”,”Italy”,”Latvia”,”Lithuania”,”Luxembourg”,”Malta”,”Neth erlands”,”Poland”,”Portugal”,”Romania”,”Slovakia”,”Slovenia”,”Spain”,”Sweden”)

## if you want to use a filtering join, you can use this as one of the input data frames:

countries_to_remove = tibble(

country = c(old_countries, eu_countries)

)

NOTE: For the rest of question 1, unless otherwise specified, always start with psd_tidy as your initial tidy data frame. Do NOT overwrite psd_tidy with any operations in later parts, since we will reuse it.

# Insert Code Here

Part 1B

Let’s explore a few columns of our psd_tidy data frame. Perform the following operations in order. Remember you should NOT overwrite psd_tidy , so please save your output to a new data frame called psd_summary .

2. For each commodity and country, summarize to obtain the total sum in each of the total.distribution, production, import, and export columns.

Note: use na.rm=TRUE inside sum() to ignore any NAs

After step 2, your summary data frame should have 2567 rows, one for each commodity-country combination.

3. Regroup by just commodity. Add a new column called global.total that has, on each row within a commodity, the same value, representing the sum of the total.distribution sum you calculated in step 2.

4. Calculate the percentage that each country’s production, import, and export (the sums in step 2) represent out of the global.total of each commodity (that you just calculated in step 3).

For each question, you should print a table with 1 row for each commodity showing the country name and the percentage. Please print the ENTIRE data frame! Note there are only 60 commodities, so you should only need to print 60 rows, use something like

2. For each commodity, which country is the largest global importer by percentage over the last 10 years?

3. For each commodity, which country is the largest global exporter by percentage over the last 10 years?

Part 1C

Again, starting with psd_tidy from part 1A, let’s focus on a few popular commodities and visualize trends in their production over the years. Create a new data frame for each question and DO NOT modify psd_tidy itself.

1. Corn is one of the most popular commodities. Make a plot of corn production over time.

2. Repeat the above steps for Wheat, another of the most popular commodities. Note you should be able to just copy the entire code above and just change Corn to Wheat everywhere.

3. Several of the commodities include the words “Meat”, “Dairy”, or “Fresh” (these are fresh produce). For example, “Meat, Chicken” and “Poultry, Meat, Broiler” are two of the several meat commodities and “Dairy, Butter” and “Dairy, Cheese” are two of several dairy commodities.

Step 1: – Use mutate(category = str_extract(commodity,”Meat|Dairy|Fresh”)) to create a new variable called category which contains either the word “Meat”, “Dairy”, “Fresh”, or NA. – Drop the NA rows in category Step 2: – Re-summarize the data to obtain total production within each country-category combination.

Step 3: – Calculate each country’s total production across all three categories, and add this as a new column, with the same value in every row within a country.

Step 4: Make a bar plot comparing the levels of meat, dairy, and fresh produce production for these 10 countries; put country on the y axis, total production on the x axis, and change the interior color of the bars by category .

Question 2

More info about the dataset can be found in the help page by running ?storms

data(“storms”) print(storms)

## # A tibble: 19,537 × 13

## name year month day hour lat long status category wind pressure

## &lt;chr&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;int&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;fct&gt; &lt;dbl&gt; &lt;int&gt; &lt;int&gt;

## 1 Amy 1975 6 27 0 27.5 -79 tropical d… NA 25 1013

## 2 Amy 1975 6 27 6 28.5 -79 tropical d… NA 25 1013

## 3 Amy 1975 6 27 12 29.5 -79 tropical d… NA 25 1013

## 4 Amy 1975 6 27 18 30.5 -79 tropical d… NA 25 1013

## 5 Amy 1975 6 28 0 31.5 -78.8 tropical d… NA 25 1012

## 6 Amy 1975 6 28 6 32.4 -78.7 tropical d… NA 25 1012

## 7 Amy 1975 6 28 12 33.3 -78 tropical d… NA 25 1011

## 8 Amy 1975 6 28 18 34 -77 tropical d… NA 30 1006

## 9 Amy 1975 6 29 0 34.4 -75.8 tropical s… NA 35 1004 ## 10 Amy 1975 6 29 6 34 -74.8 tropical s… NA 40 1002

## # <img draggable="false" role="img" class="emoji" alt="ℹ" src="https://s.w.org/images/core/emoji/15.1.0/svg/2139.svg"> 19,527 more rows

## # <img draggable="false" role="img" class="emoji" alt="ℹ" src="https://s.w.org/images/core/emoji/15.1.0/svg/2139.svg"> 2 more variables: tropicalstorm_force_diameter &lt;int&gt;, ## # hurricane_force_diameter &lt;int&gt;

Part 2A

Note the data frame has many rows per storm. The purpose of this problem is to make a data summary storms_summary with one row per storm with the following variables:

year : year of each storm name : name of each storm note there are many duplicate names in the dataset

using both year and name (almost) uniquely identifies each storm with one exception (Zeta from Dec 2005 to Jan 2006, which we just ignore for now)

min_pressure : MINIMUM air pressure (note pressure decreases as storm intensity increases)

Your result should have 639 or 655 rows; some computers use an older version of “storms” hence the difference. Print at least the first 6 rows!

# Write your code to overwrite storms_summary HERE; you can even continue with a pipe from the previous l ine if you want

# Don’t change this line, and it must be after your code above storms_summary[storms_summary==-Inf]=NA

# Print the first 6 rows here print(storms_summary, n = 6)

## # A tibble: 19,537 × 14

## name year month day hour lat long status category wind pressure

## &lt;chr&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;int&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;dbl&gt; &lt;fct&gt; &lt;dbl&gt; &lt;int&gt; &lt;int&gt;

## 1 Amy 1975 6 27 0 27.5 -79 tropical de… NA 25 1013

## 2 Amy 1975 6 27 6 28.5 -79 tropical de… NA 25 1013

## 3 Amy 1975 6 27 12 29.5 -79 tropical de… NA 25 1013

## 4 Amy 1975 6 27 18 30.5 -79 tropical de… NA 25 1013

## 5 Amy 1975 6 28 0 31.5 -78.8 tropical de… NA 25 1012 ## 6 Amy 1975 6 28 6 32.4 -78.7 tropical de… NA 25 1012

## # <img draggable="false" role="img" class="emoji" alt="ℹ" src="https://s.w.org/images/core/emoji/15.1.0/svg/2139.svg"> 19,531 more rows

Part 2B

Finally we’ll do a bit more visualizing and summarizing using storms_summary which you just created.
