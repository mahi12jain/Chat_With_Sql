# SQL Chat - Talk to Your Databases with LLMs

SQL Chat is a Streamlit application that allows you to interact with your SQL databases using natural language. Built with LangChain and Groq, this application enables you to query SQL databases through simple conversations.

## Features

- Chat with SQLite or MySQL databases using natural language
- Real-time streaming responses
- Support for both local SQLite databases and remote MySQL connections
- Powered by Groq's Llama3-8b LLM
- Session management for conversation history

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/sql-chat.git
cd sql-chat
```

2. Install dependencies:
```bash
pip install streamlit langchain-community langchain langchain-groq sqlalchemy mysql-connector-python
```

3. Prepare your database:
   - For SQLite: Make sure you have a `student.db` file in the same directory as the application
   - For MySQL: Have your connection details ready (host, username, password, database name)

4. Get your Groq API key from [Groq's website](https://console.groq.com/)

## Usage

1. Run the Streamlit app:
```bash
streamlit run app.py
```

2. In the sidebar:
   - Choose between SQLite or MySQL database
   - If MySQL, enter your connection details
   - Enter your Groq API key

3. Start chatting with your database! You can ask questions like:
   - "Show me all students with a GPA above 3.5"
   - "What's the average age of students in the Computer Science department?"
   - "List the top 5 students by attendance"

## How It Works

This application uses LangChain's SQL agent to:
1. Convert natural language queries into SQL
2. Execute the SQL against your chosen database
3. Return the results in a user-friendly format

The application maintains a conversation history so you can refer to previous questions and build on them.

## Database Schema

For optimal results, familiarize yourself with your database schema. The SQLite `student.db` file includes tables for:
- Students (id, name, age, gpa, department, etc.)
- [Additional tables if applicable]

## Troubleshooting

- **Connection Issues**: Ensure your MySQL credentials are correct and the server is accessible
- **Permission Errors**: Make sure your database user has appropriate read permissions
- **Missing Database**: Verify that the student.db file exists in the project directory

## License

[Your license information here]

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
