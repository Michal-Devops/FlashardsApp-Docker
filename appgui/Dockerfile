FROM python:3.8-slim

# Ustawiam katalog roboczy
WORKDIR /app

# instalujemy potrzebne zaleznosci dla kivy
RUN apt-get update && apt-get install -y \
    libgl1-mesa-dev \
    x11-xserver-utils \
    && rm -rf /var/lib/apt/lists/*

# pliki z aplkicacji sa kopiowane 
COPY . /app

# instalowanie zaleznosci pythona 
RUN pip install kivy

# ustawaianie zmienej srodowiskowej 
ENV DISPLAY=:0.0

# Uruchomamiamy aplikacje 
CMD ["python", "./main.py"]