FROM python:3.9

WORKDIR /app

RUN pip install gunicorn==20.1.0
RUN apt-get update && apt-get install -y netcat-openbsd && apt-get clean

COPY ./requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]