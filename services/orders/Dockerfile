FROM python:rc-alpine

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
RUN apk update && apk add bind-tools dnsmasq
RUN mkdir -p /var/www/orders_service
WORKDIR /var/www/orders_service
CMD [ "python", "./app.py" ]