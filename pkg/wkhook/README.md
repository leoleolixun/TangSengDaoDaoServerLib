

# Webhook gRPC 协议

协议源文件为 [webhook.proto](webhook.proto)。只有修改协议后需要重新生成 Go 文件时，才在 `TangSengDaoDaoServerLib` 仓库根目录执行：

```shell
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative ./pkg/wkhook/webhook.proto
```

执行环境需已安装 `protoc`、`protoc-gen-go` 和 `protoc-gen-go-grpc`。生成后核对差异与调用方兼容性；不要直接编辑生成文件。
