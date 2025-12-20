FROM python:3.11

WORKDIR /var/www/html

COPY ./docker/web/requirements.txt /var/www/html/

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "config.wsgi:application"]
