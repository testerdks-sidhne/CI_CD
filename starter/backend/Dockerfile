FROM python:3.10-slim
ENV FLASK_RUN_HOST=0.0.0.0

WORKDIR /app

RUN adduser --uid 1000 --disabled-password --gecos "" app
RUN mkdir -p /var/www/app

RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    gcc \
    libpcre2-dev \
    && rm -rf /var/lib/apt/lists/* \
    && pip install --no-cache-dir setuptools wheel pipenv

COPY Pipfile* /app/
RUN cd /app && pipenv install --system --ignore-pipfile

COPY . /app

EXPOSE 5000

CMD ["uwsgi", "--http", ":5000", "--master", "--enable-threads", "--manage-script-name", "--mount", "/=__init__:app"]