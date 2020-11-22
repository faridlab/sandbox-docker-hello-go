## Playing around with Docker

Create `Dockerfile`
```Dockerfile
FROM golang

COPY main.go /app/main.go

CMD ["go", "run", "/app/main.go"]
```

## Build image from Dockerfile
```bash
$ docker build --tag [your-image-name]:1.0 .
Sending build context to Docker daemon  66.05kB
Step 1/3 : FROM golang
latest: Pulling from library/golang
756975cb9c7e: Pull complete
d77915b4e630: Pull complete
5f37a0a41b6b: Pull complete
96b2c1e36db5: Pull complete
145393847161: Pull complete
71dfa979a65c: Pull complete
88a83f11b30a: Pull complete
Digest: sha256:cf46c759511d0376c706a923f2800762948d4ea1a9290360720d5124a730ed63
Status: Downloaded newer image for golang:latest
 ---> 6d8772fbd285
Step 2/3 : COPY main.go /app/main.go
 ---> 9b7fc412bc1e
Step 3/3 : CMD ["go", "run", "/app/main.go"]
 ---> Running in 8007cabcb542
Removing intermediate container 8007cabcb542
 ---> 05f7118af369
Successfully built 05f7118af369
Successfully tagged [your-image-name]:1.0
```
