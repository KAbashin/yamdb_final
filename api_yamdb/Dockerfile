FROM python:3.8.13-slim

WORKDIR /app

COPY . .

RUN python -m pip install --upgrade pip
RUN pip3 install -r /app/requirements.txt --no-cache-dir

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]