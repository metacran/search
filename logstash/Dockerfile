
FROM docker.elastic.co/logstash/logstash:6.4.2

RUN logstash-plugin install logstash-input-couchdb_changes
RUN logstash-plugin install logstash-filter-ruby

COPY logstash.conf /usr/share/logstash/config/logstash.conf
COPY crandb-filter.rb /usr/share/logstash/config/crandb-filter.rb

CMD ["-f", "/usr/share/logstash/config/logstash.conf"]
