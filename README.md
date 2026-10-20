# PMS — Project Management System

Designed by **SkyWood Innovator**. A Streamlit project management starter app with a light theme, dark blue/gold/white accents, budget allocation, Agile workboard, roles/RACI, risk register, OpenAI project advisor, and Word/PDF/CSV/JSON exports.

## Features
- Project charter, sponsor, dates, framework and budget baseline
- Category-based budget allocation and over-budget warnings
- Task register with owners, priorities, estimates, sprints, statuses and budget
- Team roles and example RACI matrix
- Risk and issue register
- OpenAI API advisor for budget review, planning and risk analysis
- Downloadable DOCX, PDF, TXT, CSV and JSON reports/data
- Dashboard with budget and task health indicators

## Run locally
1. Install Python 3.10 or newer.
2. Unzip the project and open a terminal in the folder.
3. Create and activate a virtual environment:
   - Windows: `py -m venv .venv` then `.venv\Scripts\activate`
   - macOS/Linux: `python3 -m venv .venv` then `source .venv/bin/activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Start app: `streamlit run app.py`

## Configure OpenAI
Create `.streamlit/secrets.toml`:
```toml
OPENAI_API_KEY = "your-real-api-key"
OPENAI_MODEL = "gpt-4.1-mini"
```
Or set environment variables. Never publish your API key in source control. API usage may incur charges.

## Deploy to Streamlit Community Cloud
1. Push `app.py`, `requirements.txt`, and `README.md` to a GitHub repository.
2. Create a new app in Streamlit Community Cloud and select `app.py`.
3. In app settings → Secrets, add `OPENAI_API_KEY` and `OPENAI_MODEL`.
4. Deploy and test report downloads and AI responses.

## Important production notes
This starter stores project edits in Streamlit session state, not a persistent database. Session data may reset. Before real organizational use, add authentication/authorization, persistent database storage, audit logs, backups, approval workflows, input validation, and tenant separation. Budget figures and AI recommendations must be reviewed by authorized humans.

## Agile workflow
Discover → Charter & Fund → Prioritize Backlog → Plan Sprint/Flow → Build & Test → Review/Accept → Retrospective → Forecast & Adapt → Release & Close.

## Suggested roles
Product Owner, Scrum Master/Agile Coach, Project Manager, Business Analyst, Developers/Delivery Team, QA/Test Engineer, Finance/Budget Owner, Sponsor/Stakeholders.
