# Mini Web App

Simple Python Flask app for DevOps pipeline demo.

## Run locally

```bash
python -m venv venv
venv\Scripts\activate   # for Windows
pip install -r requirements.txt
python app.py
```
---

### Deploy / CI/CD ideja

- GitHub repo → GitHub Actions pipeline:  
  - **Step 1:** Install Python & dependencies  
  - **Step 2:** Run linter / tests (može i `pytest`)  
  - **Step 3:** Build Docker image & deploy (lokalno ili na cloud)  

- Dockerfile (opciono):

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["python", "app.py"]
```