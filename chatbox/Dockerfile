# Stage 1: Build with Git
FROM node:20-alpine AS builder

WORKDIR /app

# Install git (and optionally openssh if using SSH access)
RUN apk add --no-cache git openssh
RUN apk add --no-cache ca-certificates

# Clone your source (example: public repo)
# You could also COPY a shell script here to make this dynamic
RUN git clone https://github.com/chatboxai/chatbox.git .

# Install deps & build
RUN npm install
RUN npm run build

# Stage 2: Runtime
FROM node:20-alpine

WORKDIR /app

# Copy only built JS and dependencies
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/node_modules ./node_modules
COPY --from=builder /app/package*.json ./

# Start the app
CMD ["node", "dist/index.js"]