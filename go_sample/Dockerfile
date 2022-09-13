FROM golang:1.19.1-alpine

RUN apk update && apk add git

# pre-copy/cache go.mod for pre-downloading dependencies and only redownloading them in subsequent builds if they change
# COPY go.mod go.sum ./
# RUN go mod download && go mod verify

RUN mkdir /go/src/app
WORKDIR /go/src/app
ADD . /go/src/app
