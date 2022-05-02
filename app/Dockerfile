FROM python:3.8
WORKDIR /django-code
RUN git clone https://github.com/volyayana/crud-docker-compose.git
#RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev
#RUN pip install psycopg2-binary
RUN pip install -r /django-code/crud-docker-compose/stocks_products/requirements.txt
EXPOSE 8000
CMD cd /django-code/crud-docker-compose/stocks_products && python manage.py migrate && gunicorn stocks_products.wsgi -b 0.0.0.0:8000
