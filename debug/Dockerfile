# Inspired by the debug container pattern found here:

# https://github.com/mauilion/debug/blob/master/Dockerfile

# TODO Multiarch
#FROM arm64v8/alpine:latest
FROM alpine:latest

# Some packages are only availabe in edge/testing
RUN  apk add cfssl --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing

RUN apk add --no-cache \
	openssl \
	openssh-client \
	tshark \
	tcpdump \
	netcat-openbsd \
	bash \
	bash-completion \
	iputils \
	bind-tools \
	curl \
	ipvsadm \
	ca-certificates
