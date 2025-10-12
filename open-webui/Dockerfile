# Start from the official Open WebUI image
FROM ghcr.io/open-webui/open-webui:0.6.25
# --- COMMON-BEGIN ---
USER root
COPY ./zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && \
    apt-get install -y ca-certificates && \
    update-ca-certificates \
# --- COMMON-END ---
