FROM python:3.9
WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_ENV=production
EXPOSE 8000
CMD ["gunicorn", "-b", "0.0.0.0:8000", "wsgi:app"]