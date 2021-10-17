# demo-docker

# inspect running docker containers command
docker ps
# docker build command example
docker build -t tag_name .

# entering in an already running container command
docker exec -t container_id bash

# docker mounting shared volume
docker run -it -v inside_computer:inside_docker tag_name

# docker X11 (GUI) pass thru
docker run -it ---env="QT_X11_NO_MITSHM=1" \
 		-v /tmp/.X11-unix:/tmp/.X11-unix \
 		-e DISPLAY=unix$DISPLAY \
         tag_name