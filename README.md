# Tibanna BIMSB

This is a fork of Tibanna for use with the Rolv platform.

We made changes to awsf3-docker:

- Remove unused packages from Dockerfile
- upload debug logs on Snakemake failures
- tag resources with "AkalinCostOwner" and "project" because for our account the "Name" tag cannot be used in AWS CostExplorer 

## Build

```sh
cd awsf3-docker
docker build --build-arg version=v5.4.3-bimsb-test .
docker tag $IMAGE bimsbbioinfo/tibanna-bimsb:latest
docker login
docker push bimsbbioinfo/tibanna-bimsb:latest
```


## TODO

- push to ECR instead of dockerhub
- change log directory for tibanna logs
