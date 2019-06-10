### 安装go
下载最新的go语言包，解压到/usr/local/
设置环境变量
GOPATH=项目目录
GOROOT=/usr/local/go
GOBIN=项目目录/bin

把GOBIN加入PATH



### 安装micro
# go get -u -v github.com/micro/micro
# cd github.com/micro/micro
# go install

#go get -u -v github.com/micro/go-micro


###安装protobuf

#wget https://github.com/protocolbuffers/protobuf/releases/download/v3.8.0/protobuf-all-3.8.0.tar.gz

#tar -xvzf protobuf-all-3.8.0.tar.gz

#cd protobuf-3.8.0

#./configure

#make

#make install

#vi /etc/ld.so.conf

#加入/usr/local/lib

#ldconfig

#protoc --version


#git -v -u github.com/micro/protoc-gen-micro

# cd github.com/micro/protoc-gen-micro

# go install

#go get -u github.com/golang/protobuf/{proto,protoc-gen-go}

#cd github.com/golang/protobuf/

#go install ./protoc-gen-go

