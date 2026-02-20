# IntelliSQL: Intelligent SQL Querying with Gemini Pro

IntelliSQL is a revolutionized database querying tool that bridges the gap between natural language and structured data. By leveraging the Gemini 1.5 Flash model, it allows non-technical users to extract insights from a SQLite database using plain English.

## **🚀 Features**

- **Text-to-SQL Translation:** Converts English questions into precise SQL queries using LLMs.
- **Regex Sanitization:** A custom logic layer that cleans AI responses to ensure only valid SQL is executed.
- **Interactive Dashboard:** A professional Streamlit interface with dark-mode support and sidebar navigation.
- **Secure Configuration:** API keys are managed safely via .env files and python-dotenv.
- **Real-time Results:** Instant rendering of database records in structured data tables.

## **🛠️ Technology Stack**

Frontend: Streamlit \
Backend: Python, Google Generative AI SDK \
Database: SQLite \
AI Model: Gemini 1.5 Flash

## **📂 Project Structure**


```
IntelliSQL/
├── .venv/                # Virtual environment [cite: 113]
├── Project Files/        # Core application source
│   ├── .env              # Secure API Key storage [cite: 1, 127]
│   ├── app.py            # Streamlit UI & AI Logic [cite: 83, 136]
│   ├── sql.py            # DB Engineering & Seeding [cite: 137]
│   ├── data.db           # SQLite Database [cite: 109]
│   └── requirements.txt  # Project Dependencies [cite: 122]
└── README.md             # High-level Documentation [cite: 57, 83]
```
## **⚙️ Setup & Installation**

1. **Clone the Repository:**

```[Bash]
eg: git clone https://github.com/anandpasupuleti/IntelliSQL.git
cd IntelliSQL
``` 
2. **Set up Environment:**

```[Bash]
python -m venv .venv
source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
pip install -r "Project Files/requirements.txt"
```
3. **Configure API Key:**

Create a `.env` file in the Project Files directory and add your key:
```[Plaintext]
GOOGLE_API_KEY="your_google_gemini_api_key"
```
4. **Initialize Database:**

```[Bash]
python "Project Files/sql.py"
```
5. **Run Application:**
```[Bash]
streamlit run "Project Files/app.py"
```

## **👥 Team Members & Roles**

1. **Mullapudi Likhitha Sahithi** (Project Manager & AI Specialist)
2. **Musunuri Sai**(Backend Developer & Data Engineer)
3. **Pasupuleti Anand Ramanaidu** (Frontend Developer & UI/UX Designer) 
4. **Puli Abhishek** (QA Engineer)


## **⚠️ Known Issues**
- Occasional hallucinations on complex multi-table joins if not specified in the schema.
- Requires an active internet connection to reach the Gemini API.