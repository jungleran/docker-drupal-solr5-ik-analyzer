FROM solr:5.5.5
ADD 5.x /conf
ADD ik-analyzer-solr5-5.x.jar /opt/solr/server/solr/lib/ik-analyzer-solr5-5.x.jar
RUN /opt/solr/bin/solr start \
    && /opt/solr/bin/solr create -d /conf -c drupal \
    && /opt/solr/bin/solr stop
VOLUME /opt/solr/server/solr/drupal
