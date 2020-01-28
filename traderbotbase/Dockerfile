FROM centos:7

RUN yum -y install epel-release && \
  yum clean all && \
  yum -y install python-pip && \
  pip install --upgrade pip && \
  pip install slackclient==1.0.2 && \
  pip install pytz && \ 
  yum -y install gcc && \
  yum -y install python-devel && \
  pip install regex && \
  pip install python-binance

ENV TRADERBOT /tmp/traderbot56
RUN mkdir -p "$TRADERBOT"     
COPY config.py $TRADERBOT/
WORKDIR $TRADERBOT
RUN chmod 644 $TRADERBOT
