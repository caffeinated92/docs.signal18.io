---
title: Build
---

## Building from source

* Download a Go release (Go 1.8 minimum): https://golang.org/dl/ or use your system's release if >= 1.8
* Create a build directory: `mkdir -p ~/go`
* Point GOPATH environment variable to this directory: `export GOPATH=~/go`
* Clone the source: `go get github.com/signal18/replication-manager`
* Compile and install: `go install github.com/signal18/replication-manager`
* Add the go binaries directory to your path: `export PATH=$PATH:~/go/bin`
* Compile all binaries: `make bin`

## Compilation flags

It is possible to disable features via the following tags

| Flags | Value |
| ----- | ----- |
| WithProvisioning | ON/OFF |
| WithArbitration | ON/OFF |
| WithArbitrationClient | ON/OFF |
| WithProxysql | ON/OFF |
| WithHaproxy | ON/OFF |
| WithMaxscale | ON/OFF |
| WithMariadbshardproxy | ON/OFF |
| WithMonitoring | ON/OFF |
| WithMail | ON/OFF |
| WithHttp | ON/OFF |
| WithSpider | ON/OFF |
| WithEnforce | ON/OFF |
| WithDeprecate | ON/OFF |
| WithTargz | ON/OFF |
