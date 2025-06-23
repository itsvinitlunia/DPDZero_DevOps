#Building Stage
FROM golang:1.21-alpine AS builder

WORKDIR /app
COPY . .

RUN go mod tidy
RUN go build -o service1 main.go

# Running the stage
FROM alpine:latest

WORKDIR /app
COPY --from=builder /app/service1 .

EXPOSE 8081

CMD ["./service1"]