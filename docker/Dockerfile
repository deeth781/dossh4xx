FROM golang:1-alpine
LABEL maintainer="Alexander I.Grafov <grafov@gmail.com>"

RUN apk add --no-cache git \
  && go get -d -v github.com/grafov/H4X \
  && go install github.com/grafov/H4X@latest \
  && rm -rf ~/go/src/github.com/grafov/H4X \
  && apk del git

ENTRYPOINT ["H4X"]

CMD ["--help"]
