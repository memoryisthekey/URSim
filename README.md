# URSim
How to get URSim on docker working with "remote control"


# Important references:
* [Official UR Sim on DockerHub](https://hub.docker.com/r/universalrobots/ursim_e-series)
* [git repository with example use](https://github.com/ahobsonsayers/DockURSim)

## Quick Guide
* Assuming you have docker installed and configured
  1. Start the docker container as shown [here](https://github.com/ahobsonsayers/DockURSim#example-usage):
     ```
     cd ~/ && mkdir programs
     ```
     ```    
     docker run -d \
      --name="dockursim" \
      -e ROBOT_MODEL=UR5 \
      -p 8080:8080 \
      -p 29999:29999 \
      -p 30001-30004:30001-30004 \
      -v /${HOME}/programs:/ursim/programs \
      --privileged \
      --cpus=1 \
      universalrobots/ursim_e-series
     ```
  2. [localhost:8080](http://localhost:8080/)
  3. With `ifconfig` find the ip of docker
  4. python3 <your_script.py> <docker_ip>
  
