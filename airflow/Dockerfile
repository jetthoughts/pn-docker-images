# Images:
#  - pubnative/airflow:latest
#  - pubnative/airflow:${GIT_COMMIT}
# 
# C.f. Makefile

FROM pubnative/airflow:python3.7

ENV AIRFLOW_VERSION "1.10.7"
ENV INFLUX_DB_VERSION "5.2.1"
ENV WERKZEUG_VERSION "0.15.4"

LABEL maintainer Denis <denis@pubnative.net>

RUN pip3 install \
  apache-airflow[statsd]==${AIRFLOW_VERSION} \
  influxdb==${INFLUX_DB_VERSION} \
  werkzeug==${WERKZEUG_VERSION}
