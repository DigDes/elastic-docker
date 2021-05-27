FROM amazon/opendistro-for-elasticsearch:1.13.2
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch ingest-attachment
RUN yum install wget -y && wget https://github.com/DigDes/elasticsearch-analysis-morphology/raw/master/analysis-morphology-7.10.2.zip -O /tmp/analysis-morphology.zip && \ 
        /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch file:///tmp/analysis-morphology.zip && rm /tmp/analysis-morphology.zip -f