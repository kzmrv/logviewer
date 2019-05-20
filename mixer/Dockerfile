FROM alpine:3.9
COPY mixer /
RUN apk add --no-cache ca-certificates && update-ca-certificates
EXPOSE 17655:17655
ENTRYPOINT ["/mixer", "-port", "17655"]
