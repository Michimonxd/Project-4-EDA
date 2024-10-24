Vanguard CX Digital Experiment: Data Analysis Project
Project Brief
This project analyzes the results of a digital experiment conducted by Vanguard, a U.S.-based investment management company. As a newly employed data analysts on Vanguard's Customer Experience (CX) team, We were tasked with interpreting and uncovering insights from the experiment results to assist the team in evaluating the impact of a new User Interface (UI) and in-context prompts on customer behavior.
Context
In an effort to modernize its online services, Vanguard hypothesized that a more intuitive User Interface (UI), combined with timely in-context prompts—such as cues, messages, hints, or instructions given to users during their interactions—could improve the online experience and encourage more clients to complete their processes. My role is to analyze the data from this experiment to determine if these changes had the desired effect.
Digital Experiment
An A/B test was conducted between March 15, 2017, and June 20, 2017. The test had two groups:
* Control Group: Clients interacted with Vanguard’s traditional online process.
* Test Group: Clients experienced the updated, more modernized digital interface.
Both groups navigated through the same sequence of steps: an initial page, followed by three sequential steps, and a final confirmation page. The goal of this experiment was to determine whether the updated design led to an improved user experience and increased process completion rates.
________________
Data Tools
This project relies on three datasets:
1. Client Profiles (df_final_demo): Contains demographic information such as age, gender, and account details for each client.
2. Digital Footprints (df_final_web_data): Detailed tracking of client interactions on Vanguard's website. The data is split into two parts (pt_1 and pt_2), which need to be merged for a full analysis.
3. Experiment Roster (df_final_experiment_clients): A list identifying which clients participated in the experiment, either in the control group or the test group.
________________
Work Summary
The project began with an initial review of all the data tables. Two parts of the digital footprint dataset were merged to create a unified dataset, which was then combined with the client participation data to explore the relationship between user behavior and the experiment. An exploratory data analysis was performed on this combined dataset to understand the context and relevance of each data point.
After cleaning the data, missing values in the client demographic dataset were handled by filling in NaN values. For instance, missing gender entries labeled as "X" were replaced with "Unknown." Rows with missing values, except for client IDs, were dropped to ensure data integrity.
Next, calculations were performed to determine the proportion of clients who reached each step of the process, both overall and for the control and test groups. These calculations revealed a difference of less than 5% in completion rates between the two groups, suggesting that the new UI had a minimal effect on completion. Errors were defined as clients going back a step, getting stuck, or having their session interrupted. The error rate was calculated for each group.
Step durations were analyzed by sorting the dataset based on client_id, visitor_id, visit_id, and date_time, and calculating the time between each step. The client journey was defined as:
   1. Start: Open UI
   2. Step 1: Searching for investment options
   3. Step 2: Choosing a product
   4. Step 3: Selecting an investment amount
   5. Confirmation: Making the investment
During the analysis, some inconsistencies were identified in the client data, such as clients with a tenure longer than their age. These issues were resolved, and clients were categorized into age groups: "Teen" (20 years or younger), "Adult" (20–60 years), and "Senior" (over 60 years).
To assess the impact of the UI redesign, hypotheses were formulated around key performance indicators (KPIs), such as completion rates, average step duration, and error rates. A series of two-sided t-tests were conducted to evaluate these hypotheses. The results showed statistically significant differences in completion rates between the control and test groups, as well as differences based on gender.
Additional hypotheses related to age and tenure were later introduced and tested, followed by further calculations and visualizations. The findings were ultimately presented through a series of graphs created in Python and Tableau.
The project concluded with the development of a comprehensive narrative summarizing the conclusions, key insights, and challenges faced during the analysis. The results were formalized and presented in a detailed report, supported by visualizations.