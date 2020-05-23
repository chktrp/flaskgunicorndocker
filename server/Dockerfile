FROM python:3.7.7-alpine

WORKDIR /usr/src/app/
COPY . .

RUN apk update
RUN apk add -f bash nginx nano
RUN pip3 install -r requirements.txt

EXPOSE 31047

CMD ["gunicorn", "-b 0.0.0.0:31047", "wsgi:app", "--access-logfile", "log"]
