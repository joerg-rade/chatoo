FROM ollama/ollama:latest
# --- COMMON-BEGIN ---
USER root
COPY ./zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && \
    apt-get install -y ca-certificates && \
    update-ca-certificates
# --- COMMON-END --- \
