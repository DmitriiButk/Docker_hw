FROM python:3.9

WORKDIR /app

COPY . /app

RUN pip install -r /app/requirements.txt && python manage.py migrate

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

