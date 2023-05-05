FROM python:3.7-slim

RUN /app

COPY ./api_yamdb/requirements.txt ./

RUN pip3 install -r /app/requirements.txt --no-cache-dir

COPY ./api_yamdb/ ./

WORKDIR /app

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 