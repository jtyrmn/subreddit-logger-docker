FROM golang:alpine

RUN apk update
RUN apk add git

WORKDIR /app

RUN git clone https://github.com/jtyrmn/subreddit-logger-database .
RUN go build -o out

ENTRYPOINT ["./out"]