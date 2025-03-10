# Ask-Your-Database-2.0

## Description
A Streamlit app built using LangChain and state of the art open source DeepSeek R1 LLM via Groq, converts natural language questions into SQL queries, retrieves data from a MySQL database, and presents the results as natural language responses

## Features
- Connect to a MySQL database using user-provided credentials.
- Automatically generate SQL queries based on natural language inputs.
- Execute queries and return results in natural language.
- Maintain a conversation history for context-aware query generation.
- 
![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/mysql-chains.png)

## Technologies Used
- UPDATE: `DeepSeek-R1-distill-llama-70`: Uses State of the Art LLM via Groq API, optionasl support for using OpenAI models
- **Streamlit**: For building the interactive web app interface.
- **LangChain**: For natural language understanding and query generation.
- **MySQL Connector**: For connecting to and querying the MySQL database.
  
## Installation

### Clone the Repository
```bash
git clone https://github.com/yourusername/Ask-Your-Database-2.0.git
cd Ask-Your-Database-2.0
```

### Set Up Environment Variables
1. Create a `.env` file:
   ```plaintext
   API_KEY=your_api_key_here
   GROQ_API_KEY=gour_groq_api_key_here
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

![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/demo1.png)
![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/demo2.png)
![alt text](https://github.com/sahilbishnoi26/Ask-Your-Database-2.0/blob/main/docs/demo3.png)


## Troubleshooting
- **Database Connection Error**: Ensure your MySQL server is running and credentials are correct.
- **Missing Dependencies**: Run `pip install -r requirements.txt` to ensure all dependencies are installed.
- **Port Already in Use**: Stop any process using the Streamlit default port (`8501`) or specify a different port using:
  ```bash
  streamlit run src\app.py --server.port=<port_number>
  ```
- **Virtual Environment Not Found**: Ensure the virtual environment is activated before running the app.
- **`.env` File Not Found**: Verify that the `.env` file exists in the `src` directory with correct API keys.
