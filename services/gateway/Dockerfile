FROM golang:1.17.5-bullseye AS builder

WORKDIR /go/src/github.com/mercari/mercari-microservices-example

COPY go.mod go.mod
COPY go.sum go.sum
RUN go mod download

COPY . .
RUN go build -o /usr/bin/gateway ./services/gateway

CMD ["/usr/bin/gateway"]
