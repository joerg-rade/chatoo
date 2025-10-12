FROM ubuntu:20.04
USER root
COPY ./zscaler-root.crt /usr/local/share/ca-certificates/
RUN apt-get update && \
    apt-get install -y curl && \
    apt-get install -y ca-certificates && \
    update-ca-certificates
# Create the models directory
RUN mkdir -p /models
RUN curl -L -o /models/Phi-3-mini-128k-instruct.Q4_K_M.gguf \
    https://huggingface.co/QuantFactory/Phi-3-mini-128k-instruct.GGUF/resolve/main/Phi-3-mini-128k-instruct.Q4_K_M.gguf
