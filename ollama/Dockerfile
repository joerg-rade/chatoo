FROM ollama/ollama:0.9.5
USER root
COPY ./zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && apt-get install -y ca-certificates && update-ca-certificates
RUN update-ca-certificates
