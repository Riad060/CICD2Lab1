# CICD-2 FastAPI Lab Template

This repository contains a FastAPI lab for the CICD-2 module.  
Use this `README.md` as the standard structure for future labs.

---

## Lab Title

**Replace this with the lab title**

Example:

> Lab 1 — Creating a Basic FastAPI Application

---
## Repository Structure

Use the following structure for the labs:

```text
project-name/
│
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── schemas.py
│   ├── services.py
│   └── models.py
│
├── tests/
│   ├── __init__.py
│   └── test_main.py
│
├── requirements.txt
├── README.md
└── .gitignore
```
## Lab 5 - HTTPX Microservices
The project now contains two FastAPI services.
### User API
Runs on port 8000:
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
### Product Service
Runs on port 8001:
python -m uvicorn product_service.main:app --host 0.0.0.0 --port 8001 --reload
The User API endpoint:
GET /api/products/{product_id}
calls the Product Service using HTTPX.
PRODUCT_SERVICE_URL configures the address of the Product Service.
In Codespaces it defaults to:
http://127.0.0.1:8001