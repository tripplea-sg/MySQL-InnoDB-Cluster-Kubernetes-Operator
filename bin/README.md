## Installing from Binary

If pulling the Docker image from Docker Hub is not an option, you can build the Triplea-Operator image locally by following these steps:

1. **Download the required files**  
   Obtain the `triplea-operator.tar.gz` archive and the `Dockerfile`.

2. **Extract the archive**  
```bash
tar -zxvf triplea-operator.tar.gz
```
3. **Build the docker image**  
```
docker build --memory 2g --cpus 4 -t triplea-operator:1.0 .
```
