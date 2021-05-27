FROM ubuntu:focal
MAINTAINER Pradeep A. Dalvi "prad@apache.org"

RUN apt-get update --fix-missing

RUN apt-get install -y curl

RUN apt-get install -y python3
RUN apt-get install -y python3-requests
RUN apt-get install -y python3-pip
RUN apt-get install -y python3-dev
RUN pip install --upgrade pip

RUN pip install -U setuptools

RUN curl -L http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz -o /tmp/ta-lib-0.4.0-src.tar.gz
RUN tar -zxf /tmp/ta-lib-0.4.0-src.tar.gz -C /tmp
WORKDIR /tmp/ta-lib
RUN ./configure --prefix=/usr
RUN make
RUN make install

RUN pip install numpy

RUN pip install pandas
RUN pip install yfinance
RUN pip install plotly
RUN pip install cufflinks
RUN pip install chart_studio
RUN pip install dash
RUN pip install dash-bootstrap-components

RUN pip install ta-lib
