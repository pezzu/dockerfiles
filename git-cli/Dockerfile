FROM alpine:latest
RUN apk add --no-cache git
WORKDIR /sbx

ARG UID=1000
ARG GID=1000

RUN addgroup -g $GID group && adduser --disabled-password --uid $UID user --ingroup group

USER user

ENTRYPOINT ["git"]
