# Text-to-Speech

Using Linux `flite` for simple Text-to-Speech  
Leverages Docker, go, gRPC, Kubernetes and cgo

## `Run`

```shell
cd backend
make build
docker run --rm -v $(pwd)/data:/data -w /data campoy/say "hello"

# Play output
aplay data/out.wav  # Linux
afplay data/out.waw # MacOS
```

## `Debugging`

```shell
# If you have Linux test without docker
cd backend
go run main.go "hello"
aplay out.wav
```

Spawn new docker container with vi

```shell
docker run -it --name vi debian
```

## Timeline

- add gRPC and endpoints as API
- Connect Docker containers to K8
- Add Docker multistage build
- Publish and stage K8 build to GCP
