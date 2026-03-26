# SUMMARY
WILL THE CUSTOMER ACCEPT THE COUPON? 

Exploratory data analysis project using Python, pandas, Matplotlib, and Seaborn to identify the factors that influence whether drivers accept or reject coupons. Includes statistical summaries, visualizations, key findings, and business recommendations based on UCI survey data.





# DETAILED
WILL THE CUSTOMER ACCEPT THE COUPON? 

Exploratory data analysis project using Python, pandas, Matplotlib, and Seaborn to identify the factors that influence whether drivers accept or reject coupons. Includes statistical summaries, visualizations, key findings, and business recommendations based on UCI survey data.

Project Overview
This project investigates the question: Will a customer accept the coupon? Using survey data from the UCI Machine Learning Repository, I analyzed the differences between customers who accepted a driving coupon and those who rejected it. The notebook applies exploratory data analysis, plotting, statistical summarization, and data visualization to identify patterns in coupon acceptance and translate them into practical recommendations.

This repository was created as Practical Application 1 for the coupon acceptance assignment.

Business Question
Which customer and trip characteristics are associated with a higher likelihood of accepting a coupon?


Dataset
The dataset comes from the UCI Machine Learning Repository and was collected through a survey on Amazon Mechanical Turk. Each observation describes a driving scenario, including variables such as:

destination
time of day
weather
passenger type
coupon type
coupon expiration
customer demographics
venue visit frequency
Target Variable
Y = 1 → coupon accepted
Y = 0 → coupon rejected
Coupon Types
Coffee House
Restaurant(<20)
Carry out & Take away
Bar
Restaurant(20-50)


Tools Used:
Python
pandas
NumPy
Matplotlib
Seaborn
SciPy
Jupyter Notebook/Google Colab


Repository Contents:
prompt.ipynb — completed Jupyter notebook with full analysis and tutor-style explanations
Coupons.csv — source dataset
images — exported charts used for the project
README.md — nontechnical report and summary of findings
Data Cleaning
The original dataset contains 12,684 rows and 26 columns.


Cleaning decisions:
Dropped the car column because it was missing in almost the entire dataset
Dropped the remaining rows with missing values after removing car
Final cleaned dataset size: 12,079 rows
This kept the analysis clean while preserving most of the observations.


Analysis Approach
The notebook follows this workflow:

Load and inspect the data
Check for missing and problematic values
Clean the dataset
Measure the overall coupon acceptance rate
Visualize coupon distributions and acceptance patterns
Complete the required Bar coupon investigation
Perform an independent investigation on Coffee House coupons
Summarize findings, recommendations, and next steps


Key Visualizations:
Distribution of Coupon Types
Acceptance Rate by Coupon Type
Bar Coupon Acceptance by Bar Visit Frequency
Coffee House Coupon Acceptance by Visit Frequency


Summary of Findings:
Overall coupon behavior
Overall coupon acceptance rate: 56.93%

Highest-performing coupon types:
Carry out & Take away: 73.77%
Restaurant(<20): 70.90%

Lowest-performing coupon types:
Bar: 41.19%
Restaurant(20-50): 44.60%



Bar coupon findings:
The assignment-required a Bar coupon investigation that showed strong differences between customers based on their existing bar-going behavior.

Customers who went to bars more than 3 times per month accepted Bar coupons at 76.17%
Customers who went to bars 3 or fewer times per month accepted at 37.27%
Customers who went to bars more than once a month and were over age 25 accepted at 68.98%
The comparison group for that analysis accepted at 33.77%

Customers who went to bars more than once a month, were not traveling with kids, and were not in farming/fishing/forestry accepted at 70.94%
That comparison group accepted at 29.79%

Interpretation:
Bar coupons work much better when the customer already behaves like a likely bar customer. Habit and trip context matter.



Coffee House coupon findings
For the independent investigation, I focused on Coffee House coupons.

Overall Coffee House coupon acceptance rate: 49.63%
Customers who visited coffee houses at least once a month accepted at 65.90%
Infrequent visitors accepted at 34.03%
Coffee House coupons with 1-day expiration performed better than those with 2-hour expiration
Acceptance was highest when the destination was No Urgent Place
Acceptance was lowest when the destination was Home
A strong target segment
(frequent coffee house visitors + 1-day expiration + No Urgent Place + Friend/Partner passenger) accepted at 80.77%
A low-propensity segment
(infrequent visitors + 2-hour expiration + going Home) accepted at 13.54%

Interpretation:
Coffee House coupon acceptance is strongly tied to existing coffee-shop habits, trip flexibility, and expiration timing.



Actionable Recommendations
Target coupons based on existing habits.
People who already visit bars or coffee houses frequently are far more likely to accept matching offers.

Use Bar coupons selectively.
Bar coupons perform best among frequent bar-goers and perform much worse in more family-oriented travel contexts.

Use Coffee House coupons when the customer has flexibility.
Longer expiration windows and “No Urgent Place” trips are much more favorable than short-expiration, home-bound trips.

Keep broad distribution for convenience-focused offers.
Carry out & Take away and Restaurant(<20) already perform well and appear to be good candidates for wider campaigns.

Improve personalization.
Matching coupon type to known customer behavior should increase acceptance rates and improve marketing efficiency.



Next Steps
Build a predictive machine learning model for coupon acceptance
Test which features contribute most to performance
Compare acceptance drivers across all coupon categories
Evaluate whether targeted campaigns outperform untargeted campaigns



Conclusion
The analysis shows that customers are most likely to accept coupons when the offer matches both their existing habits and their current trip context. The strongest coupon strategies are behavior-based targeting for niche offers like Bar and Coffee House, while broader convenience-based offers can be distributed more widely.

Author
Jabari Martin

Source
UC Berkely Engineering, Machine Learning and Artificial Intelligence
UCI Machine Learning Repository dataset provided for the Practical Application assignment.
