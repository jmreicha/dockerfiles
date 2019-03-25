# Inspired by the debug container pattern found here:

# https://github.com/mauilion/debug/blob/master/Dockerfile

# TODO Multiarch
#FROM arm64v8/alpine:latest
FROM alpine:latest

#COPY --from=gcr.io/etcd-development/etcd /usr/local/bin/etcdctl /usr/local/bin/etcdctl
#COPY --from=bitnami/kubectl /opt/bitnami/kubectl/bin/kubectl /usr/local/bin/kubectl
#
#RUN chmod +x /usr/local/bin/kubectl && \
#    chmod +x /usr/local/bin/etcdctl

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
	ca-certificates

