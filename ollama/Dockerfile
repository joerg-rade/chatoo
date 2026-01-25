# 0.14.2 / latest
FROM ollama/ollama:0.14.2
USER root
COPY zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && \
    apt-get install -y ca-certificates && \
    update-ca-certificates

