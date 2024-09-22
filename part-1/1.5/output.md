```
janicezhong@janices-macbook-pro devops-with-docker % docker image ls
REPOSITORY                          TAG       IMAGE ID       CREATED       SIZE
ubuntu                              latest    2b1b17d5e5a2   3 weeks ago   101MB
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   3 years ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   3 years ago   15.7MB
janicezhong@janices-macbook-pro devops-with-docker % docker run -d devopsdockeruh/simple-web-service:alpine
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
3825f8ceb0c1ed8c2c5885c87b656af649c670c3695897befec35ce7e98b0718
janicezhong@janices-macbook-pro devops-with-docker % docker exec -it 3825f8 sh
/usr/src/app # tail -f ./text.log
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-09-22 15:04:27 +0000 UTC
2024-09-22 15:04:29 +0000 UTC
2024-09-22 15:04:31 +0000 UTC
2024-09-22 15:04:33 +0000 UTC
2024-09-22 15:04:35 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-09-22 15:04:37 +0000 UTC
2024-09-22 15:04:39 +0000 UTC
2024-09-22 15:04:41 +0000 UTC
2024-09-22 15:04:43 +0000 UTC
2024-09-22 15:04:45 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-09-22 15:04:47 +0000 UTC
2024-09-22 15:04:49 +0000 UTC
2024-09-22 15:04:51 +0000 UTC
2024-09-22 15:04:53 +0000 UTC
2024-09-22 15:04:55 +0000 UTC
```
