# BIS2024
## 1.     Objectives and prerequisites
 
**1.1 Why go into product development?**
 
**- Business Objective**
 
To make it easier to find alternatives to appliances that consume less resources and thus allow the user to save money on utilities.
 
**- Why it will get better than it is now from using ML What we will consider the success of the iteration from a business perspective**
 
*   Use AI to analyze data on current resource consumption(electricity, water, gas), taking into account external factors and predicting future consumption.<br>
*   Evaluate the efficiency of appliances and suggest alternatives (e.g., more energy efficient appliances) based on current energy consumption parameters.
*   Provide personalized advice, for example, based on time of day, weather conditions or user habits.
*   Monitor appliance health in real time to predict breakdowns and improve the longevity of appliances, which can help avoid unnecessary repair or replacement costs.
 
**- What we will consider the success of the iteration from a business perspective**
 
Integration of our system into existing appliance sales companies.
 
**1.2 Business Requirements and Constraints**
 
**- Brief description of BT and links to detailed business requirements documents**
 
*   Database and system for its regular updates
*   Release of own application to the market
*   AI to analyze current user service consumption and predict data based on it
*   AI to suggest the best working alternative to tech based on his consumption history and preferences
*   Developing a user-friendly interface for the user and API for companies
 
**- Business constraints**
 
*   Data privacy, collecting user data information about their consumption data
*   Development and testing within budget and project timeline.
*   Managing dependencies on third-party APIs and keeping the model within financial constraints.
 
**- What we expect from a particular iteration.**
 
<u>First iteration:</u>
Prototyping the core functionality to demonstrate the system's capability.
 
<u>Second iteration:</u>
Running an alpha test 
 
<u>Third iteration:</u>
Analyzing performance on real data and scaling up the system. 
 
<u>Fourth iteration:</u>
Improving the system based on employee feedback and optimizing its performance. 
 
<u>Fifth iteration:</u>
Beta test
 
**- Pilot business process description as far as possible - how exactly will we use the model in the existing business process?**
 
<u>Which BTs will be covered from a technical point of view in the first iteration:</u>
*   Development of a prototype system based on analyzing consumption data and proposing alternatives.
*   Development and testing of a basic API for integration with user databases and third-party services.
*   Development of an interface to visualize current consumption and suggestions.
*   What won't be closed:
*   Deep analysis and forecasting based on multiple external factors (e.g., weather, time of day) will be deferred to later iterations.
*   Integration with external tech sales companies.
*   A full real-time appliance health monitoring system to predict breakdowns.
 
<u>-Which BTs will be covered from a technical point of view for the second iteration:</u>
*   Start collecting data from real users for further analysis.
*   Improving the prediction algorithm based on the collected data.
*   Testing integration with external databases and APIs.
*   Improving the user interface based on feedback from the test group.
 
 
<u>-Which BTs will be covered from a technical perspective for the third iteration:</u>
*   Introduction of additional features to analyze external factors (e.g. weather conditions) in forecasting.
*   Scaling up testing and engagement with real home appliance suppliers.
*   Optimize and improve the accuracy of the appliance condition monitoring system.
 
**- Description of the result in terms of code quality and reproducibility**
*   The code should be structured, support modularity for easy updating of individual parts of the system (analysis algorithms, interface, etc.).
*   The system should be easily deployable in different environments (locally and on a server), using containers (Docker) or CI/CD.
*   Documentation should be complete, with instructions on how to run, configure and use the API.
 
**- Description of planned technical debt**
*   Temporary use of basic forecasting algorithms instead of more sophisticated neural network solutions.
*   Limited integration with external APIs in the initial stages (possibly manually collected data instead of automatic connectivity).
*   Temporary lack of full monitoring and diagnostics of appliances.
 
**- What do we consider a successful pilot? Criteria for success and possible ways of project development**
*   Successful completion of the first iteration: The prototype should be operational and demonstrate the basic functions of the system. Evaluation of success is positive feedback from the first test users.
*   Alpha test: Collect data from real users and improve the model based on them. A successful test is the adaptation of the model to a variety of usage scenarios.
*   Integration with companies: Integration with at least one tech company will be considered a success, allowing the product to scale and offer real solutions to customers.
 
**1.3 What is included in the project/iteration scope, what is not included**
 
<u>Included:</u>
*   Development of a prototype system and basic data analytics.
*   Data visualization and generation of technique replacement recommendations.
*   Basic user interface.
*   API for integration with external databases.
 
<u>Not included:</u>
*   Full-fledged forecasting based on complex factors (time of day, weather, regional peculiarities).
*   Diagnosis and prediction of machinery breakdowns.
*   Full integration with retailers and marketplaces.
 
**1.4 Solution prerequisites**
 
<u>To create a system that meets the needs of the business and users, we consider the following prerequisites:</u>
*   <u>Data used</u>: Interaction with resource consumption data (electricity, water, gas), appliance characteristics, external factors (weather, regional characteristics) and financial indicators (cost of resources in the region). This data will come from user bases as well as external sources via APIs.
*   <u>Forecasting horizon</u>: Consumption forecasting will be for short-term (1-3 months) and medium-term (6-12 months) periods. This will allow users to see both the immediate benefit of replacing appliances and the long-term savings.
*   <u>Model granularity</u>: Forecasts and recommendations will be built at the individual appliance level as well as aggregated at the household level. Additionally, region-level analysis will be considered to account for regional factors and external conditions.
*   <u>Data and technology selection rationale</u>: Using consumption data and external factors, the model can accurately predict future resource consumption and provide personalized recommendations for appliance replacement. Machine learning and time-series forecasting algorithms (e.g., ARIMA, LSTM) will allow processing historical data and suggesting optimal alternatives to users, taking into account their preferences and external conditions.
 
## 2.     Data Scientist methodology
 
**2.1 Problem Statement**
 
From the Data Scientist perspective, the main technical challenges are:
*   Create a system that will analyze resource consumption parameters and suggest some alternatives for home appliances. The model will be based on historical data and characteristics of available appliances.
*   Building predictive models to determine future resource consumption based on time series, including seasonal and external factors, like weather.
*   Integrate business rules to select the most efficient solutions in terms of machinery replacement. The system will take into account user preferences and utility cost reduction goals.
*   Identify unexpected consumption spikes that may indicate malfunctioning appliances or changes in user habits.
 
**2.2 Solution Block Diagram**
 
Baseline block diagram (Baseline):
1.         Data Preparation:
Collecting and processing data on resource consumption, machine characteristics and external factors (weather, regional tariffs).
Data validation and cleaning.
2.        Building predictive models:
Application of time series models to forecast consumption.
3.        Recommender system:
Create a model that will suggest alternatives for appliances based on analysis of current consumption and device characteristics.
4.        Testing and Optimization:
Conducting A/B testing of recommendations and predictions.
Optimizing algorithms based on feedback and performance.
5.        Closing technical debt:
Improving the architecture, optimizing the model to handle real user data, reporting and making recommendations to the business.
 
MVP block diagram:
1.        Data Preparation:
Creating a data showcase with a complete set of historical data on consumption, technique characteristics and external factors.
2.        Business rules integration:
Defining technique selection rules and recommendations based on business metrics and resource consumption reduction goals.
3.        Preparation of forecasting models and recommendations:
Integrating time series models and recommendations into a single pipeline.
4.        Testing on real data:
Model validation on real-time user data.
5.        Pilot training:
Deploying the model to a limited number of users and collecting feedback.
 
**2.3 Stages of problem solving**
 
**Step 1: Data preparation (Baseline and MVP)**
 
- Data and Entities:
Historical consumption data, machinery characteristics, weather data, and resource tariffs.
Data source: internal databases, APIs of external data providers (e.g., weather services).

- Data Quality:
Checking for data completeness, eliminating anomalies.
Expected outcome: ready data for model training and testing.
 
**Step 2: Build predictive models**
 
- Baseline:
Apply standard time series models (ARIMA, Prophet) to forecast consumption.
Expected outcome: baseline consumption forecasts for short and medium time horizons.
 
- MVP:
Implementation of more complex models like LSTM that take into account additional parameters (e.g., time of day, weather conditions).
Expected outcome: Improved forecast accuracy through the use of more complete data analysis techniques.
 
**Step 3: Recommendation System**
 
- Baseline:
Use of a simple system based on predefined rules (e.g., replace appliances when a certain consumption level is exceeded).
Expected outcome: baseline recommendations for replacing appliances.
 
- MVP:
Utilize more flexible systems using machine learning (e.g., collaborative filtering algorithms or content-based recommendations).
Expected outcome: personalized recommendations for each user.
 
**Step 4: Model testing and interpretation**
 
- Baseline:
A/B testing on a small amount of data to evaluate system performance.
Expected outcome: prediction and recommendation metrics for the Baseline model.
 
- MVP:
Conduct full-scale testing with real users and business metrics (reduced resource consumption, improved savings).
Expected outcome: models with high prediction accuracy and quality recommendations.
 
**Step 5: Optimization and preparation of the pilot**
 
- Baseline:
Optimization of existing models and calculation of business metrics.
Expected outcome: improved performance metrics and forecast accuracy.
 
- MVP:
Deployment of the system for pilot and collection of user experience data.
Expected outcome: model adaptation based on real data and user feedback.
 
**Step 6: Business Rules Integration**
 
- Baseline:
The baseline version of the model integrates simple predefined business rules (e.g., energy consumption threshold or frequency of machinery use).
Expected outcome: improved accuracy of forecasts and recommendations based on business metrics such as machinery replacement cost or annual energy consumption.
 
- MVP:
More sophisticated business rules that can take into account additional factors: user preferences, budget constraints, seasonal changes in energy rates.
Expected outcome: personalized recommendations based on complex rules and integration of these rules with forecasting and recommendation algorithms.
 
**Step 7. Optimizer development**
 
- Baseline:
The simplest optimization approaches based on selecting the most energy-efficient technique options will be used to test recommendations.
Expected outcome: a baseline model for selecting optimal solutions to reduce utility costs.
 
- MVP:
The optimizer will also take into account parameters such as projected increase in appliance life, maintenance costs, and individual user preferences.
Expected outcome: an intelligent system that can offer comprehensive solutions to reduce utility costs and increase appliance longevity.
 
**Step 8: Prepare the final report for the business**
 
- Baseline:
Create reports that will contain key metrics such as accuracy of consumption forecasts, recommendation effectiveness scores, and savings rates for users.
Expected outcome: baseline reports to evaluate system performance.
 
- MVP:
Produce more detailed reports that include detailed analysis of system performance, savings projections for each user, and feedback on technique usage.
Expected Result: analytical reports that allow strategic decisions to be made for further development of the system.
 
Description of planned technical debt:
- Technical Debt
Improve data quality (e.g., real-time validation of incoming data), and optimize algorithms to handle large amounts of data, identify and account for external factors.
 
## 3. Pilot training
 
**3.1 How the pilot will be evaluated**
 
The evaluation of the pilot will be based on the following approach:
A limited group of users (e.g. 100-500 people) will be selected to test the recommendation and prediction system. Data will be collected on their technique consumption and feedback on the suggested recommendations. A/B testing is applied: one group receives recommendations from the system, the other group uses their technique without modification.
 
Evaluation methods:
·      Prediction accuracy metrics: We compare predicted and actual resource consumption rates.
·      User satisfaction: Survey users about the recommendations offered, the usability of the interface, and their understanding of the proposed alternatives.
·      Economic Impact: Evaluate the reduction in utility costs for users who followed the recommendations.
 
The evaluation will be based on analyzing these metrics over time and comparing them to a control group.
 
**3.2 What is considered a successful pilot**
 
The success of the pilot will be determined by the following formalized metrics:
 
*   Forecast Accuracy: Consumption forecast error is not meaningful (e.g., MAPE < 10% at a forecast horizon of 3 months).
*   Acceptance of recommendations: Over 70% of users who are offered alternative devices are expected to take up recommendations or express willingness to consider them.
*   Resource savings: On average, a 15-20% reduction in resource consumption for users who follow the system's recommendations.
*   User Satisfaction: More than 80% of users should rate the system a 4+ out of 5 on the satisfaction scale.
 
**3.3 Pilot Preparation**
 
To ensure the computational efficiency of the pilot, the following measures will be taken:
 
*   Expected computational cost: 
During the pilot phase, the system will be deployed on a limited scale. The required resources for model performance, including forecast recalculation frequency and recommendations, will be calculated. If necessary, the model will be optimized to run with less data or using less resource-intensive models for real-time predictions.
 
*   Refinement of computational complexity parameters: 
Computational cost data (e.g., number of operations and required memory for each prediction) will be collected during the baseline experimentation phase. This will allow the pilot parameters to be adjusted, limiting the frequency of updates and optimizing the processes for real-world workloads.

## 4. Implementation for production systems
 
**4.1 Solution Architecture**
 
Block diagram of the solution:
1. Frontend (User Interface):
*   Displays recommendations to users in the application.
*   Collects data about user habits.
*   Connects via API to the backend service.
2. Backend (Main Server):
*   Responsible for processing user data.
*   Interfaces with consumption and recommendation databases.
*   Generates forecasts and recommendations using ML models.
3. ML Engine:
*   Module to perform consumption and recommendation analysis.
*   Uses trained models to predict consumption and find alternative devices.
4.             Database:
*   Stores data on consumption, user preferences, and devices.
5.             API Gateway:
*   Enables communication between Frontend and Backend services.
 
**Main API methods:**
- Receive consumption data: o GET /consumption
- Generating recommendations: POST /recommendations
- Getting forecasts: POST /forecast
 
**4.2 Description of infrastructure and scalability**
 
**Infrastructure:**
Choice of cloud provider: 
*   Cloud infrastructure (e.g. AWS, GCP, Azure) is used to provide flexibility and scalability.
 
Reasons for selection:
*   Ease of scaling the system as the load increases.
*   Ability for automatic load balancing and fault tolerance.
*   High level of data security.
 
Pros:
*   Reduced cost of in-house infrastructure.
*   Flexibility in customization of services and their scaling.
 
Minuses:
*   Dependence on third-party vendors.
*   Potential risks of failures on the cloud provider's side.
 
Why the chosen solution is better than others:
*   Cloud-based solutions provide fast integration, high availability, and out-of-the-box tools for deploying ML solutions.
 
**4.3 System Performance Requirements**
 
SLA (Service Level Agreement):
*   99.9% service availability.
*   Ability to process up to 10,000 requests per minute.
*   Average response time of no more than 500 ms for standard requests and up to 2 seconds for complex operations (e.g., forecast generation).
 
**4.4 System Security**
 
Potential vulnerabilities:
*   API vulnerabilities: Possible attacks through API weaknesses such as flaws in authentication and authorization.
*   DDoS Threats: The system may be overloaded due to targeted attacks.
 
Security measures:
*   Protecting the API with tokens and OAuth 2.0.
*   Application of traffic monitoring system and DDoS protection.
 
**4.5 Data Security**
 
GDPR Compliance:
*   User Data Processing: All user data must be processed in compliance with GDPR, including users' explicit consent to data collection.
*   Anonymization: Personal data must be anonymized or pseudonymized when processed for analysis.
 
Data security principles:
*   Encryption of data in transit (TLS).
*   Encryption of data at rest (e.g., AES-256).
*   Regular security audits and protection against data leakage.
 
**4.6 Costs**
 
Estimated Costs:
*   The approximate cost of running the system in the cloud is about $2000-$5000 per month, depending on the volume of queries and the intensity of computing resources for predictions and recommendations.
*   Approximate cost of $500 per month to store user data.
 
**4.7. Integration points**
 
Interaction between services:
*   Frontend ↔ Backend: Interaction APIs to retrieve consumption data and display recommendations to users.
*   Backend ↔ ML Engine: Calls to generate forecasts and recommendations based on user data.
*   Backend ↔ Database: Storage of consumption history and parameters of user devices.
 
**4.8 Risks**
 
Main risks:
*   Lack of data: Limited consumption data may affect the accuracy of predictions.
*   Recommendation errors: Incorrect recommendations may cause user dissatisfaction.
*   Dependence on third-party APIs: Problems with third-party APIs can cause system failures.
 
Risk management measures:
*   Develop backup methods of operation when data is unavailable.
*   Continuous monitoring of models and retraining them on new data.
*   Implement testing and monitoring to detect bugs early.




