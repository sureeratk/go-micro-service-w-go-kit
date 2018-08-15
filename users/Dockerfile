FROM golang

RUN mkdir -p /go/src/github.com/sureeratk/go-micro-service-w-go-kit

ADD . /go/src/github.com/sureeratk/go-micro-service-w-go-kit

RUN go get  -t -v ./...
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/sureeratk/go-micro-service-w-go-kit/users/cmd  -watch github.com/sureeratk/go-micro-service-w-go-kit/users
