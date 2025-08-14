# 1. Python 3.10 tabanlı image
FROM python:3.10-slim

# 2. Çalışma dizini
WORKDIR /app

# 3. Gereksinimleri kopyala ve yükle
COPY requirements.txt .
RUN pip install --upgrade pip setuptools wheel
RUN pip install -r requirements.txt

# 4. Uygulama dosyalarını kopyala
COPY . .

# 5. Flask uygulamasını çalıştır
#    Eğer app.py içindeki Flask uygulama objesi 'app' ise
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

# 6. Uygulamanın expose edeceği port
EXPOSE 5000

# 7. Başlangıç komutu
CMD ["flask", "run"]
