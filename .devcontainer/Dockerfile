FROM qmcgaw/godevcontainer
RUN apk add bind-tools
RUN apk add curl
RUN apk add git
RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
RUN go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
RUN echo 'export PATH="$PATH:$(go env GOPATH)/bin"' >> ~/.zshrc
RUN apk update && apk add --no-cache make protobuf-dev
COPY . .
