FROM python:3.12-slim
WORKDIR /app/backend
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5050
CMD [ "flask", "--app", "app", "run", "--host", "0.0.0.0", "--port", "5050", "--debug" ]
