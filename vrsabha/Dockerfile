FROM python:3.9
MAINTAINER Pradeep A. Dalvi "prad@apache.org"

RUN apt-get update --fix-missing

RUN pip install -U setuptools

RUN wget http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz -o /tmp/ta-lib-0.4.0-src.tar.gz
RUN tar -zxf /tmp/ta-lib-0.4.0-src.tar.gz -C /tmp
WORKDIR /tmp/ta-lib
RUN bash ./configure
RUN make
RUN make install

RUN pip install numpy

RUN pip install pandas
RUN pip install yfinance
RUN pip install plotly
RUN pip install cufflinks
RUN pip install chart_studio

RUN pip install ta-lib
