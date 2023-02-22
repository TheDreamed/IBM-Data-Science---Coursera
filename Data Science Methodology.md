Data Science Methodology
    Methodology - Systems of methods used in a particular area of study or activit.y

Data Science Methodology aims to answer the following 10 questions in this prescribed sequence:

From problem to approach: 
    1. What is the problem that you are trying to solve?
    2. How can you use data to answer the question?

Working with the data:
    3. What data do you need to answer the question?
    4. Where is the data coming from (identify all sources) and how will you get it?
    5. Is the data that you collected representative of the problem to be solved?
    6. What additional work is required to manipulate and work with the data?

Deriving the answer:
    7. In what way can the data be visualized to get the answer that is required?
    8. Does the model used really answer the initial question or does it need to be adjusted?
    9. Can you put the model into practice?
    10. Can you get constructive feedback into answering the question?


CRISP-DM(Cross-Industry Standard Process for Data Mining)
    - a process aimed at increasing the sue of data ming over a wide variety of business applications and industries.

Crisp-DM model 
    1. Business Understanding - This is where the intention of the project is outlined.
    
    2. Data Understanding - Relies on business understanding. Data is collected at this stage of the process. CRISP-DM combines the stages of Data Requirements, Data Collection, and Data Understanding from the Foundational Methodology Outline.

    3. Data Preparation - Data must be transformed into a useable subset unless it is determined that more data is needed. Must be checked for questionable, missing, or ambiguous cases.

    4. Modeling - Once prepared  for use, the data must be expressed through models, give meaningful insights, and hopefully new knowledge. The use of models reveals patterns and structures within the data that provide insights to the features of interest. 

    5. Evaluation - The selected model must be tested. This is usally done by having a pre-selected test, set to run the rained model on.

    6. Deployment - The model is used on new data outside of the scope of the data set and by new stakeholders. The new interactions at this phase might reveal the new variables and needs for the dataset and model. Revisions are often found after deployment.


From Understanding to Approach 
    
    Business understanding -  What is the problem that you are trying to solve?

    Analytic approach - How can you use data to answer the question?

    Seeking Clarification - What's the goal?
     
    Supporting the Goal - Break down the objectives.

    Getting stakeholder "buy-in" and support

    Case Study -  Applying concepts (Health Care)

    Question: Best way to allocate limited health care budget.

    Goals - To provide quality care without increasing cost.
    Objectives - Review the process to identify inefficiencies.

    What's the sponsor's involvement
    1. Set overall direction.
    2. Remained engaged and provide guidance.
    3. Ensured necessary support, where needed.

    Business Requirements
    1. Predicting readmissions outcome (Y or N) for each patient with CHF
    2. Predicting readmission risk for each patient
    3. Understanding explicitly what combination of events led to the predicted outcome for each patient
    4. Easy to understand and apply to new patients to predict their readmission risk.

Analytic Approach 
    
    Pick analytic approach based on type of question

    Descriptive
    - Current Status

    Diagnostic (Statistical Analysis)
    - What happened?
    - Why is this happening?

    Predictive
    - What if these trends continue?
    - What will happen next?
    
    Prescriptive
    - How do we solve it?


    What are the types of questions?
     The correct approach depends on business requirements for the model.


    If the question is to determine probabilities of an action
    - Use a Predictive model

    If the question is to show relationships
    - Use a decriptive model

    If the question requires a yes/no answer
    - Use a classification model

    Machine Learning
    - Learning without explicitly programmed.
    - Identifies relationships and trends in t


    Case Study - Decision tree classification selected!

    Predictive model 
        - To predict an outcome
    
    Decision Tree classification
        - Categorical outcome
        - Explicit "decision path" showing conditions leading to high risk
        - Likelihood of classified outcome
        - Easy to understand and apply

Data requirements - Cooking with data 

    From Requirements to Collection
        Data Requirements 
            - What are data requirements?
        Data Collection
            - What occurs during data collection?
    

    Case Study 
    
    Define and select cohort
        - In-patient within health insurance provider's service area
        - Primary diagnosis of CHF in one year.
        - Continuous enrollment for at least 6 months prior to primary CHF admission
        - Disqualifying conditions
    
    Content, formats, representations suitable for decision tree classifier.
        - One record per patient with columns representing variables(dependent variable and predictors)
        - Content covering all aspects of each patient's clinical history
            - Transactional format 
            - Transformations required. 

    
    Data collection - Ingredients?

        From Requirements to Collection
            Data Requirements
                - What are data requirements?
            Data Collection
                - What occurs during data collection  
    
    Case Study - Gathering available data

        Available data sources
            - Corporate data warehouse (single source of medical and claims, eligibility, provider, and member information)
            - In-patient record system
            - Claim payment system
            - Disease management program information

    Case Study - Deferring Inaccessible data
        
        Data wanted but not available
            - Pharmaceutical records
            - Decided to defer

    Case Study - Merging data

        Eliminate redundant data

    

Understanding the Data
    
    From Understanding to Preparation
        
        Data Understanding
            - What does it mean to "prepare" or "clean" data?
        Data Preparation
            - What are ways in which data is prepared?
    

    Case Study - Understanding the data
        
        Descriptive statistics
            Univariate statistics
            Pairwise correlations
            Histogram 

    Case Study - Looking at data quality

        Data quality
            - Missing values
            - Invalid or misleading values.

    Case study - This is an iterative process

        Iterative data collection and understanding
            - Refined definition of CHF admission.

    Data preparation - Cleansing Data

            Transforming data to be easier to work with

    Using domain knowledge
         
         Feature Engineering - the process of using domain knowledge of the data to create features that make the machinelearning algorithms work.

    Working with text analysis


    Case Study - Data Preparation

    Actually define Congested Heart Failure

    1. Set of diagnosis
    2. CHF is only one type of heart failure

    Defining readmission.

    1. Timing of events are evaluated whether one is an index admission or first time or not.


    Case Study -  Defining CHF admission
    
        Define CFF admission and CHF Readmission
    
    Case Study - Aggregating records
        
        Transactional records
            - Claims: professional provider, facility, pharmaceutical
            - Inpatient and outpatient records: diagnoses, procedures, prescriptions, etc.
            - Possibly thousands per patient depending on clinical history.
    
    Aggregating to patient level
        
        Roll up to 1 record per patient
        Create new columns representing the transaction
        Outpatients visits/Inpatient episodes: frequency, recency, diagnoses/ length of stay, procesdures and prescriptions.
        Comorbidities with CHF

    More or less data needed?

        Literature review of important factors for CHF readmission
        
        Loop back to data collection stage and add additional data, if needed. 
    
    Completing the data set

        Merge all data into one table
            - One record per patient
            - List of variables used in modeling
                - Target: CHF readmission with 30 days (Yes/No), following discharge from CHF hospitalization.

    Using training sets
     Cohort: 2,343 patients

     Randomly divided into training and testing sets: 70% / 30% split.

     Training: 1,640 patients
     Testing: 703 patients
     