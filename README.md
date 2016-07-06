This is a jenkins slave primarily for use with area51/jenkins but should work with any jenkins server.

Full documentation: https://area51.onl/Docker/JenkinsSlave

The user is jenkins and the default password is jenkins. To change simply add -e JENKINS_PASSWORD=newpassword when running the image.

Mountable volumes:
* /var/run/docker.sock allows you to run docker commands within the slave. Normally you'd run it with -e /var/run/docker.sock:/var/run/docker.sock and nothing else.
* When using docker you can get the container to log in (so you can deploy images from jobs) with -e DOCKER_USER=userOrOrganisation -e DOCKER_PASSWORD=password
* Optionally you can use a local docker repository when logging in by adding -e DOCKER_SERVER=hostname

