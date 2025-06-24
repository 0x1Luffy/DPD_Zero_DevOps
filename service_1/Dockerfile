# Use the official Go image
FROM golang:1.22-alpine

# Set working directory
WORKDIR /app

# Copy source code
COPY main.go .

# Initialize Go module
RUN go mod init service1

# Install curl for health checks
RUN apk add --no-cache curl

# Expose port
EXPOSE 8001

# Run using go run
CMD ["go", "run", "main.go"]