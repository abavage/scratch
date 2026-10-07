FROM registry.redhat.io/openshift4/ose-cli-rhel9:v4.16.0-202609140237.p2.g33afbae.assembly.stream.el9
RUN dnf -y --nodocs install jq git && \
    dnf clean all && \
    curl -L -o /tmp/trident-installer-26.06.1.tar.gz https://github.com/NetApp/trident/releases/download/v26.06.1/trident-installer-26.06.1.tar.gz && \
    tar -zxpf /tmp/trident-installer-26.06.1.tar.gz -C /tmp/ && \
    cp /tmp/trident-installer/tridentctl /usr/local/bin/ && \
    rm -rf /tmp/trident*
#COPY index.html /var/www/html/index.html
#EXPOSE 8080
#CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
