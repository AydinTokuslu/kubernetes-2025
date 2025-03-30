FROM python:alpine
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
WORKDIR /app
COPY . .
EXPOSE 80
CMD ["python", "app.py"]
