FROM alpine:3.3
LABEL io.openshift.s2i.scripts-url="image:///usr/libexec/s2i"
RUN apk add --no-cache build-base
USER 1001
COPY  ["run","assemble-runtime","/usr/libexec/s2i/"]

