FROM alpine:3.9
COPY worker /
RUN apk add --no-cache ca-certificates && update-ca-certificates
EXPOSE 17654:17654
ENTRYPOINT ["/worker", "-port", "17654"]
