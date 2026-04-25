# Latest Ubuntu bazası
FROM ubuntu:latest

# APT yeniləmələri
RUN apt-get update
RUN apt-get upgrade -y

# Python və Pip quraşdırılması
RUN apt-get install -y python3 python3-pip

# Windows/Docker mühitində pip xətasının qarşısını almaq üçün bu sətri mütləq əlavə edirik
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Flask-ın quraşdırılması
RUN pip3 install flask
RUN pip3 install flask-cors

# İş qovluğunu təyin edirik
WORKDIR /app

# api.py-ı konteynerin daxilinə kopyalayırıq
COPY ./api.py /app/api.py

# Konteyner işə düşəndə tətbiqi başladırıq
CMD ["python3", "/app/api.py"]