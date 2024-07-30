<img src="https://go.dev/images/gophers/pink.svg" width="150" height="150">

[![Go](https://github.com/BullionBear/crypto-engine/actions/workflows/go.yml/badge.svg)](https://github.com/yitech/golang-grpc-template/actions/workflows/go.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/BullionBear/crypto-engine)](https://goreportcard.com/report/github.com/BullionBear/crypto-engine)
[![codecov](https://codecov.io/gh/BullionBear/crypto-engine/graph/badge.svg?token=EYQLFL9HN6)](https://codecov.io/gh/BullionBear/crypto-engine)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Crypto Engine

Crypto Engine is a distributed system integrated feed, indicator, and trade as a monolithic repo.

## Directory Structure
```bash
.
├── api
│ └── helloworld.go # Generated gRPC code
├── bin # Directory for binaries
├── cmd
│ ├── client
│ │ └── main.go # gRPC client implementation
│ └── server
│   └── main.go # gRPC server implementation
├── compile_proto.sh # Script to compile protobuf files
├── go.mod # Go module file
├── go.sum # Go dependencies file
├── grpc
│ ├── helloworld # Generated gRPC code
│ ├── helloworld_grpc.pb.go
│ └── helloworld.pb.go
├── LICENSE # License file
├── Makefile # Makefile for build automation
├── proto
│ └── helloworld.proto # Protobuf file
└── README.md # This README file
```

## Getting Started

### Prerequisites

- Go 1.16 or higher
- Protocol Buffers compiler (`protoc`)
- Go plugins for `protoc`

### Install Protocol Buffers Compiler

Follow the [installation guide for `protoc`](https://grpc.io/docs/protoc-installation/).

### Install Go Plugins for `protoc`

```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```
Make sure $GOPATH/bin is in your PATH.

### Compile Protobuf Files
Use the compile_proto.sh script to compile the protobuf files:

```bash
make proto
```
### Build and Run
Use the Makefile to build the server and client binaries.

#### Build
```bash
make build
```
#### Run Server
```bash
./bin/server
```
#### Run Client
```bash
./bin/client
```

### Project Layout
- proto/helloworld.proto: Protobuf definition for the helloworld service.
- grpc/helloworld: Generated Go code for the helloworld service.
- cmd/server/main.go: Entrypoint of the gRPC server.
- cmd/client/main.go: Entrypoint of the gRPC client.
- compile_proto.sh: Script to compile protobuf files.
- Makefile: Makefile to automate the build process.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
- gRPC
- Protocol Buffers
