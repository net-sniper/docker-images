FROM cargo.caicloud.io/caicloud/centos:7.2.1511

ENV GOLANG_VERSION 1.9.2
ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH $PATH:$GOPATH/bin:$GOROOT/bin

RUN yum update -y 											\
	&& yum install -y wget tar g++ gcc libc6-dev make glibc.i686	 	\
	&& wget -O go.tgz "https://golang.org/dl/go1.9.2.linux-386.tar.gz" \
	&& tar -C /usr/local -zxf go.tgz 						\
	&& rm -f go.tgz											\
	&& mkdir -p "$GOPATH/src" "$GOPATH/bin" 				\
	&& chmod -R 777 "$GOPATH"

