# ADIDAS-USA-SALES-ANALYSIS

Adidas, is a German manufacturer of athletic shoes and apparel and sporting goods. In the early 21st century it was the largest sportswear manufacturer in Europe and the second largest (after Nike) in the world.


This analysis covers the company sales between 2021 and 2022. The tool used in this analysis is Power BI.

Dataset is from kaggle.

The problem statements and metrics I will derive my insights from are:

1. What sales method generated the highest sales?
2. What are the top 3 products with the highest sales?
3. What region and state recorded the highest sales and profit?
4. Which retailer generated the highest sales?
5. What Are The Top 5 States With The Highest Sales?
6. Before this analysis is being carried out. I will ensure my ETL (extraction, transformation, and loading) procedures is taken to ensure my raw data is ready for analysis.

The first step is to load my raw data into power query in Power BI for data transformation. I have three tables in my dataset.

Table 1: Data sales adidas

You can see there are four rows with null values. So I need to remove them by using the ‘remove top rows’ function, and make the first row as the headers. And change the data type of ‘retailer ID’ to ‘text’, ‘Total Sales’ and ‘Operating profit’ to ‘Fixed decimal number’, ‘Operating margin’ to ‘percentage’.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*75Ot2a8mvZKPUrpqkwMD4Q.png">

The transformed table:

<img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*uvj8sm1js6tuA2Oo9BJQow.png">

Table 2: Location

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*79RHHkoY9JqndSzfy5L3Hw.png">

The first three rows contain null values also. So I have to remove them by using the ‘remove top rows’ function and make the first row as headers like what I did in table 1.

The transformed table:

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*pmCa18Wb_1Gl-Wc4rM4rZg.png">

Table 3: Product

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*5Evt1nQXaPl5-WyspkhWow.png">

I only need to make the first row as headers here.

Transformed table:

<img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*a2Q5OQ6N3MzlVuao16eFyQ.png">

So I am done with my tables transformation. Then I close and apply to load the dataset into Power BI.

The next step I will take is creating my data modelling. This is to create a one-to-many relationship with my tables. Though Power BI automatically created this modelling. However, I need to add the calendar table to the modelling by using the DAX function and formula.

The initial modelling:

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*w9ZcWQSekh5a3eKRpqac4A.png">

The DAX formula: Go to the ‘modelling’ panel and create a ‘new table’ with the formula and click enter:

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*Fg5_gFZChTZ01uBgDAJf3w.png">


Then connect the calendar table to the main table by dragging the ‘date’ on the calendar to the ‘invoice date’ on the ‘adidas sales’ table. So this is the new data modelling:

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*TiK973hIqtxWe39_t39sAA.png">


Before creating my report, I will formulate some measures like; Total unit sold, Total sales, average price, etc. These will help me create an insightful report.


List of Measures To Be Calculated

1. Total Unit Sold: To calculate the total number of unit of products sold.


<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*XyK5HbN1Svk1p1_Mtgkf3w.png">


2. Total Sales: To calculate the total number of revenue generated.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*sCbjgBZU2dmu2DOfckhHxQ.png">



3. Average Price: This is the average price of each product.

   <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*EUsw6V4NCe5RNVJGLdOvhQ.png">


4. Profit: This is to calculate the total profit accrued from the sales

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*fukU986lPE4a5waDyVStgw.png">


5. Average Operating Margin: This is the average value of operating margin. Note that this will be in percentage.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*uWsXbxas-uwm-dxPYoJvWg.png">


6. Transaction Count: This is the total number of transactions made.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*4ldrEA4azggij2w6WysD1A.png">


DASHBOARDS:

Home Page

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*xUdR-YT-sqaiesK7GyFHjw.png">


Product Page

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*767wSoMeQ_mC2-7s5KiB0A.png">


Deep Insights Page

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*l9R1DTDPesgnO4z7nUB-6w.png">

Trend Analysis Page

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*BgodgU724U5PR20n_uWsPQ.png">




