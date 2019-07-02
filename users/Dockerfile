FROM golang

RUN mkdir -p /go/src/github.com/arron1993/learn-go-bug-tracker

ADD . /go/src/github.com/arron1993/learn-go-bug-tracker

RUN go get  -t -v ./...
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/arron1993/learn-go-bug-tracker/users/cmd  -watch github.com/arron1993/learn-go-bug-tracker/users
