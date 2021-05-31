## GO gRPC

### Compiling your protocol buffers

> install on windows: https://github.com/protocolbuffers/protobuf

```
go get google.golang.org/protobuf/cmd/protoc-gen-go google.golang.org/grpc/cmd/protoc-gen-go-grpc
go install google.golang.org/protobuf/cmd/protoc-gen-go google.golang.org/grpc/cmd/protoc-gen-go-grpc

go mod tidy

protoc --proto_path=proto proto/*.proto --go_out=pb --go-grpc_out=pb
```

server:

```
go run cmd/server/server.go
```

client:

```
go run cmd/client/client.go
```
