# Tibanna BIMSB

This is a fork of Tibanna for use with the Rolv platform.

We made changes to awsf3-docker:

- Remove unused packages from Dockerfile
- upload debug logs on Snakemake failures

## Build

```sh
cd awsf3-docker
docker build --build-arg version=4.0.0 .
docker tag $IMAGE bimsbbioinfo/tibanna-bimsb:latest
docker login
docker push bimsbbioinfo/tibanna-bimsb:latest
```


## TODO

- push to ECR instead of dockerhub
- change log directory for tibanna logs
