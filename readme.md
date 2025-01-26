# Ask-Your-Database-2.0

## Description
A Streamlit-based interactive chat application that connects to a MySQL database, allowing users to ask questions about their data and receive SQL-generated responses in natural language.

## Features
- Connect to a MySQL database using user-provided credentials.
- Automatically generate SQL queries based on natural language inputs.
- Execute queries and return results in user-friendly language.
- Maintain a conversation history for context-aware query generation.
- 
![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/mysql-chains.png)

## Technologies Used
- **Streamlit**: For building the interactive web app interface.
- **LangChain**: For natural language understanding and query generation.
- **MySQL Connector**: For connecting to and querying the MySQL database.
  
## Installation

### Clone the Repository
```bash
git clone https://github.com/yourusername/chat-with-mysql.git
cd chat-with-mysql
```

### Set Up Environment Variables
1. Create a `.env` file in the `src` folder:
   ```plaintext
   API_KEY=your_api_key_here
   GROQ_API_KEY=groq_api_key_here
   ```
2. Replace placeholders with your actual API keys.

### Create and Activate a Virtual Environment
#### On Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

#### On macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

## Usage
1. Run the application:
   ```bash
   streamlit run src\app.py
   ```
2. Open the provided URL in your browser.
3. Enter your MySQL database credentials in the sidebar and click "Connect."
4. Ask questions in the chat input to interact with your database.

![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/pic1.png)


## Troubleshooting
- **Database Connection Error**: Ensure your MySQL server is running and credentials are correct.
- **Missing Dependencies**: Run `pip install -r requirements.txt` to ensure all dependencies are installed.
- **Port Already in Use**: Stop any process using the Streamlit default port (`8501`) or specify a different port using:
  ```bash
  streamlit run src\app.py --server.port=<port_number>
  ```
- **Virtual Environment Not Found**: Ensure the virtual environment is activated before running the app.
- **`.env` File Not Found**: Verify that the `.env` file exists in the `src` directory with correct API keys.
``````
