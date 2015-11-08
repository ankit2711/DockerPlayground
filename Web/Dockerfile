FROM ankit2711/elasticsearch_tomcat7_java8_ubuntu

# Install supervisor.
RUN apt-get update && apt-get install -y supervisor
RUN mkdir -p /var/log/supervisor

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Expose ports.
#   - 9200: HTTP
#   - 9300: transport
EXPOSE 9200 9300 8080

# Define default command.
CMD ["/usr/bin/supervisord"]

