# protocol

```shell
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

More to read [regenerate-grpc-code](https://grpc.io/docs/languages/go/quickstart/#regenerate-grpc-code).

- Run `mage` to gen rpc_caller.

## [Generate Protocol Buffers with Mage](./mage-README.md)


1、配置环境
export PATH=$PATH:/www/wwwroot/proto/bin

protoc  --version
2、配置gen-go
export PATH=$PATH:$(go env GOPATH)/bin

protoc-gen-go --version
3、加入代码
protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    office/office.proto