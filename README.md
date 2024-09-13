# URSim with Docker
How to get URSim on docker working with "remote control"


# Important references:
* [Official UR Sim on DockerHub](https://hub.docker.com/r/universalrobots/ursim_e-series)

## Quick Guide

### If you don't have Docker installed
* Install docker - [Instructions](https://docs.docker.com/engine/install/)


### If you do have Docker installed

*  Pull the URSim repository: `docker pull universalrobots/ursim_e-series`

* Next Step: 
  1. Start the docker container as shown [here](https://hub.docker.com/r/universalrobots/ursim_e-series) or follow the commands below:
     ```
     # VNC port: 5900
     # Web browser VNC port: 6080
     docker run --rm -it -p 5900:5900 -p 6080:6080 universalrobots/ursim_e-series

     ```
  > -p 5900:5900 will publish the VNC port to the host, allowing the host to view the robots user interface with a VNC application, by connecting to localhost:5900.
  > -p 6080:6080 allows the host to view the robots user interface through a web browser with URL http://localhost:6080/vnc.html?host=localhost&port=6080⁠

  2. [localhost:8080](http://localhost:8080/)
  3. With `ifconfig` find the ip of docker
  4. python3 <your_script.py> <docker_ip>
  
