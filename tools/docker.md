# Docker

## Speed up multi-stage build

- Build the runtime stage, using cached compile stage
```
docker build --target runtime-image \
       --cache-from=itamarst/helloworld:compile-stage \
       --cache-from=itamarst/helloworld:latest \
       --tag itamarst/helloworld:latest .
```

Reference: https://pythonspeed.com/articles/faster-multi-stage-builds/

## Override ENTRYPOINT with docker run
```
sudo docker run -it --entrypoint /bin/bash [docker_image]
```

Reference: https://phoenixnap.com/kb/docker-run-override-entrypoint

## Run docker without sudo
```
sudo usermod -aG docker anthony
```
Re-login
