```
janicezhong@janices-macbook-pro 1.8 % docker build . -t web-server
[+] Building 1.2s (5/5) FINISHED                                                                                          docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                      0.0s
 => => transferring dockerfile: 93B                                                                                                       0.0s
 => [internal] load .dockerignore                                                                                                         0.0s
 => => transferring context: 2B                                                                                                           0.0s
 => [internal] load metadata for docker.io/devopsdockeruh/simple-web-service:alpine                                                       1.2s
 => [1/1] FROM docker.io/devopsdockeruh/simple-web-service:alpine@sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e054  0.0s
 => => resolve docker.io/devopsdockeruh/simple-web-service:alpine@sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e054  0.0s
 => exporting to image                                                                                                                    0.0s
 => => exporting layers                                                                                                                   0.0s
 => => writing image sha256:978fbf315695ef5a3ec2e77ee411c4dcd9aa9b867fbc7ea3d26962545fda0585                                              0.0s
 => => naming to docker.io/library/web-server                                                                                             0.0s

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview
janicezhong@janices-macbook-pro 1.8 % docker run web-server
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```
