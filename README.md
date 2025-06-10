# AWS-Athena-with-Power-BI-for--Insurance-Claim-Fraud-Detection-Analysis

**📌 Project Overview**
Developed a cloud-based end-to-end data analysis pipeline to detect and analyze fraudulent vehicle insurance claims. Leveraging AWS services (S3, Glue, Athena) and Power BI, the solution identifies fraud patterns through efficient data processing and visualization, enabling proactive decision-making.

**🧾 Dataset**

* **Source:** Kaggle – Vehicle Claim Fraud Detection
* **Volume:** \~15,000 records
* **Target Variable:** `FraudFound_P` (1 = Fraudulent, 0 = Legitimate)
* **Key Features:** AgeOfVehicle, VehiclePrice, PolicyType, Make, MaritalStatus, Sex

**☁️ Cloud Architecture and Workflow**

* **AWS S3:**

  * Created a dedicated S3 bucket
  * Uploaded the dataset under `/dataset/`

* **AWS Glue:**

  * Configured IAM roles with appropriate access policies
  * Set up a Glue Crawler to scan the dataset and populate the AWS Glue Data Catalog

* **AWS Athena:**

  * Executed SQL queries directly on data in S3 using Athena
  * Conducted aggregations to uncover fraud trends across demographics and policy types

* **Power BI:**

  * Connected Power BI to Athena via ODBC using AWS credentials
  * Designed interactive dashboards to present key fraud insights and drill-down capabilities

**📊 Key Dashboard Insights**

* **Total Claims:** 15,000
* **Fraudulent Claims:** 923 (\~6%)

**Fraud Trends Identified:**

* Higher fraud rates observed in vehicles older than 6 years
* Vehicles priced above \$69,000 are more likely to be involved in fraudulent claims
* "Sport-Collision" policy type shows the highest fraud rate (\~13.79%)
* Car makes such as Mercedes, Acura, and Saturn display higher fraud likelihood
* Filterable insights by demographic factors (Age, Gender, Marital Status)

**📌 Visual Components:**

* KPI Cards
* Donut & Bar Charts
* Stacked Column Charts
* Interactive Filters and Slicers

**🚀 Future Enhancements**

* Integrate machine learning models (e.g., XGBoost, Logistic Regression) using **AWS SageMaker** for predictive fraud detection
* Implement real-time fraud alerting via **AWS Lambda** and **SNS**
* Enable dashboard embedding through **Power BI REST API** or transition to **AWS QuickSight** for tighter cloud integration

