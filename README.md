# grpc-demo

gRPC の動作確認

## Requirement

- go 1.17.2

## Setup

protoc を使って Go 固有の gRPC コードの生成

```
$ protoc --go_out=plugins=grpc:chat chat.proto
```

grpc のインストール

```
$ go get -u google.golang.org/grpc
```

Protocol Buffers v3 をインストール

```
$ brew install protobuf
```

Protocol Buffers の Go プラグインをインストール

```
$ go get -u github.com/golang/protobuf/protoc-gen-go
```

go mod init の実行(必要であれば)

```
$ go mod init grpc-demo
```

## Usage

サーバー側の起動

```
$ go run server.go
Go gRPC Beginners Tutorial!
```

クライアント側の起動

```
$ go run client.go
2022/01/26 23:13:02 Response from server: Hello From the Server!
```
