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


## git -v -u github.com/micro/protoc-gen-micro

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
