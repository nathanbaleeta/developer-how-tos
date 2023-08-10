# Build Multi-Architecture Images with Buildx

#### Jumpstart your [multi-architecture build](https://www.docker.com/blog/how-to-rapidly-build-multi-architecture-images-with-buildx/)
```
docker buildx build --platform linux/amd64,linux/arm64 \
--tag your_docker_username/multi_arch_sample:buildx-latest .
```

#### Tag image
```
docker tag your_docker_username/multi_arch_sample:buildx-latest .
```
