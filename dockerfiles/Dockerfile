FROM registry.redhat.io/ubi9:9.8-1790067847
RUN dnf -y --nodocs install jq git && \
    dnf clean all && \
    curl -L -o /usr/local/bin/trident-installer-26.06.1.tar.gz https://github.com/NetApp/trident/releases/download/v26.06.1/trident-installer-26.06.1.tar.gz 
    #tar -zxpf /usr/local/bin/trident-installer-26.06.1.tar.gz -C /usr/local/bin/ && \
    #rm /usr/local/bin/trident-installer-26.06.1.tar.gz && \
    #mv /usr/local/bin/trident-installer/trident /usr/local/bin/trident && \
    #rm -rf /usr/local/bin/trident-installer && \
    #chmod +x /usr/local/bin/trident
#COPY index.html /var/www/html/index.html
#EXPOSE 8080
#CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
