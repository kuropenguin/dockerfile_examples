FROM golang:1.19.1-alpine

RUN apk update && apk add git


RUN go install -v golang.org/x/tools/gopls@latest \
	&& go install -v github.com/ramya-rao-a/go-outline@latest \
	&& go install -v golang.org/x/tools/cmd/goimports@latest \
	&& go install -v github.com/mdempsky/gocode@latest

RUN mkdir /go/src/app
WORKDIR /go/src/app

# pre-copy/cache go.mod for pre-downloading dependencies and only redownloading them in subsequent builds if they change
COPY . ./
RUN go mod download && go mod verify
