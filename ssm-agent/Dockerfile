# Needed for process reaping
FROM phusion/baseimage:0.11

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get install -yq \
    lsb-release \
    curl

# TODO Add in any other tools that may be needed

ENV AGENT_URL https://amazon-ssm-us-east-1.s3.amazonaws.com/latest/debian_amd64/amazon-ssm-agent.deb

RUN curl ${AGENT_URL} -o amazon-ssm-agent.deb && \
    dpkg -i amazon-ssm-agent.deb && \
    rm -f amazon-ssm-agent.deb

COPY entrypoint.sh /etc/service/ssm/run

WORKDIR /opt/amazon/ssm/
CMD ["/sbin/my_init"]
