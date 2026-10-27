FROM golang:1.16

WORKDIR /app
COPY . .
RUN go build
ENV PORT=8080 REQUEST_ORIGIN="http://localhost"

CMD [ "./server" ]