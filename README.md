ODI Match SQL Agent with Gemini
This project imports ODI match data from a CSV file into a SQLite database and enables natural language querying using Google Gemini (gemini-2.5-flash) via LangChain SQL Agent.
________________________________________
Features
•	Import ODI match data (ODI_Match_info.csv) into SQLite
•	Connect SQLite database using LangChain
•	Use Gemini 2.5 Flash LLM for natural language queries
•	Ask cricket-related questions like:
o	"How many times Pakistan won the match as winner?"
________________________________________
Project Structure
├── ODI_Match_info.csv
├── odi_matches.db
├── apii.py
├── main.py
└── README.md
________________________________________
Gemini API Key Setup
1. Create apii.py
Create a local file named apii.py and store your Gemini API key:
# apii.py
def get_api_key():
    return "YOUR_GEMINI_API_KEY"
Do NOT upload this file to public repositories. Add it to .gitignore.
________________________________________
Installation
Install required dependencies:
pip install pandas langchain langchain-community langchain-google-genai google-generativeai
________________________________________
Step 1: Import CSV into SQLite
The script:
•	Reads ODI_Match_info.csv
•	Creates odi_matches.db
•	Inserts data into match_info table
________________________________________
Step 2: Configure Gemini
The project uses:
•	Model: gemini-2.5-flash
•	LLM Wrapper: GoogleGenerativeAI
•	Agent Type: zero-shot-react-description
________________________________________
Usage
Run the script:
python main.py
Example query:
chat("how many times Pakistan won the match as winner")
________________________________________
How It Works
1.	CSV → SQLite Database
2.	LangChain connects to database
3.	Gemini LLM interprets natural language
4.	SQL Agent generates and executes SQL queries
5.	Returns structured answer
________________________________________
Technologies Used
•	Python
•	Pandas
•	SQLite
•	LangChain
•	Google Gemini API
________________________________________
Important Notes
•	Keep your API key private.
•	Add apii.py to .gitignore.
•	Ensure ODI_Match_info.csv exists in the project root.
________________________________________
Example Output
Pakistan has won XX matches.
________________________________________
Author
M Abssar Hussain
