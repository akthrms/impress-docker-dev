FROM golang:1.16 as builder

COPY ./main.go ./
RUN go build -o /sample-go-app ./main.go


FROM gcr.io/distroless/base

EXPOSE 8080
COPY --from=builder /sample-go-app /.
ENTRYPOINT ["./sample-go-app"]
