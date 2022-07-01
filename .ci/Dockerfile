FROM python:3.10-slim

WORKDIR /usr/app/src/

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

# system
RUN apt-get update && apt-get install -y build-essential git gzip brotli parallel --no-install-recommends && rm -rf /var/lib/apt/lists/*

# jupyter-book
COPY .ci/requirements.txt .ci/requirements.txt
RUN pip install --no-cache-dir -r .ci/requirements.txt

# Python deps
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

CMD ["jupyter-book"]
