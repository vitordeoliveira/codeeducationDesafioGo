FROM golang:alpine as builder

WORKDIR /usr/src/app

COPY . .

RUN  go build hello-world.go
RUN rm hello-world.go

FROM alpine

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app .

CMD [ "./hello-world" ]

