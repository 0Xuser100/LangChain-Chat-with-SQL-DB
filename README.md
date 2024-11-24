# 🦜 Chat with SQL Database using LangChain and Streamlit

This project is an interactive chatbot powered by **LangChain** and **Groq models**, designed to allow users to interact with SQL databases using natural language queries. The chatbot supports both **SQLite** and **MySQL** databases and provides a seamless interface through **Streamlit**.

## 🌟 Features

- **Conversational Interface**: Chat with your SQL database using natural language.
- **Database Support**: Connect to a local SQLite database (`student.db`) or your own MySQL database.
- **Powered by LangChain and Groq LLM**: Utilizes advanced language models for understanding and processing queries.
- **Streamlit Integration**: Interactive and user-friendly web application.
- **Real-time Responses**: Get immediate answers to your database queries.
- **Session Management**: Clear message history and maintain conversation context.

## 🛠️ Technologies Used

- **Python 3.7+**
- **Streamlit**: For building the web application interface.
- **LangChain**: To create agents that interpret and execute natural language queries.
- **Groq Language Model**: For language understanding and response generation.
- **SQLite3**: For local database operations.
- **MySQL Connector/Python**: For connecting to MySQL databases.
- **SQLAlchemy**: Database toolkit and Object-Relational Mapping (ORM) library.

## 🚀 How to Run the Project

### Prerequisites

1. **Python 3.7 or higher** installed on your system.
2. **Groq LLM API key**: Obtain your API key from [Groq](https://groq.com/).
3. **For MySQL Support** (optional):
   - MySQL server running.
   - MySQL user credentials and database details.

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your_username/your_repository.git
   cd your_repository
   ```

2. **Create a Virtual Environment**

   ```bash
   python -m venv venv
   ```

3. **Activate the Virtual Environment**

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

4. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   

requirements.txt

 is not provided, install packages manually:*

   ```bash
   pip install streamlit langchain langchain_groq sqlalchemy sqlite3 mysql-connector-python
   ```

### Setting Up the Database

#### SQLite Database

1. **Create and Populate the SQLite Database**

   Run the `sqlite.py` script to create `student.db` with sample data:

   ```bash
   python sqlite.py
   ```

#### MySQL Database (Optional)

1. **Ensure MySQL Server is Running**

2. **Prepare Your MySQL Database**

   - Create a new database or use an existing one.
   - Import or create the necessary tables and data corresponding to the `STUDENT` table structure used in `sqlite.py`.

### Running the Application

1. **Start the Streamlit App**

   ```bash
   streamlit run app.py
   ```

2. **Configure the App via Sidebar**

   - **Select Database Option**

     Choose between:

     - *Use SQLite 3 Database - `student.db`*
     - *Connect to Your MySQL Database*

   - **For MySQL Users**

     Enter the required MySQL connection details:

     - Host
     - User
     - Password
     - Database name

   - **Enter Groq API Key**

     Provide your Groq LLM API key for language processing.

3. **Interact with the Chatbot**

   - Type natural language queries related to your database.
   - Examples:

     - *"List all students in Data Science class with marks above 80."*
     - *"What is the average mark of students in section A?"*

## 🧩 Project Structure

```
your_repository/
├── app.py             # Main Streamlit application
├── sqlite.py          # Script to create and populate SQLite database
├── student.db         # SQLite database file (created after running sqlite.py)
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation
```

## 📚 How It Works

1. **Streamlit Interface**

   - The app presents a sidebar for configuration and a main chat interface for interaction.
   - Users can select the database type and provide necessary credentials.

2. **Database Configuration**

   - **SQLite**: Uses `student.db` located in the same directory.
   - **MySQL**: Connects using provided credentials. Requires `mysql-connector-python`.

3. **Language Model Integration**

   - Utilizes **Groq's Llama3-8b-8192** model for processing natural language queries.
   - The model interprets user queries and formulates SQL queries to interact with the database.

4. **Agent Setup**

   - **LangChain Agent**: Created with `create_sql_agent`, which handles the logic of converting natural language into SQL queries.
   - **Toolkit**: Uses `SQLDatabaseToolkit` for database interactions.

5. **Session Management**

   - Maintains conversation history using `st.session_state`.
   - Provides the option to clear message history via a sidebar button.

## 🧪 Example Use Case

1. **User Query**

   *"Show all students who scored more than 85 marks."*

2. **Assistant Response**

   - The assistant processes the query using the language model.
   - Converts it into an SQL query:

     ```sql
     SELECT * FROM STUDENT WHERE MARKS > 85;
     ```

   - Executes the query on the connected database.
   - Returns the results to the user in a readable format.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the Repository**

2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add YourFeature"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Open a Pull Request**

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 📞 Contact

For questions or suggestions, feel free to reach out to:

- **Name**: *Mahmoud Abdulhamid*
- **Email**: *mahmoudabdulhamid22@gmail.com*
- **GitHub**: [https://github.com/your_username](https://github.com/0Xuser100)
- **LinkedIn**: [(https://www.linkedin.com/in/yourprofile/)](https://www.linkedin.com/in/mahmoud-abdulhamid-052244230/)

---

# 🔗 Acknowledgments

- [Streamlit](https://streamlit.io/)
- [LangChain](https://github.com/hwchase17/langchain)
- [Groq](https://groq.com/)
- [SQLite](https://www.sqlite.org/index.html)
- [MySQL](https://www.mysql.com/)

# 📌 Notes

- Ensure that `student.db` is in the same directory as `app.py` when using the SQLite option.
- Replace placeholders like `your_username`, `your_repository`, and contact information with your actual details.

# 📝 

Requirements.txt

 Example

If you need to create a 

requirements.txt

, here's an example:

```txt
streamlit
langchain
langchain-groq
sqlalchemy
sqlite3
mysql-connector-python
```

# 🛡️ Disclaimer

This project is for educational purposes. Ensure you handle API keys and database credentials securely and do not expose them in public repositories.

# Shortcuts

- **Run App**: `streamlit run app.py`
- **Create SQLite DB**: `python sqlite.py`

---
