FROM node:8.7.0-alpine
ENV npm_package_engines_vscode=^1.8.1
RUN apk add --update git && \
    rm -rf /tmp/* /var/cache/apk/*
RUN git clone https://github.com/vscode-icons/vscode-icons.git app
VOLUME [ "/app-out" ]
WORKDIR /app
COPY build.sh .
CMD [ "sh", "./build.sh" ]
