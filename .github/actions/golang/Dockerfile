FROM golang:latest

LABEL "name"="Golang workflow" \
    "com.github.actions.icon"="code" \
    "com.github.actions.color"="green-dark" \
    "com.github.actions.name"="golang　workflow" \
    "com.github.actions.description"="This is an Action to run go and go test commands."

COPY entrypoint.sh /entrypoint.sh

ENV LINT_VERSION="v1.15.0"

RUN curl -sfL https://install.goreleaser.com/github.com/golangci/golangci-lint.sh | sh -s -- -b $(go env GOPATH)/bin ${LINT_VERSION} \
  && chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
