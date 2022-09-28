# Drone Engineering Ecosystem   
![software-arch](https://user-images.githubusercontent.com/32190349/155320787-f8549148-3c93-448b-b79a-388623ca5d3f.png)

## General description

The Drone Engineering Ecosystem is a software tool that allows controlling the operation of various types of drones. 
It allows  to establish flight plans, record flight data and manage the information collected.   
    
The ecosystem contains several modules, that are briefly described in the following.

* *Dashboard*: a desktop application that allows the global control of the system. From the dashboard, 
the user can select the drone platform, control de drone operation and manage the data involved in the mission.
   
* *Mobile app*: an app for smartphones that implements a subset of the functionalities of the dashboard. 
 
* *Autopilot service*: an on-board module that controls the autopilot to execute the commands coming from the Dashboard
or the Mobile app (arm, takeoff, go to position, etc.) 

* *Camera service*: an on-board module that controls the on-board camera to execute the commands coming from
the Dashboard or the Mobile app (take a picture, get the video stream, etc.)   
   
* *LEDs service*: an on-board module that controls the LEDs of the drone platform to inform
of the status of the drone platform, as required by other modules.    
  
* *gate*: connects the on-board modules with the external modules.    

* *Local broker*: on-board middleware that connects the on-board modules through publications and subscription.   

* *Global broker*: middleware that connects the gate with the external modules through publications and subscription.    

* *API REST*: a server that provides data storage and retrieval through HTTP basic operations (GET, POST, PUT, DELETE).      

* *Data service*: provides the required by the rest of modules interface to access data in the API REST
via publications and subscriptions. 

The Mission Planner module that appears in the figure does not belong to the Ecosystem,
but is used for development purposes, since it provides an autopilot simulator, 
so that the ecosystem can be developed and tested without requiring a real drone platform.

## Demo   
[Drone Engineering Ecosystem demo](https://www.youtube.com/playlist?list=PL64O0POFYjHpXyP-T063RdKRJXuhqgaXY)   

## DroneApp
Mobile app made with the help of the Python library named **Kivy** made to develop GUI, especially for mobile devices.
These are the current functionalities of the mobile app:
- Start/Stop a LEDs sequence in the drone
- Take a picture in the built-in camera of the drone
- Start/Stop a streaming video from the built-in camera of the drone
- Arm/Disarm the drone
- Go to a certain position

## Example and tutorials

A nice course on Kivy can be found here:   
[Kivy](https://www.youtube.com/watch?v=l8Imtec4ReQ)   