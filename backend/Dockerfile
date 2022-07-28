FROM alpine

RUN apk update && apk add flite
# Add compiled go package after running `make build`
ADD app /app
ENTRYPOINT ["/app"]
