FROM python:3.8.13

WORKDIR /first-ml-deploy

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

EXPOSE $PORT

CMD gunicorn --workers=4 --bind 0.0.0.0:$PORT app:app