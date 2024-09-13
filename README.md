# URSim with Docker
How to get URSim on docker working with **Remote Control**


# Important references:
* [Official UR Sim on DockerHub](https://hub.docker.com/r/universalrobots/ursim_e-series)

## Quick Guide

### If you don't have Docker installed
* Install docker - [Instructions](https://docs.docker.com/engine/install/)


### If you do have Docker installed

*  Pull the URSim repository: `docker pull universalrobots/ursim_e-series`

* Next Steps: 
1. Start the docker container as shown [here](https://hub.docker.com/r/universalrobots/ursim_e-series) or follow the commands below:
     ```
     
     docker run --rm -it -p 5900:5900 -p 6080:6080 universalrobots/ursim_e-series

     ```
     > # VNC port: 5900
     > # Web browser VNC port: 6080
     > -p 5900:5900 will publish the VNC port to the host, allowing the host to view the robot's user interface with a VNC application, by connecting to localhost:5900.
     > -p 6080:6080 allows the host to view the robot's user interface through a web browser with URL http://localhost:6080/vnc.html?host=localhost&port=6080⁠

  In your terminal you should get something like this:
  ![image](https://github.com/user-attachments/assets/c621288c-b6ba-4f54-b9b8-762e927ab7bb)

2. Take note of the IP of the simulator that appears on your terminal (red block) and open the link that is shown on your terminal (green block) in your preferred browser:

![ur_ip](https://github.com/user-attachments/assets/9a6ac9e3-1c40-4fd2-a81b-96348a9470fa)

3. Initialize the robot:

https://github.com/user-attachments/assets/552ea76b-ee6a-4ba7-8e2c-406c7fe72997
   
4. Enable remote control on the simulated robot:

https://github.com/user-attachments/assets/5b7dc5be-ecee-4414-aaac-cdcd4d09b53a

5. Change to Remote Control Mode:
   
https://github.com/user-attachments/assets/868ac612-d553-4243-96c1-0f96fce8890b

6. **Use the IP of the simulator in your control code/script**

7. To see the robot while your code is running you need to do a little "hack" and change from Remote to Local to be able to switch tabs and see your simulated robot.
   When your code connects and runs you'll see a green "Running" on the screen. 

https://github.com/user-attachments/assets/ef825300-c69a-44cd-acd5-528595815bd1


   
  
