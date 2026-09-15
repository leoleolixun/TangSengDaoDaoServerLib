# TangSengDaoDaoServerLib

唐僧叨叨服务端通用库，为业务模块提供配置与上下文、模块生命周期、服务装配、消息模型和基础工具。它是 Go 依赖库，没有独立的业务 API 部署入口。

## 环境与使用

- Go 兼容版本以 [go.mod](go.mod) 为准，当前声明为 Go 1.20。
- Go module 路径为 `github.com/TangSengDaoDao/TangSengDaoDaoServerLib`。
- 在 jsIM 工作区中，Server 使用的库来源以 `TangSengDaoDaoServer/go.mod` 中的 `require` / `replace` 为准。当前 Server 固定到远程 fork 版本，不会自动引用这个相邻目录；只修改本目录不代表 Server 已使用修改。
- 按改动运行对应 package 的测试；数据库、Redis 等外部依赖由相关测试自身约束，不默认连接生产环境。

## 代码入口

| 目录 | 内容 |
| --- | --- |
| `config/` | 配置、上下文及消息等公共能力 |
| `module/`、`server/` | 模块接口和服务装配 |
| `common/`、`model/`、`pkg/` | 公共模型与工具 |
| `testutil/` | 测试辅助 |
| `pkg/wkhook/` | Webhook gRPC 协议与生成代码，见 [生成说明](pkg/wkhook/README.md) |

## 许可证

使用 Apache 2.0 许可证，详见 [LICENSE](LICENSE)。


