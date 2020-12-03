FROM golang:1-alpine

RUN apk add --no-cache git \
  && go get -d -v github.com/hacker795/dosattack \
  && go install github.com/hacker795/dosattack \
  && rm -rf ~/go/src/github.com/hacker795/dosattack \
  && apk del git

ENTRYPOINT ["dosattack"]

CMD ["--help"]
