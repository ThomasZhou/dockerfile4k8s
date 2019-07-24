FROM golang:1.12-alpine

RUN apk --no-cache add \
    bash \
    git \
    g++ \
    openssl

RUN cat <<EOF >> /etc/profile \
export HTTP_PROXY="http://172.30.65.47:8080" \
export HTTPS_PROXY="http://172.30.65.47:8080" \
export HTTP_PROXY_AUTH="basic:*:z00238418:Golang1.12.4" \
EOF

RUN cat <<EOF >> /etc/wgetrc \
http_proxy = http://z00238418:Golang1.12.4@172.18.32.221:8080 \
https_proxy = http://z00238418:Golang1.12.4@172.18.32.221:8080 \
EOF
