# DHT Tracer

## Requirements

 - Go
 - Jaeger All-in-One
 - Docker (optional)

## Installation

### DHT Tracer

```
$ go get github.com/libp2p/dht-tracer

$ cd $GOPATH/src/github.com/libp2p/dht-tracer

$ make install
```

### Jaeger

#### Docker Installation

```
$ docker run -d --name jaeger \
  -e COLLECTOR_ZIPKIN_HTTP_PORT=9411 \
  -p 5775:5775/udp \
  -p 6831:6831/udp \
  -p 6832:6832/udp \
  -p 5778:5778 \
  -p 16686:16686 \
  -p 14268:14268 \
  -p 9411:9411 \
  jaegertracing/all-in-one:1.12
```

#### Binary Installation

For macOS:
```
# Download the archive
$ wget https://github.com/jaegertracing/jaeger/releases/download/v1.12.0/jaeger-1.12.0-darwin-amd64.tar.gz
# Extract the binary
$ tar xvf jaeger-1.12.0-darwin-amd64.tar.gz
# Run the all-in-one binary
$ jaeger-1.12.0-darwin-amd64/jaeger-all-in-one --collector.zipkin.http-port=9411
```

For linux:
```
# Download the archive
$ wget https://github.com/jaegertracing/jaeger/releases/download/v1.12.0/jaeger-1.12.0-linux-amd64.tar.gz
# Extract the binary
$ tar xvf jaeger-1.12.0-linux-amd64.tar.gz
# Run the all-in-one binary
$ jaeger-1.12.0-linux-amd64/jaeger-all-in-one --collector.zipkin.http-port=9411
```
