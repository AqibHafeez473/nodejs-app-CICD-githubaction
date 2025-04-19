FROM golang:1.18 AS builder

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download

COPY ./src .

RUN go build -o main .

FROM alpine:latest

# Install libc6-compat for compatibility
RUN apk add --no-cache libc6-compat

WORKDIR /root/

COPY --from=builder /app/main .

EXPOSE 8080

CMD ["./main"]
