# Megaline – Prepaid Mobile Plan Analysis

This project analyzes data for the telecommunications company Megaline, which offers two prepaid plans: Surf and Ultimate. The commercial team seeks to understand which plan generates more revenue to optimize the advertising budget.

🧾 Project Description

We analyzed the behavior of 500 customers based on call, text, and internet usage data throughout 2018. The analysis includes:

Data cleaning and preparation

Monthly revenue calculation per user

Descriptive statistics of plan usage

Visualizations to understand user behavior

Statistical tests to validate hypotheses about revenue by plan and region

💡 Objective

Determine, based on statistical evidence, which plan (Surf or Ultimate) generates more average revenue, and explore usage patterns across different regions.

📦 Data Used

The data is organized in five CSV files:

megaline_users.csv: user registration data

megaline_calls.csv: information on calls made

megaline_messages.csv: information on messages sent

megaline_internet.csv: internet usage data

megaline_plans.csv: details of Surf and Ultimate plans

📝 Plan Descriptions

Surf

💵 Monthly price: $20

Includes: 500 min, 50 SMS, 15 GB

Overage charges:

Per minute: $0.03

Per SMS: $0.03

Additional GB: $10

Ultimate

💵 Monthly price: $70

Includes: 3,000 min, 1,000 SMS, 30 GB

Overage charges:

Per minute: $0.01

Per SMS: $0.01

Additional GB: $7

Note: Calls are rounded up to the nearest minute. Monthly web traffic is rounded up to the nearest GB.

⚙️ Project Steps

1. Data Preparation
Data type conversion

Handling missing values and inconsistencies

Monthly usage aggregation per user

2. Revenue Calculation
For each user, monthly revenue was calculated by summing:

Overage charges (minutes, messages, data)

Fixed monthly plan fee

3. Exploratory Analysis
Descriptive statistics (mean, standard deviation, variance)

Usage and revenue histograms

Comparison between plans and regions

4. Hypothesis Testing
Hypothesis 1: The average revenue of Ultimate and Surf plan users is different.

Hypothesis 2: The average revenue of users in the NY-NJ area is different from that of other regions.

📊 Main Tools
pandas, numpy – data manipulation

matplotlib, seaborn – visualizations

scipy.stats – statistical tests

📁 Project Structure
📦 Megaline
├── 📁 data/
│ ├── megaline_calls.csv
│ ├── megaline_messages.csv
│ ├── megaline_internet.csv
│ ├── megaline_users.csv
│ └── megaline_plans.csv
├── 📄 README.md
└── 📄 megaline_analysis.ipynb

✅ Project Status

🟢 Completed – The analysis was successfully conducted, and the findings can help guide strategic decisions regarding advertising and resource allocation.

In comparing the two plans, Ultimate and Surf, the following insights were observed:

The number of calls is consistently higher for Surf users throughout the year, especially in January. In the last four months, this difference narrows.

The minimum usage demand is significantly higher for Surf users.

The average call duration ranges between 400–500 minutes.

Call durations for Ultimate users are longer than Surf users in the first quarter.

Data traffic volume increases in the last quarter.

The null hypothesis that both plans generate equal revenue was rejected.

