# SQL-LLM-Agent (Natural Language to SQL Query App)

This project is a natural language-driven application that allows non-technical users to interact with SQL databases. By using OpenAI's language models and integrating with Azure SQL Database, the system translates plain language questions into SQL queries and retrieves data in a user-friendly format.

## **Architecture Overview**

![ss](https://github.com/user-attachments/assets/687ce2ce-4136-4274-adb8-3041a7a67eb7)


1. **User Input**: Non-technical users submit queries in plain language through a Streamlit web interface.
2. **Streamlit Front-End**: The front-end sends the user's input to a Flask backend via an API request.
3. **Flask Middleware**: Processes the request, sends the natural language query to OpenAI, and handles the generated SQL query execution.
4. **OpenAI Integration**: Converts the natural language query into an SQL query.
5. **Azure SQL Database**: Executes the generated SQL query and returns the results.
6. **Response Handling**: Results are sent back to the Streamlit front-end for display.

## **Features**

- **Natural Language Querying**: Users can ask questions in plain language.
- **Seamless SQL Generation**: Automatically generates SQL queries optimized for Azure SQL databases.
- **Scalable Integration**: Built with Flask middleware to handle complex requests and database operations.
- **Interactive UI**: Easy-to-use Streamlit interface for real-time interaction.

## **Tech Stack**

- **Front-End**: Streamlit
- **Backend Middleware**: Flask
- **AI Integration**: OpenAI API (Azure OpenAI)
- **Database**: Azure SQL Database (Data Warehouse)
- **Hosting**: Azure Cloud

## **Setup and Installation**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/natural-language-sql-app.git
   cd natural-language-sql-app
