
FROM alpine:3.4

RUN apk --no-cache add py-pip libpq python-dev curl

RUN pip install flask python3-consul

ADD / /app

WORKDIR /app

HEALTHCHECK CMD curl --fail http://localhost:5000/health || exit 1

CMD python3 app.py & python3 admin.py
