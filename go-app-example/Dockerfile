# syntax=docker/dockerfile:1

FROM golang:1.17 AS build

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY *.go ./

RUN go build -o /myapp

##
## Deploy
##
FROM gcr.io/distroless/base-debian10

WORKDIR /

COPY --from=build /myapp /myapp

EXPOSE 3000

CMD [ "/myapp" ]
