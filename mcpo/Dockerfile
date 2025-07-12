FROM python:3.11-slim

WORKDIR /app

# Install Node.js and npm directly
RUN apt-get update && \
    apt-get install -y nodejs npm && \
    apt-get clean

# Verify installation
RUN node -v && npm -v && npx --version

# Install OpenAPI MCP Server globally
RUN npm install -g @ivotoby/openapi-mcp-server

# Install mcpo Python package
RUN pip install mcpo

COPY config.json /app/config.json

EXPOSE 8000

CMD ["mcpo", "--config", "/app/config.json", "--port", "8000"]
