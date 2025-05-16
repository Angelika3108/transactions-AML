## Analysis of customer payment transactions in the context of Anti-Money Laundering (AML) monitoring

The primary objective is to assess the behavior of payment flows, detect suspicious activity through alert rules, and visualize actionable insights using interactive dashboards.

### The analysis integrates three datasets:
1.	Customers.csv: Customer information and characteristics
2.	Payments.csv: Details of all money transfer transactions
3.	Alerts.csv: Generated alerts triggered by AML rule violations

### 🧩 Data Preparation and Modeling
•	All three datasets were imported and cleaned in Power BI.
•	Relationships were created:
o	Customers[CustomerID] ↔ Payments[CustomerID]
o	Payments[PaymentID] ↔ Alerts[PaymentID]
•	A CountryCode column was created by extracting the 5th and 6th characters of the CounterpartBIC field.
•	A CountryName column was derived using a country code mapping.

### 📊 Dashboard Features
![Chart]('Charts.jpg')


### 🔍 Insights
1.	All rejected alerts and connected to them payments triggered by Rules 1 to 7.
2.	Customers with most Total alerts count show significantly higher alert volumes, which may indicate unusual behavior worth deeper investigation.
