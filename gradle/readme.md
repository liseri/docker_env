# 镜像编译
docker build -t my/gradle:7.4.2-jdk17-jammy .
# 使用镜像编译gradle项目
docker run --rm -it -u gradle -v ~/.gradle:/home/gradle/.gradle  -v "$PWD":/home/gradle/project -w /home/gradle/project my/gradle:7.4.2-jdk17-jammy gradle desktop:package