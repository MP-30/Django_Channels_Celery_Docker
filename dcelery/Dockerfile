FROM python:3.10.12-alpine

WORKDIR /usr/src/app

# this will prevent python from writing .pyc files
ENV PYTHONDONWRITEBYTECODE 1

# this will ensure Python output is sent directly to the terminal without buffering
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/app/requirements.txt

RUN pip install -r requirements.txt

COPY ./entrypoint.sh /usr/src/app/entrypoint.sh

COPY . /usr/src/app 

ENTRYPOINT ["/usr/src/app/entrypoint.sh"]