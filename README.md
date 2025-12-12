# Team_2_Genomics
Smart Anticoagulant Dosing Through Precision Medicine


# 1. Company Overview 
GenexaHealth Insights is a Utah-based precision health company founded in 
2008 by bioinformatics researchers, data engineers, and clinical 
pharmacologists. The mission is to make genomic testing and personalized 
healthcare accessible to consumers, hospitals, and insurers by converting 
complex genetic and clinical data into safe, actionable medical decisions. 
Growth & Milestones 
● 2010: Launched first consumer DNA testing kit. 
● 2014: Expanded into pharmacogenomics with drug-response testing. 
● 2017: Partnered with hospitals to integrate pharmacogenomic reports 
into EHRs. 
● 2021: Introduced AI-driven clinician and patient dashboards for 
personalized care pathways. 
● 2024: Established an enterprise data platform with real-time clinical 
data feeds, enabling large-scale pharmacogenomic research and 
production-grade ML.


# Market Presence 
● 15M+ customers across patients, hospitals, insurers, and pharma 
partners. 
● Integrated with leading EHR vendors and payer systems. 
● Partnerships with academic research centers and global insurance 
providers for clinical studies and reimbursement models. 
2. Business Challenge 
Warfarin is still one of the most commonly prescribed anticoagulants 
worldwide, but it has a narrow therapeutic window. Small dosing errors can 
cause severe bleeding or clotting events, leading to hospitalizations, 
disability, or death. Despite existing guidelines and INR monitoring, most 
prescribing workflows do not fully integrate genetic variants, clinical history, 
and lifestyle data in a systematic, real-time way. This results in: 
Impact on Patients 
● Safety Risks: Incorrect doses increase the risk of hemorrhage (high 
dose) or thrombosis (low dose). 
● Trust Erosion: Patients hear about “personalized medicine,” yet are 
often given generic dosing protocols. 
● Quality of Life: Lengthy stabilization periods (weeks to months), 
frequent INR tests, dose adjustments, and anxiety about side effects. 




# Impact on Hospitals 
● Clinical Liability: Warfarin-related adverse drug events (ADEs) are a 
leading cause of medication-related readmissions. 
● Financial Strain: Each ADE can cost thousands of dollars in extended 
length of stay, labs, and interventions. 
● Operational Load: Clinicians spend significant time doing trial-and-error 
dosing instead of using data-driven tools. 
Impact on GenexaHealth 
● Proof of Value: Hospitals and insurers need clear evidence that 
pharmacogenomic-guided dosing improves outcomes and reduces 
costs. 
● Competitive Pressure: Other players are deploying AI-based dosing 
tools; differentiation requires data quality, robustness, and 
explainability, not just models. 
● Revenue Risk: Without demonstrable ROI, large-scale contracts with 
hospital systems and payers are at risk. 





# 3. Rationale for the Project 
Pharmacogenomic-Guided Anticoagulant Dosing 
The project integrates genomic variants (e.g., CYP2C9, VKORC1), clinical data 
(age, weight, comorbidities, concomitant meds), and lifestyle factors (diet, 
alcohol, adherence) into a single dosing recommendation engine. 
Goals 
● Reduce bleeding and clotting events. 
● Accelerate time to stable INR. 
● Automate and standardize dosing decision support at the point of care. 
Real-World Context 
● Regulatory bodies and clinical guidelines increasingly recommend 
genetic considerations for Warfarin dosing. 
● Leading health systems already integrate pharmacogenomic data into 
their EHR decision support. 
● AI-driven genomics is being used in drug development and clinical 
trials, creating expectations for similar rigor in clinical practice.



# Strategic Reasons 
● Patient Safety: Reduce Warfarin-related adverse events. 
● Regulatory Alignment: Stay ahead of precision medicine requirements 
and payer expectations. 
● Market Differentiation: Provide a clinically validated, AI-enabled, and 
explainable dosing solution. 
● Trust Building: Show clear, individualized recommendations supported 
by data and explainability. 
● Operational Efficiency: Reduce clinician burden with decision support 
and automate monitoring at scale. 
4. Cross-Functional Roles & Objectives 
This is a multi-disciplinary program combining clinical expertise, data 
analytics, data science, and business leadership. 
4.1 Data Analytics (DA) 

# Core Responsibilities 
● Explore the Data: Get familiar with the dataset, understand its 
structure, and check for any issues (missing data, outliers, etc.). 
● Analyze Patient and Clinical Data: Use the data to measure key metrics 
like how long it takes patients to stabilize their INR (time to stabilization) and how often they experience bleeding/clotting events 
(adverse events). 
● Create dashboards and reports for clinical and business stakeholders.

# Key Objectives 
1. Prepare and Clean the Data 
● Handle missing values and fix any inconsistencies in the data. 
● Convert categorical data (like Sex, Ethnicity, Hypertension) into 
a usable format for analysis. 
2. Analyze Key Metrics 
● Time to INR Stabilization: Calculate how long it takes for patients 
to stabilize their INR levels (INR_Stabilization_Days). 
● Adverse Events: Track how often patients experience bleeding or 
clotting events (Adverse_Event), and see if there are patterns 
related to medications or conditions. 
● Therapeutic Range Control: Calculate what percentage of 
patients are in the therapeutic range at key time points (e.g., 
days 3, 7, 10, and 30 using TTR_pct). 
3. Create Dashboards to Visualize Data 
● Build dashboards showing key metrics like: 
○ How long it takes patients to stabilize INR. 
○ The rate of adverse events. 
○ The percentage of patients within the therapeutic range 
over time. 
4. Generate Reports on Current Performance 
● Provide a clear snapshot of the current state of Warfarin dosing: 
○ Average time to INR stabilization. 
○ Percentage of patients experiencing adverse events. 
○ The overall effectiveness of Warfarin therapy (e.g., how 
many patients are within the therapeutic range). 




# 4.2 Data Science (DS) 
Core Responsibilities 
● Clone the project repo and pull the curated datasets from the API into 
the GitHub repository. 
● Develop models for initial dose prediction and ongoing dose 
adjustment. 
● Ensure explainability and robust validation. 
Key Objectives 
● Train and compare: 
○ Baseline models (linear regression, Random Forest). 
○ Deep learning models that handle multimodal inputs. 
● Evaluate models on: 
○ RMSE/MAE for dose prediction accuracy. 
○ Predicted vs simulated time-in-therapeutic range (TTR). 
○ Clinical surrogate metrics like % of patients within the 
therapeutic range at key time points. 
● Use LIME to generate per-patient explanations and permutation 
importance for global feature importances. 
● Check in model training notebooks, configuration files, and MLflow 
experiment links within GitHub (/models/, /notebooks/). 

# 4.3 Business Analysis (BA) 
Core Responsibilities 
● Capture requirements from clinicians, IT, compliance, and insurers. 
● Map current vs future state workflows for Warfarin dosing. 
Translate these into functional requirements for data, models, and 
dashboards. 
Key Objectives 
● Maintain a requirements traceability matrix stored in GitHub 
(/docs/requirements/). 
● Define key KPIs: 
○ 25% reduction in bleeding events within 6 months. 
○ Target % of patients reaching therapeutic INR in <10 days. 
○ ROI per hospital (cost savings vs implementation cost). 
● Partner with DA to build business cases using the analytics generated 
from GitHub-hosted datasets. 



# 4.4 Project Management Office (PMO) 
Core Responsibilities 
● Coordinate work across DA, DS, BA, and clinical stakeholders. 
● Use Agile with 1-week sprints and Snowflakes issues/boards (plus Jira if 
used) for task tracking.
● Ensure everything is documented and versioned in GitHub (code, data, 
docs). 
Key Objectives 
● Keep the roadmap updated in /docs/roadmap/ (or linked from 
Confluence but referenced in GitHub). 
● Facilitate sprint planning, reviews, and retros focused on delivering: 
○ Data pipelines 
○ Curated datasets 
○ Models and evaluation results 
○ Pilot deployment assets 


# 4.5 Governance, Risk & Compliance (GRC) 
Core Responsibilities 
● Establish and enforce data governance policies for protected health 
information (PHI) and genetic data across all project phases. 
● Assess regulatory requirements including HIPAA, GINA, HITECH, and FDA 
guidance on Software as a Medical Device (SaMD) and Clinical Decision 
Support. 
● Conduct risk assessments for data handling, model deployment, 
third-party integrations, and clinical decision support workflows. 
● Define and monitor compliance controls for data access, audit logging, and 
incident response. 
● Collaborate with clinical, legal, and IT teams to ensure AI/ML governance 
standards are met for model validation, explainability, and bias monitoring.

# Key Objectives 
● Regulatory Assessment 
● Determine whether the dosing recommendation engine qualifies as 
a regulated medical device under FDA guidance. 
● Document applicable federal and state regulations for genetic data 
and clinical AI. 
● Establish a regulatory pathway and timeline if FDA submission is 
required. 
● Data Privacy & Protection 
● Define de-identification standards for datasets used in model 
training and analytics. 
● Ensure all data handling practices comply with HIPAA Privacy and 
Security Rules. 
● Validate genetic data protections under GINA and applicable state 
laws. 
● Risk Management 
● Maintain a risk register documenting identified risks, likelihood, 
impact, and mitigation strategies. 
● Conduct third-party risk assessments for EHR vendors, cloud 
providers, and integration partners. 
● Perform periodic reassessments as the project scales to new sites 
and use cases. 
● AI/ML Governance 
● Establish model validation criteria and documentation requirements 
before deployment.
● Define policies for bias monitoring, performance drift detection, and 
scheduled retraining. 
● Ensure explainability outputs (e.g., LIME, SHAP) meet clinical and 
regulatory standards. 
● Audit & Incident Response 
● Define audit trail requirements for data access, model predictions, 
and clinical overrides. 
● Develop incident response protocols for data breaches, model 
failures, and adverse clinical events. 
● Ensure documentation supports regulatory filings, payer contracts, 
and legal defensibility.

# Key Deliverables 
● Regulatory Assessment Report 
● FDA/SaMD determination and regulatory pathway documentation. 
● Summary of applicable federal, state, and international 
requirements. 
● Data Governance Policy 
● PHI and genetic data handling standards. 
● Data retention, access control, and destruction policies. 
● Risk Register 
● Comprehensive list of identified risks with likelihood, impact, and 
mitigation plans. 
● Third-party risk assessment summaries for vendors and partners. 
● AI/ML Governance Framework 
● Model validation protocols and documentation standards. 
● Bias monitoring and drift detection policies. 
● Retraining and version control requirements. 
● Audit Trail Specification 
● Logging requirements for data access, predictions, and clinical 
actions. 
● Retention periods and access controls for audit logs. 
● Incident Response Plan 
● Breach notification procedures and escalation paths. 
● Clinical escalation protocols for model failures or adverse events. 
● Post-incident review and remediation processes. 





# 5. Technology Stack 
Data & Integration 
● Ingestion & ETL: Python, Pandas, possibly PySpark for larger offline 
jobs. 
● Pipelines: Makefiles or simple CI workflows (GitHub Actions) for 
reproducible ETL runs. 
● Storage for Collaboration: GitHub repo as the central project artifact 
hub (code + de-identified datasets). 
● Git LFS for larger CSV/Parquet files in /data/processed/. 
Model Development & MLOps 
● Modeling: TensorFlow/Keras, Scikit-learn, XGBoost. 
● Experiment Tracking & Registry: MLflow.
● Explainability: LIME for feature attributions, standardized explanation 
templates for clinicians. 
Serving & Applications 
● Model Serving: Gradio App for dosing recommendations. 
● Dashboards: Streamlit or Dash for clinician dashboards; BI tool (e.g., 
Looker / Power BI / Tableau) for executive and operational analytics. 
Governance & Collaboration 
● Project Management: Jira (Agile boards), Confluence (designs, 
decisions, SOPs). 
● BA & Process: BPMN diagrams for workflow design, requirements 
traceability matrices, stakeholder maps. 
● Security & Compliance: IAM, encryption at rest/in transit, data access 
logs, DLP policies. 



#  6. End-to-End Workflow 
# Phase 1: Initiation & Requirements 
Leads: BA + PMO, with Clinical & IT stakeholders 
● Conduct workshops with cardiologists, hematologists, pharmacists, 
nurses, hospital IT, and compliance. 
● Define clinical and business success metrics and regulatory constraints. 
● Design the target dosing workflow: where and when dosing 
recommendations appear in the EHR. 
● Establish governance for data privacy, access, and auditing. 
Phase 2: Data Exploration & Analytics Baseline 
Leads: Data Analytics, with DS and Clinical 
● Perform descriptive analysis of historical Warfarin patients (doses, INRs, 
ADEs, subgroups). 
● Quantify current-state performance: 
○ Time to stable INR. 
○ Baseline bleeding/clotting rates and costs. 
○ Identify high-risk cohorts to target for early roll-out and impact 
evaluation. 
● Provide clinical teams with baseline dashboards to align on problem 
severity and priorities. 
Phase 3: Model Development & Validation 
● Conduct workshops with cardiologists, hematologists, pharmacists, 
nurses, hospital IT, and compliance. 
● Define clinical and business success metrics and regulatory constraints. 
● Design the target dosing workflow: where and when dosing 
recommendations appear in the EHR. 
● Establish governance for data privacy, access, and auditing. 

# Phase 2: Data Exploration & Analytics Baseline 
Leads: Data Analytics, with DS and Clinical 
● Perform descriptive analysis of historical Warfarin patients (doses, INRs, 
ADEs, subgroups). 
● Quantify current-state performance: 
○ Time to stable INR. 
○ Baseline bleeding/clotting rates and costs. 
○ Identify high-risk cohorts to target for early roll-out and impact 
evaluation. 
● Provide clinical teams with baseline dashboards to align on problem 
severity and priorities. 

# Phase 3: Model Development & Validation 
○ Dose distributions vs historical patterns. 
○ INR trajectories and stabilization times. 
○ ADE rates vs pre-implementation baselines. 
● BA and DA run impact analyses (clinical + financial), including 
readmission reductions and cost savings. 
● Clinical and compliance teams review safety metrics and document 
outcomes for regulators and payers. 

# Phase 5: Scaling, Retraining & Continuous Improvement 
Leads: DA, DS, PMO 
● Scale integration across additional hospital sites and partner systems. 
● Implement scheduled retraining (e.g., quarterly) based on new outcome 
data and population shifts. 
● Monitor for model drift, subgroup performance, and bias. 
● Continuously refine dashboards and workflows based on user feedback. 
● Use DA insights to refine contracts and pricing models for hospitals and 
insurers.



#v 7. Expected Outcomes 
Clinical Impact 
● ≥25% reduction in Warfarin-related bleeding events within 6–12 months. 
● Higher percentage of patients achieving stable INR in <10 days. 
● Increased overall TTR in the first 90 days of therapy. 
Operational & Financial Impact 
● Reduction in Warfarin-related readmissions and length of stay. 
● Lower clinician time spent on manual dose adjustments. 
● Demonstrable cost savings per patient and per hospital per year. 
Strategic Impact for GenexaHealth 
● Strong clinical and economic evidence to support precision medicine 
adoption. 
● Differentiation as a data-first, engineering-strong partner (not just a 
testing lab or model shop). 
● Expanded contracts with hospitals, payers, and pharma for additional 
pharmacogenomic use cases.











