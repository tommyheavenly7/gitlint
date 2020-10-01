FROM python:3-alpine

RUN apk update && apk add --no-cache git openssh
RUN pip install gitlint
WORKDIR /git
ENTRYPOINT [ "/usr/local/bin/gitlint" ]
