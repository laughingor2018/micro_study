# 安装go
## 下载最新的go语言包，解压到/usr/local/
## 设置环境变量
## GOPATH=项目目录
## GOROOT=/usr/local/go
## GOBIN=项目目录/bin

## 把GOBIN加入PATH



# 安装micro
##  go get -u -v github.com/micro/micro
##  cd github.com/micro/micro
##  go install

## go get -u -v github.com/micro/go-micro


# 安装protobuf

## wget https://github.com/protocolbuffers/protobuf/releases/download/v3.8.0/protobuf-all-3.8.0.tar.gz

## tar -xvzf protobuf-all-3.8.0.tar.gz

## cd protobuf-3.8.0

## ./configure

## make

## make install

## vi /etc/ld.so.conf

## 加入/usr/local/lib

## ldconfig

## protoc --version


## go get -v -u github.com/micro/protoc-gen-micro

## cd github.com/micro/protoc-gen-micro

## go install

## go get -u github.com/golang/protobuf/{proto,protoc-gen-go}

## cd github.com/golang/protobuf/

## go install ./protoc-gen-go



# 安装go-micro

## go get -v -u github.com/micro/go-micro


# 安装micro

# go get -u -v github.com/micro/micro


# git clone https://github.com/grpc/grpc-go.git $GOPATH/src/google.golang.org/grpc

# git clone https://github.com/golang/net.git $GOPATH/src/golang.org/x/net

# git clone https://github.com/golang/text.git $GOPATH/src/golang.org/x/text

# go get -u github.com/golang/protobuf/{proto,protoc-gen-go}

# git clone https://github.com/google/go-genproto.git $GOPATH/src/google.golang.org/genproto

# cd $GOPATH/src/

# go install google.golang.org/grpc


# go-micro打包进docker中需要网络编译

## GOOS=linux GOARCH=amd64 go build -tags netgo -o rollingupdate${TAG} main.go


# 解决微服务打包

## https://studygolang.com/articles/12094?fr=sidebar


# go-micro打包进docker中也可以采用官方
## CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -ldflags '-w' -i -o micro ./main.go ./plugins.go


# rpc服务可以被打包进docker，默认是外部不能直接访问，可以指定暴露端口以及server地址，可以直接被外部直接访问，否则必须通过docker打包cli来访问
## docker run -d -p 50052:50052 -e MICRO_SERVER_ADDRESS=:50052 -e MICRO_REGISTRY=mdns service-srv


# micro网关可以被单独打包进docker，运行时必须指定--handler,否则api接口接收不到请求数据

## docker run -d -p 8080:8080 -e MICRO_API_ADDRESS=:8080 service-micro api --handler=api
## 可以指定暴露端口，已经服务地址及端口


# api服务可以被单独打包进docker

## docker run -d -e MICRO_REGISTRY=mdns service-api

