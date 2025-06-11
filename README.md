## Step 1: Ask — Define the Business Task

Bellabeat wants to explore how smart device users (via Fitbit data) engage with their health and wellness habits, specifically around physical activity and sleep. The goal is to uncover behavioral patterns that can inform targeted marketing strategies for Bellabeat's wellness products.

As a junior data analyst on the marketing analytics team, I have been tasked with analyzing Fitbit user data and applying insights to support the promotion of **Bellabeat's Time wellness watch**, which tracks activity, stress, and sleep.

This case study aims to:
- Identify trends in activity and sleep behavior
- Determine how these trends align with Bellabeat’s product offerings
- Develop data-driven marketing recommendations to increase user engagement and product adoption


## Step 2: Prepare — Describe the Data

**Data Source**:  
The dataset is publicly available on Kaggle: [Fitbit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit).  
It includes anonymized data from 30 Fitbit users collected over 1 month.

**Files Used in This Analysis**:
- `dailyActivity_merged.csv`: Contains daily summaries of steps, distance, calories burned, and minutes spent in different activity intensities.
- `sleepDay_merged.csv`: Contains sleep data including total minutes asleep, time in bed, and number of recorded sleep sessions per day.

**Data Structure**:
- The data is in **wide format**, with each row representing a user on a specific day.
- Data is joined by `Id` (unique user ID) and date (`ActivityDate` or `SleepDay`).

**Limitations**:
- Only 30 users participated; results may not generalize to a broader population.
- The data reflects a short time span (approx. 1 month).
- Sleep data is not available for every user on every day.
- No demographic attributes (age, gender, region) are included.

**Integrity**:
- Data appears to be clean and well-structured, though some inconsistent formats were corrected during the processing step.


## Step 3: Process — Cleaning and Data Preparation

**1. Removed Duplicate Records**
- Both `dailyActivity_merged.csv` and `sleepDay_merged.csv` were checked for duplicates and
  null values to ensure that I had a clean data.

**2. Standardized Date Columns**
- `ActivityDate` in daily activity data and `SleepDay` in sleep data were both converted to `datetime` format using `pd.to_datetime()`.
- Extracted only the date (no time) for consistent merging: `.dt.date`

**3. Added Derived Columns**
- `DayOfWeek`: extracted from the date for both activity and sleep datasets using `.dt.day_name()`.
- `SleepEfficiency`: calculated as `(TotalMinutesAsleep / TotalTimeInBed) * 100`.

**Outcome**:
The data is now clean and structured for analysis. While merging was considered, current insights are based on separate exploration of sleep and activity datasets.


## Step 4: Analyze — Key Findings from Activity and Sleep Data

### 🏃‍♂️ Activity Analysis:
- Most users are sedentary, with very limited time spent in high-activity zones.
- Calories burned positively correlate with Total Steps (Just to test it)
- Weekday activity is slightly higher than on weekends, especially Tuesday through Thursday.

### 😴 Sleep Analysis:
- Users average around 7 hours of sleep with high sleep efficiency (~91.7%).
- Weekend sleep duration is longer than weekday sleep, indicating a catch-up pattern.
- Sleep efficiency is stable throughout the week.

### 💡 Strategic Insights:
- Bellabeat can schedule motivational nudges midweek when users are already active.
- Targeting sedentary users with wellness coaching and movement reminders is a clear opportunity.
- Promote weekday sleep consistency with relaxation content and reward consistent users.


## Step 5: Share — Communicating the Insights

To share the results with Bellabeat’s executive and marketing team, key findings are presented using clear, visual summaries supported by concise insights:

### 📊 Key Visuals Created:
1. **Activity Level Pie Chart** — Showed that ~80% of users are sedentary.
2. **Steps vs Calories Scatterplot** — Demonstrated a positive relationship between steps and calories burned.
3. **Bar Chart: Activity by Day of Week** — Revealed midweek activity peaks (Tuesday–Thursday).
4. **Bar Chart: Sleep Duration by Day** — Highlighted longer sleep durations on weekends.
5. **Dual-Axis Plot: Sleep Efficiency & Duration** — Illustrated consistent sleep efficiency with variable sleep length.

### 🎯 Sharing Strategy:
- Focus messaging on how Bellabeat’s **Time watch** supports better daily movement and sleep recovery.
- Use visuals to drive key talking points in presentations, dashboards, or stakeholder summaries.
- Ensure plots are labeled clearly with brief bullet-point insights attached for accessibility.

## Step 6: Act — Strategic Recommendations for Bellabeat

Based on the analysis of Fitbit activity and sleep data, the following high-level strategies are recommended for promoting the Bellabeat **Time** wellness watch:

### 1. Target Sedentary Users with Lifestyle Coaching
- Create onboarding journeys for new users labeled "Sedentary Starter" or "Wellness Beginner"
- Promote Time's inactivity reminders and step tracking as habit-building tools

### 2. Time Campaigns Around Midweek Engagement
- Launch challenges or nudges on **Tuesday–Thursday**, when users are naturally more active
- Reinforce ongoing activity streaks during these high-engagement days

### 3. Promote Weekday Sleep Support Features
- Use Sunday and Monday to push relaxing content (e.g., guided sleep meditations, stress tracking)
- Highlight Time’s ability to improve **sleep consistency**, not just duration

### 4. Reward Consistency & Recovery
- Celebrate users with **high sleep efficiency** or weekly streaks using badges or messages in the app
- Frame the Time watch as a **recover**




