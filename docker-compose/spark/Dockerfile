FROM jupyter/pyspark-notebook:x86_64-spark-3.5.0

USER root

RUN apt-get update
RUN apt-get install -y curl unzip

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && sudo ./aws/install

USER jovyan
RUN pip install poetry
ENV JUPYTER_TOKEN=""