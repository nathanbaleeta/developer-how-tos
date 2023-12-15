# Build multi-architecture images with Buildx

#### Specifying the platform for both the build command and version tag - Docker in fact detects the Apple M1 Pro platform as linux/arm64/v8
```
# Build for AMD64
docker buildx build --platform=linux/amd64 -t <image-name>:<version>-amd64 .

# Build for ARM64 
docker buildx build --platform=linux/arm64/v8 -t <image-name>:<version>-arm64 .
docker buildx build --build-arg VERSION=3.8.2 --platform=linux/arm64/v8 -t <image-name>:<version>-arm64
```


#### Tag image - Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
```
docker tag <SOURCE_IMAGE>:<TAG> <TARGET_IMAGE:TAG>
docker tag hello-world:latest nbaleeta/hello-world:latest
```

#### Login to your remote container registry
```
docker login

OR

docker login myregistry.azurecr.io
```

#### Upload an image to a [registry](https://docs.docker.com/engine/reference/commandline/push/)
```
docker push <image>:<version>
docker push nbaleeta/hello-world
```

#### Pull public image from Azure Container Registry
```
docker pull myregistry.azurecr.io/hello-world:latest
```
