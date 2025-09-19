FROM node:18-alpine

# Install a few utilities (curl, ca-certificates) then install dart-sass via npm
RUN apk add --no-cache ca-certificates bash git \
  && npm install -g --no-audit --no-fund sass@1.78.0 \
  && rm -rf /tmp/* /var/cache/apk/*

WORKDIR /work

# Default entrypoint is the sass binary. Commands will be appended by docker run.
ENTRYPOINT ["sass"]
