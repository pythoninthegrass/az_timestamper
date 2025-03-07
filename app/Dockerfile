# syntax=docker/dockerfile:1.7.0

ARG PYTHON_VERSION=3.11.11

FROM python:${PYTHON_VERSION}-alpine

WORKDIR /app

COPY requirements.txt /app

RUN python -m pip install -r requirements.txt

COPY . /app

ENTRYPOINT ["/app/scripts/entrypoint.sh"]
CMD ["python3", "app.py"]
