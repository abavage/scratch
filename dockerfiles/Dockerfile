FROM registry.redhat.io/ubi9:9.8-1790067847
#RUN dnf -y --nodocs install jq git && \
#    dnf clean all && \
RUN curl -L -o /tmp/trident-installer-26.06.1.tar.gz https://github.com/NetApp/trident/releases/download/v26.06.1/trident-installer-26.06.1.tar.gz && \
    tar -zxpf /tmp/trident-installer-26.06.1.tar.gz -C /tmp/ && \
    cp /tmp/trident-installer/tridentctl /usr/local/bin/ 
#COPY index.html /var/www/html/index.html
#EXPOSE 8080
#CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
