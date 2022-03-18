# Ubuntu Desktop Dockerfile

Docker container for Ubuntu 16.04 including ubuntu-desktop and vncserver.

# How to run

`docker run  --name qsynclient -p 5901:5901 -v /volume:/data ubuntu-desktop`

# How to install Qsync-client
step1:
docker cp QNAPQsyncClientUbuntux64-1.0.6.2624.deb qsynclient:/
step2:
docker exec -it qsynclient bash
step3:
dpkg -i /QNAPQsyncClientUbuntux64-1.0.6.2624.deb


and then connect to:

`vnc://<host>:5901` via VNC client.

The VNC password is `password`.

Application --> Other --> QNAP Qsync Client
