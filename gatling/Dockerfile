FROM openjdk:11-jre-slim
ENV LANG C.UTF-8

RUN apt-get update -y \
    && apt-get upgrade -y \
    && apt-get install -y wget unzip

RUN mkdir /gatling && cd /gatling
WORKDIR /gatling

RUN wget -qO- https://repo1.maven.org/maven2/io/gatling/highcharts/gatling-charts-highcharts-bundle/3.5.1/gatling-charts-highcharts-bundle-3.5.1-bundle.zip -O /gatling/gatling-charts-highcharts-bundle-3.5.1-bundle.zip
RUN unzip gatling-charts-highcharts-bundle-3.5.1-bundle.zip
RUN rm gatling-charts-highcharts-bundle-3.5.1-bundle.zip
ENV GATLING_HOME=/gatling/gatling-charts-highcharts-bundle-3.5.1

RUN ln -s /gatling/gatling-charts-highcharts-bundle-3.5.1/bin/gatling.sh /usr/local/bin/gatling && chmod ug+x /usr/local/bin/gatling
