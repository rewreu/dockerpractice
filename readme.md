# Docker image size compression practice

1. base image in Dockerfile, this gives 1.14 GB
2. Using two stages, Dockerfile2stages gives 64.2MB 
3. compile with static library and use stratch image, DockerfileStaticlib gives 938KB
4. compile with static library in alpine, and use stratch image, DockerfileStaticlibApline gives 95.7KB

# HowTo
docker run --rm -it -v $(pwd):/tmp -w /tmp gcc gcc -o hello hello.c -static
docker run --rm -it -v $(pwd):/tmp -w /tmp frolvlad/alpine-gxx gcc -o hello2 hello.c -static
docker run --rm -it rewreu/dockerstaticlibalpine


