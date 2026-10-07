FROM registry.redhat.io/openshift4/ose-cli-rhel9:v4.16.0-202609140237.p2.g33afbae.assembly.stream.el9
ARG TRIDENT
ARG TRIDENT_PROTECT

RUN dnf -y --nodocs install jq git && \
    dnf clean all && \
    # trident
    #curl -L -o /tmp/trident-installer-26.06.1.tar.gz https://github.com/NetApp/trident/releases/download/v26.06.1/trident-installer-26.06.1.tar.gz && \
    curl -L -o /tmp/trident-installer-${TRIDENT}.tar.gz https://github.com/NetApp/trident/releases/download/v${TRIDENT}/trident-installer-${TRIDENT}.tar.gz && \
    tar -zxpf /tmp/trident-installer-${TRIDENT}.tar.gz -C /tmp/ && \
    cp /tmp/trident-installer/tridentctl /usr/local/bin/ && \
    # protect
    curl -L -o /tmp/tridentctl-protect-linux-amd64  https://github.com/NetApp/tridentctl-protect/releases/download/v${TRIDENT_PROTECT}/tridentctl-protect-linux-amd64 && \
    mv /tmp/tridentctl-protect-linux-amd64 /usr/local/bin/tridentctl-protect && \
    chmod +x /usr/local/bin/tridentctl-protect && \
    rm -rf /tmp/trident*
#COPY index.html /var/www/html/index.html
#EXPOSE 8080
#CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
