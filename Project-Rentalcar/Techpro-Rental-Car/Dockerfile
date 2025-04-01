FROM python:3.9

# Çalışma dizinini belirle
WORKDIR /app

# Bağımlılıkları yükle
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Uygulama dosyalarını kopyala
COPY . .

# Ortam değişkenlerini belirle
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_ENV=production

# Port tanımla
EXPOSE 8000

# Uygulamayı başlat
CMD ["gunicorn", "-b", "0.0.0.0:8000", "app:app"]