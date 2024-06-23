### Project Description

#### Problem Statement
Telecom operator "TeleDom" wants to reduce customer churn. 
To achieve this, their employees will start offering promo codes and special conditions to customers who plan to terminate their services.
To proactively identify such users, "TeleDom" needs a model that predicts whether a subscriber will terminate their contract. 
The operator's team has collected personal data about some customers and information about their tariffs and services.
Your task is to train a model on this data to predict customer churn.

#### Description of Services
The operator provides two main types of services:
- **Fixed-line telephone service:** Multiple lines can be connected simultaneously.
- **Internet:** Connection can be through DSL (digital subscriber line) or fiber optic cable.
  
Additionally, subscribers have access to several services:
- Internet security: antivirus (Device Protection) and blocking of dangerous websites (Online Security).
- Dedicated technical support line (Tech Support).
- Cloud storage for data backup (Online Backup).
- Streaming TV (Streaming TV) and a catalog of movies (Streaming Movies).

Customers can pay for services monthly or once every 1-2 years. Various payment methods are available, including electronic invoicing.

#### Data Description
The data is stored in a PostgreSQL database and consists of several tables:
- **contract:** Information about contracts.
  - `customerID` — customer ID.
  - `BeginDate` — contract start date.
  - `EndDate` — contract end date.
  - `Type` — payment type (monthly or once every 1-2 years).
  - `PaperlessBilling` — electronic billing flag.
  - `PaymentMethod` — payment method.
  - `MonthlyCharges` — monthly charges.
  - `TotalCharges` — total charges.

- **personal:** Personal customer data.
  - `customerID` — customer ID.
  - `gender` — gender.
  - `SeniorCitizen` — senior citizen status.
  - `Partner` — whether the customer has a partner.
  - `Dependents` — whether the customer has dependents.

- **internet:** Information about internet services.
  - `customerID` — customer ID.
  - `InternetService` — type of internet connection.
  - `OnlineSecurity` — online security service status.
  - `OnlineBackup` — online backup service status.
  - `DeviceProtection` — device protection service status.
  - `TechSupport` — tech support service status.
  - `StreamingTV` — streaming TV service status.
  - `StreamingMovies` — streaming movies service status.

- **phone:** Information about phone services.
  - `customerID` — customer ID.
  - `MultipleLines` — multiple lines service status.

Contract information is current as of February 1, 2020.
