# syntax=docker/dockerfile:1
FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
#no cache is for minimising the image size always while downloading the image.
COPY requirements.txt requirements.txt 
RUN pip install -r requirements.txt
#image runs on 5000 so expose is not necessary.
EXPOSE 5000
COPY . .
CMD ["flask", "run"]