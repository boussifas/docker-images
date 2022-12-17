FROM docker:20.10.22-dind

## INSTALLING JQ PACKAGE##
RUN apk add --no-cache curl jq git

## INSTALLING AWSCLI THROUGH PIP
RUN apk add --no-cache python3 py3-pip
RUN pip install awscli

## INSTALLING KUBECTL
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.1/bin/linux/amd64/kubectl
RUN chmod u+x kubectl && mv kubectl /bin/kubectl