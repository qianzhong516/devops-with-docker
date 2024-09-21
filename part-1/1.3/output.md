```
janicezhong@janices-macbook-pro devops-with-docker % docker run -d --rm -it --name exer devopsdockeruh/simple-web-service:ubuntu
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
0c1591f2455f6f819e837d96e21f122da70e4dd1d0c40ece7349d7416af8c6da
janicezhong@janices-macbook-pro devops-with-docker % docker ps -a
CONTAINER ID   IMAGE                                      COMMAND                 CREATED         STATUS         PORTS     NAMES
0c1591f2455f   devopsdockeruh/simple-web-service:ubuntu   "/usr/src/app/server"   9 seconds ago   Up 9 seconds             exer
janicezhong@janices-macbook-pro devops-with-docker % docker exec -it exer bash
root@0c1591f2455f:/usr/src/app# tail -f ./text.log
2024-09-21 11:21:27 +0000 UTC
2024-09-21 11:21:29 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-09-21 11:21:31 +0000 UTC
2024-09-21 11:21:33 +0000 UTC
2024-09-21 11:21:35 +0000 UTC
2024-09-21 11:21:37 +0000 UTC
2024-09-21 11:21:39 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-09-21 11:21:41 +0000 UTC
2024-09-21 11:21:43 +0000 UTC
^C
root@0c1591f2455f:/usr/src/app# exit
exit
janicezhong@janices-macbook-pro devops-with-docker % docker kill exer
exer
janicezhong@janices-macbook-pro devops-with-docker % docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```
