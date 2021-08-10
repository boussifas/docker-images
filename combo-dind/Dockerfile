FROM docker:dind

## ENABLE DOCKERBUILT
#ENV DOCKER_BUILDKIT=1

## INSTALLING NODEJS & NPM ##
Run apk add --update npm 

## INSTALLING JQ PACKAGE##
RUN apk add --no-cache curl jq 

## INSTALLING AWSCLI THROUGH PIP
RUN apk add --no-cache python3 py3-pip
RUN pip install awscli


## ANSIBLE PACKAGE ##
FROM willhallonline/ansible:latest
CMD [ "ansible-playbook", "--version" ]

## HEALTHCHECK --interval=5m --timeout=3s \ CMD curl -f http://localhost/ || exit 1

