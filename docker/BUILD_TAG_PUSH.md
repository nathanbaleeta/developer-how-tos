# Build Multi-Architecture Images with Buildx

#### Jumpstart your [multi-architecture build](https://www.docker.com/blog/how-to-rapidly-build-multi-architecture-images-with-buildx/)
```
docker buildx build --platform linux/amd64,linux/arm64/v8 \
                    --tag <image-name>:<version> .
```

#### Specifying the platform to both the build command and version tag - Docker in fact detects the Apple M1 Pro platform as linux/arm64/v8
```
# Build for AMD64
docker buildx build --platform=linux/amd64 -t <image-name>:<version>-amd64 .

# Build for ARM64 
docker buildx build --platform=linux/arm64/v8 -t <image-name>:<version>-arm64 .
```

#### Tag image - Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
```
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
docker tag hello-world:latest nbaleeta/hello-world:latest
```

#### Upload an image to a [registry](https://docs.docker.com/engine/reference/commandline/push/)
```
docker push [OPTIONS] NAME[:TAG]
docker push nbaleeta/hello-world
```
