## Playing around with Docker

Create `Dockerfile`
```Dockerfile
FROM golang

COPY main.go /app/main.go

CMD ["go", "run", "/app/main.go"]
```

