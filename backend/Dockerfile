FROM python:3.10
WORKDIR /backend
RUN python3 -m venv .venv
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5050
CMD [ "flask", "--app", "backend/app", "run", "--host", "0.0.0.0", "--port", "5050", "--debug" ]