FROM docker.elastic.co/elasticsearch/elasticsearch:7.6.0
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch ingest-attachment
RUN yum install wget -y && wget https://github.com/DigDes/elasticsearch-analysis-morphology/raw/master/analysis-morphology-7.6.0.zip -O /tmp/analysis-morphology-7.6.0.zip && \
        /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch file:///tmp/analysis-morphology-7.6.0.zip && rm /tmp/analysis-morphology-7.6.0.zip -f