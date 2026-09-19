###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build

RUN apt update && apt install -y golang-go

ENV GO111MODULE=off

COPY . .

RUN CGO_ENABLED=0 go build -o /app .


############################################
# MULTI STAGE BUILD WITH DISTROLESS IMAGE
############################################

FROM scratch

COPY --from=build /app /app

ENTRYPOINT ["/app"]
