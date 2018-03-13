FROM sentry:latest

RUN apt-get update && apt-get install -y --no-install-recommends \
  libxmlsec1-dev \
  pkg-config

WORKDIR /usr/src/sentry

ENV PYTHONPATH /usr/src/sentry

COPY . /usr/src/sentry

RUN pip install -r requirements.txt

RUN cp sentry.conf.py $SENTRY_CONF/
