FROM alpine:3.23

RUN apk add --no-cache olm ca-certificates ffmpeg su-exec bash jq curl yq-go

COPY matrix-line /usr/bin/matrix-line
COPY docker-run.sh /docker-run.sh
RUN chmod +x /docker-run.sh

ENV BRIDGEV2=1
WORKDIR /data
CMD ["/docker-run.sh"]
