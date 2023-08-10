# Build Multi-Architecture Images with Buildx

#### Jumpstart your multi-architecture build
```
docker buildx build --platform linux/amd64,linux/arm64 \
--tag your_docker_username/multi_arch_sample:buildx-latest .
```
