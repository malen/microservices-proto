# microservices-proto

# 事前准备
下载protoc 可执行文件，用来生成接口库(pb文件)，这里以Windows环境为例：
https://github.com/protocolbuffers/protobuf/releases/download/v30.1/protoc-30.1-win64.zip

解压之后，将protoc.exe文件移动到%USERPROFILE%\go\bin 目录中

## Protocol buffers
### Generating Go source code
 protoc \
    --go_out=. \
    --go_opt=paths=source_relative \
    --go-grpc_out=. \
    --go-grpc_opt=paths=source_relative \
    payment.proto