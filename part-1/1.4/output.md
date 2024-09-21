```
janicezhong@janices-macbook-pro devops-with-docker % docker run -d --rm -it --name exer ubuntu
b65c39fb5e695485cdbfa8332fbaa5954d526614a545524c6ed19ddcb9ec8873
janicezhong@janices-macbook-pro devops-with-docker % docker ps -a
CONTAINER ID   IMAGE     COMMAND       CREATED         STATUS         PORTS     NAMES
b65c39fb5e69   ubuntu    "/bin/bash"   3 seconds ago   Up 2 seconds             exer
janicezhong@janices-macbook-pro devops-with-docker % docker exec -it exer bash
root@b65c39fb5e69:/# apt-get update
root@b65c39fb5e69:/# apt-get install -y curl
root@b65c39fb5e69:/# while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.24.0</center>
</body>
</html>
```
