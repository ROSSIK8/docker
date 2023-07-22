FROM python:3.8

COPY ./stocks_products/requirements.txt /src/requirements.txt
RUN pip3 install -r /src/requirements.txt

COPY . /src

WORKDIR src

EXPOSE 8000

RUN python stocks_products/manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products/stocks_products.wsgi"]
