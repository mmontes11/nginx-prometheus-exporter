FROM golang:1.14

LABEL maintainer="Martín Montes <martin11lrx@gmail.com>"

ENV WORKDIR /go/src/github.com/nginxinc/nginx-prometheus-exporter
RUN mkdir -p ${WORKDIR}
WORKDIR ${WORKDIR}
COPY . ${WORKDIR}

RUN make build

EXPOSE 9113

ENTRYPOINT [ "bin/nginx-prometheus-exporter" ]
