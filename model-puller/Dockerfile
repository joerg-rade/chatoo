FROM ollama/ollama:latest
USER root

COPY ./zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && \
    apt-get install -y curl ca-certificates && \
    update-ca-certificates

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
