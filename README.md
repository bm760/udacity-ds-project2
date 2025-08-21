# Software Engineering for Data Scientists 

This repository contains code for the **Software Engineering for Data Scientists** final project, part of Udacity's Data Scientist nanodegree. 

### Author:
Benjamin Mardin

### Topic:
Data Science Dashboard

### Repository Structure
```
├── README.md
├── assets
│   ├── model.pkl
│   └── report.css
├── env
├── python-package
│   ├── employee_events
│   │   ├── __init__.py
│   │   ├── employee.py
│   │   ├── employee_events.db
│   │   ├── query_base.py
│   │   ├── sql_execution.py
│   │   └── team.py
│   ├── requirements.txt
│   ├── setup.py
├── report
│   ├── base_components
│   │   ├── __init__.py
│   │   ├── base_component.py
│   │   ├── data_table.py
│   │   ├── dropdown.py
│   │   ├── matplotlib_viz.py
│   │   └── radio.py
│   ├── combined_components
│   │   ├── __init__.py
│   │   ├── combined_component.py
│   │   └── form_group.py
│   ├── dashboard.py
│   └── utils.py
├── requirements.txt
├── start
├── tests
    └── test_employee_events.py
```

### employee_events.db

```mermaid
erDiagram

  employee {
    INTEGER employee_id PK
    TEXT first_name
    TEXT last_name
    INTEGER team_id
    
  }

  employee_events {
    TEXT event_date
    INTEGER employee_id FK
    INTEGER team_id FK
    INTEGER positive_events
    INTEGER negative_events
  }

  notes {
    INTEGER employee_id PK
    INTEGER team_id PK
    TEXT note
    TEXT note_date PK
  }

  team {
    INTEGER team_id PK
    TEXT team_name
    TEXT shift
    TEXT manager_name
  }

  team ||--o{ employee_events : "team_id"
  employee ||--o{ employee_events : "employee_id"
  notes }o--o{ employee_events : ""
```

### Libraries used:
- flake8
- ipython
- matplotlib==3.9.2
- numpy==2.1.2
- pandas==2.2.3
- pytest
- python-fasthtml==0.8.0
- scikit-learn==1.5.2
- scipy==1.14.1


### Instructions
1. download the repository files to the location of your choice, extracting if necessary
2. start your environment in ipython/conda/etc. 
3. pip install employee_events-0.5.tar.gz from udacity-ds-project2\python-package\dist\
4. using python, run dashboard.py from udacity-ds-project2\report\
5. open a web browser to http://localhost:5001/ to see the dashboard 
6. selecting a different user or team will update the charts and the notes on the dashboard. 






### Acknowledgements:
- Udacity data scientist program | Software Engineering for Data Scientists
- data sourced from Udacity 

#

