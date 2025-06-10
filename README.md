# Bellabeat_Case_Study

**1. Ask**
**1.1  Key Stakeholders**

   1. Urska Srsen: Cofounder and Chief Creative Officer at Bellabeat.
   2. Sando Mur: Cofounder and key member of the Bellabeat executive team.
   3. Marketing analytics team at Bellabeat: A team of data analysts responsible          for marketing bellaport product.
   4. Customers: People who purchases bellabeat product or use their service.


**1.2 Business Task/ Objective:**

To analyze Fitbit fitness tracker data from thirty eligible users in order to generate actionable insights that can inform the marketing strategy for Bellabeat products.

To examine user behavior through smart device usage data, with a specific focus on understanding how customers engage with health-tracking features.

For this case study, the analysis will center on the Bellabeat Time smart watch.


**2: Prepare**

**2.1 Data Source**

1. The dataset is publicly available, Fitbit user data provided by Mobius, consisting of personal fitness tracker information from over 30 consenting users.

2. Although the full dataset includes 18 CSV files, I focused on just 2 files for this analysis:

- One file with daily activity 

- Another containing sleep time
  
This narrowed scope allows for a more targeted exploration of users’ daily routines and sleep behavior.

**2.2 Sorting the Data**

1. I used Jupyter Notebook as the development environment and Pandas for data manipulation.

2. The CSV files were downloaded locally to my laptop and then loaded into Jupyter Notebook for analysis.

**2.3 Data Credibility**

1. As a general rule, a sample size of at least 30 users is considered sufficient for drawing meaningful insights. This dataset contains 33 users, which meets that threshold.

2. The data falls within the last 10 years, making it reasonably recent and relevant.

3. The type of data collected closely aligns with Bellabeat’s products, allowing the insights drawn to apply to Bellabeat’s offerings.

**3. Process**

**3.1 Loading Libraries:**
1. Data Preparation

1. I began by importing the necessary Python libraries for data processing and visualization:

   - Pandas and NumPy for data manipulation

   - Seaborn and Matplotlib for creating visualizations

   - Datetime for handling date and time operations

2. Next, I loaded the datasets daily_activity.csv and sleepDaily.csv into the environment for analysis.


**3.2 Data Exploration and Transformation**

1. I began by inspecting the Daily Activity dataset, reviewing the first 10 rows to understand its structure and checking its dimensions.

2. I examined the dataset for duplicate entries and missing values to determine if any data cleaning was necessary.

3. During this review, I noticed that the date column was stored as an object type, so I converted it to a proper datetime format.

4. I also observed that the dataset lacked a day column. To enrich the data, I added a column indicating the day of the week, as well as separate columns for weekday and weekend indicators.

         
   

     
