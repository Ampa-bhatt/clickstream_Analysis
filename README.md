# clickstream_Analysis
 Clickstream Analysis for E-commerce Website

This project involves analyzing a large dataset with over 1.3 crore rows of clickstream data. The analysis is divided into four main parts: descriptive analysis, data visualization, model creation, and prediction. The goal is to derive actionable business insights and conclusions to optimize customer navigation and increase conversions.

Methodology

1. Data Cleaning and Transformation

Regex for Data Cleaning: Regular expressions were used to clean and transform the data.

Session Identification: Sessions were created by grouping clicks based on user behavior and timestamps.

Bot Session Removal: Identified and removed bot sessions to ensure data integrity.

2. Data Visualization and Interpretation

Data visualization was performed based on five key objectives:

Time Spent on Each Page: Calculated the time difference between consecutive timestamps to estimate time spent on each page.

Call-to-Action (CTA) Pages: Identified CTA pages based on specific keywords and analyzed user interactions.

Most/Least Visited Pages: Determined the frequency of visits to each page.

Exit Pages: Analyzed the last page visited by users in a session.

Clicks per Session: Plotted the number of clicks per session against the number of users.

3. Predictive Modeling

Click Prediction: Using clicking patterns (sequences of 3 clicks), the 4th click was predicted. This process was repeated to predict the 5th click, then the 6th click using the 3rd, 4th, and 5th clicks. This analysis revealed user navigation paths and intentions, distinguishing between CTA and non-CTA customers.

Model Used: Long Short-Term Memory (LSTM), a type of Recurrent Neural Network (RNN), was used for prediction.

Edit Distance: Levenshtein distance was calculated to measure string dissimilarity, helping identify non-CTA customers who are convertible. Lesser values indicate higher similarity and potential for conversion.

4. Business Insights

The model's purpose is to optimize customer navigation and predict when to prompt non-CTA customers to visit CTA pages, ultimately leading to conversions.

Observations and Conclusions

Session Analysis

Clicks per Session: The maximum estimated clicks per session are 40, 50, and 60, with a session timeout considered at 10, 20, and 30 minutes. Based on trials, 40 clicks per session with a 30-minute timeout showed the most rational and realistic outcomes.

Session Timeout: While a 20-minute timeout is also feasible, 30 minutes was considered standard for this analysis.

Abnormal Conditions: Timestamps and durations showing anomalies or contradictions were voided.

Exit Pages

Exit Page Analysis: The time delta function calculated the difference between sequential timestamps to estimate the time spent on exit pages.

Optimization and Targeting

High Click Rates: Sessions with higher-order clicks show a drop rate, indicating diminishing user interest.

CTA Navigation: The model predicts clicking patterns to identify when and how to navigate non-CTA customers to CTA pages. Prompts can be designed to guide users effectively.

Conclusion

This project demonstrates how clickstream data can be analyzed to understand user behavior, optimize navigation paths, and improve conversion rates. By identifying key patterns and leveraging predictive models, e-commerce businesses can enhance user experience and drive targeted strategies for customer retention and sales.
