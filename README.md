# SQL-LLM-Agent

SQL-LLM-Agent is a natural language interface for querying SQL databases. It leverages LLM's (OpenAI, gpt-35-turbo-instruct) powerful language model to convert plain English questions into SQL queries and fetch data from an Azure SQL database (as Data Warehouse). This app provides a seamless interface for non-technical users to interact with complex databases without writing any SQL code.

---

## Table of Contents

- [Architecture Overview](#architecture-overview)  
- [Features](#features)  
- [Tech Stack](#tech-stack)
- [Data Warehouse Schema](#data-warehouse-schema)
- [Streamlit App](#streamlit-app)  
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)  

---

## **Architecture Overview**

![arch](https://github.com/user-attachments/assets/b9fcd8e6-8810-4565-b3f9-258f49db553e)



1. **User Input**: Non-technical users submit queries in plain language through a Streamlit web interface.
2. **Streamlit Front-End**: The front-end sends the user's input to a Flask backend via an API request.
3. **Flask Middleware**: Processes the request, sends the natural language query to OpenAI, and handles the generated SQL query execution.
4. **OpenAI Integration**: Converts the natural language query into an SQL query.
5. **Azure SQL Database**: Executes the generated SQL query and returns the results.
6. **Response Handling**: Results are sent back to the Streamlit front-end for display.

---

## **Features**

- **Natural Language Querying**: Users can ask questions in plain language.
- **Seamless SQL Generation**: Automatically generates SQL queries optimized for Azure SQL databases.
- **Scalable Integration**: Built with Flask middleware to handle complex requests and database operations.
- **Interactive UI**: Easy-to-use Streamlit interface for real-time interaction.
- **Modify SQL Query Before Execution**: Allows users to review and edit the generated SQL query by LLM before Excuting it, ensuring flexibility and control.

---

## **Tech Stack**

- **Front-End**: Streamlit
- **Backend Middleware**: Flask
- **AI Integration**: OpenAI API (Azure OpenAI)
- **Database**: Azure SQL Database (Data Warehouse)
- **Hosting**: Azure Cloud

---

# **Data Warehouse Schema**
![schema](https://github.com/user-attachments/assets/ff313a72-25a9-4cb7-af4d-1fbbb264a284)


Tables:
- Sales_Fact: sales_id, product_id, customer_id, time_id, quantity_sold, total_amount
- Products_Dim: product_id, product_name, category, price
- Customers_Dim: customer_id, customer_name, region, country
- Time_Dim: time_id, date, month, quarter, year

Relationships:
- Sales_Fact.product_id -> Products_Dim.product_id
- Sales_Fact.customer_id -> Customers_Dim.customer_id
- Sales_Fact.time_id -> Time_Dim.time_id

---

## **Screenshots**
# 1-
![1](https://github.com/user-attachments/assets/753a8650-34c2-4a69-89a3-49203bb40abe)

# 2-
![2](https://github.com/user-attachments/assets/18f09d7f-801f-464a-9480-673951066dd9)


---

## **Future Enhancements**
- Add support for more databases (PostgreSQL, MySQL, etc.).
- Dockerize the Backend App to easy deploy on Instance.
- Integrate advanced visualization tools for richer insights.
- Implement caching for faster query responses.
- Enable local LLMs like Mistral-7B-Instruct-v0.3 for privacy.
- Using Azure Synapse Analytics As it is designed specifically for data warehousing and big data analytics.


