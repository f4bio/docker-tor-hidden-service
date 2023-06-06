# docker-tor-hidden-service

## multiarch build

```bash
docker buildx build \
  --platform linux/arm/v7,linux/arm/v8,linux/arm64 \
  --build-arg BUILD_DATE=$(date -u +'%Y-%m-%dT%H:%M:%SZ') \
  --build-arg APPLICATION_NAME=tor-hidden-service \
  --build-arg BUILD_VERSION=1.0 \
  --file Dockerfile \
  --tag f4bio/tor-hidden-service:latest \
  --push \
  .
```

## normal build

```bash
docker build \
  --build-arg BUILD_DATE=$(date -u +'%Y-%m-%dT%H:%M:%SZ') \
  --build-arg APPLICATION_NAME=tor-hidden-service \
  --build-arg BUILD_VERSION=1.0 \
  --file Dockerfile \
  --tag f4bio/tor-hidden-service:latest \
  --push \
  .
```
