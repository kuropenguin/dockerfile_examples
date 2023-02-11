FROM golang:1.19.5

RUN apt update && apt upgrade
RUN go install github.com/cosmtrek/air@v1.29.0


WORKDIR /app

COPY go.mod go.sum ./ 

CMD ["air", "-c", ".air.toml"]
