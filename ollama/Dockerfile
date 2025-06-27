FROM repository.int.kn/ollama/ollama:latest
USER root
COPY zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && apt-get install -y ca-certificates && update-ca-certificates
RUN update-ca-certificates
