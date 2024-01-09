FROM python:3.9-slim
EXPOSE 8080

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY payment.py payment.py
COPY rabbitmq.py rabbitmq.py

ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123

CMD ["uwsgi", "--ini", "payment.ini"]





# FROM python:3.9-slim
# EXPOSE 8080
# WORKDIR /app
# COPY . .
# RUN pip install -r requirements.txt
# ENV AMQP_USER=roboshop \
#     AMQP_PASS=roboshop123
# ENTRYPOINT ["python", "payment.py"]
