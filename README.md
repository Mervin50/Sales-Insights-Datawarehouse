# Sales-Insights-Datawarehouse



1. Database Setup
   
- Checked for existing 'DataWarehouseAnalytics' DB and dropped it

- Created a fresh instance of the DB

- Defined a custom schema: 'gold'

2. Schema Design
   
- Created 3 core tables under 'gold'

  a. dim_customers

  b. dim_products

  c. fact_sales

3. Data Loading

- Used BULK INSERT to load CSV data from local filesystem

- Corrected syntax: single quotes for file paths

- Ensured each table was truncated before load

4. Metadata Exploration

- Queried INFORMATION_SCHEMA.TABLES and COLUMNS

<img width="1470" height="231" alt="imaGE DE" src="https://github.com/user-attachments/assets/b6484217-f8a4-404a-ab3a-272b4a3f43a3" />

- Analyzed schema structure and validated columns

<img width="502" height="97" alt="imaGE DE" src="https://github.com/user-attachments/assets/eceb8c86-2fbf-4110-a142-b7112944d1c1" />

5. Dimension Insights

- Extracted distinct countries, categories, subcategories, product names

<img width="401" height="448" alt="imaGE DE" src="https://github.com/user-attachments/assets/72ec49e7-0351-4860-b737-a97c6ce6ce60" />

6. Fact Table Exploration

- Found first/last order dates and sales range

<img width="375" height="53" alt="imaGE DE" src="https://github.com/user-attachments/assets/dda18042-bfe6-4ca5-8704-d04d1eed4036" />

- Find the youngest and the oldest customer
- 
<img width="442" height="50" alt="imaGE DE" src="https://github.com/user-attachments/assets/9994493a-63ea-4da2-bfd4-43544617427d" />

- Calculated total sales, quantities, average price, order counts

<img width="122" height="47" alt="imaGE DE" src="https://github.com/user-attachments/assets/509116cf-62e3-400f-81e2-037e0a2d82d7" />


<img width="131" height="51" alt="imaGE DE" src="https://github.com/user-attachments/assets/1490a57c-f5eb-4ac7-be43-15126826e369" />


<img width="112" height="47" alt="imaGE DE" src="https://github.com/user-attachments/assets/80ee88a2-41b4-4bda-9827-b5034e3611e4" />


7. Summary Report (KPI Dashboard)
- Used UNION ALL to generate a consolidated metrics report:

- Total Sales, Quantity, Average Price, Orders, Products, Customers

<img width="137" height="272" alt="imaGE DE" src="https://github.com/user-attachments/assets/767ff57a-8f89-4715-8840-e810599e2436" />


<img width="160" hei<img width="140" height="262" alt="imaGE DE" src="https://github.com/user-attachments/assets/4a8f2981-e793-47c1-9dd4-bd1882008944" />


ght="50" alt="imaGE DE" src="https://github.com/user-attachments/assets/b95ea81e-acce-4646-8082-d1c01508b4c6" />


<img width="147" height="55" alt="image" src="https://github.com/user-attachments/assets/3414d60a-5e92-492a-b82e-cc54ef6f7caa" />


<img width="287" height="157" alt="image" src="https://github.com/user-attachments/assets/90aaab45-f50b-4d1f-89b2-80caf6f85638" />


8. Grouped Aggregations

- Total customers by gender and country

<img width="213" height="92" alt="imaGE DE" src="https://github.com/user-attachments/assets/2f7b8356-29a9-4ef3-8746-568150849f12" />


<img width="257" height="187" alt="imaGE DE" src="https://github.com/user-attachments/assets/cb863e9d-0666-471c-8960-eb4505658818" />


- Product counts by category

<img width="226" height="128" alt="imaGE DE" src="https://github.com/user-attachments/assets/6a5f4b2d-8937-4bb6-997e-82da50f9d601" />

- Average cost by category

<img width="196" height="132" alt="imaGE DE" src="https://github.com/user-attachments/assets/6f0221e8-f572-42ac-b2e1-4e5d8d8d177a" />


9. Revenue Analysis

- Revenue by product category

<img width="212" height="90" alt="imaGE DE" src="https://github.com/user-attachments/assets/e0087884-b2b9-42cb-8fc8-996379f32c03" />

- Revenue by customer (top earners)

<img width="402" height="456" alt="imaGE DE" src="https://github.com/user-attachments/assets/65e0119f-24cd-46fb-ba96-e9d731a4987f" />

- Item distribution across countries

<img width="255" height="177" alt="imaGE DE" src="https://github.com/user-attachments/assets/f7bb780d-f21e-4980-915a-f2363dbde96e" />


10. Performance Ranking

- Top 5 products by revenue (subcategories + product names)

<img width="386" height="346" alt="imaGE DE" src="https://github.com/user-attachments/assets/7d70261b-dc49-43db-8500-62f8876d616f" />


- Bottom 5 products by revenue

<img width="272" height="138" alt="imaGE DE" src="https://github.com/user-attachments/assets/b801108f-c117-4e13-ac44-8a1a64bc05e1" />

- Top 10 customers by revenue

<img width="383" height="233" alt="imaGE DE" src="https://github.com/user-attachments/assets/15a90ca2-9310-4435-ad4e-bdd862b2666e" />

- Bottom 3 customers by order count (least active)

<img width="376" height="93" alt="imaGE DE" src="https://github.com/user-attachments/assets/d8dbda65-7023-4ad9-a504-380c0522356c" />

