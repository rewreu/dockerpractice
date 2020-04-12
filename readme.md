# Docker image size compression practice

1. base image in Dockerfile, this gives 1.14 GB
2. Using two stages, Dockerfile2stages gives 64.2MB 
3. compile with static library and use stratch image, DockerfileStaticlib gives 938KB
4. 