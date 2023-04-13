# Control-and-Trajectory-Tracking-for-Autonomous-Vehicles
## Project Description
In this project it has to be designed a PID controller to perform vehicle trajectory tracking. Given a trajectory as an array of locations, and a simulation environment (the vehicle with possible perturbations), a PID controller has to be designed, coded and tested its efficiency on the CARLA simulator used in the industry.

 * the Behavior Planner
 * the Motion Planner. 
 
## Step 1: Build the PID controller object
Complete the TODO in the pid_controller.h and pid_controller.cpp.
<br>
Here's a screenshot of the CARLA simulator.
![Alt text](Pic/Step1.png "Step 1")
## Step 2: PID controller for throttle
* In [main.cpp](Code/main.cpp), complete the TODO (step 2) to compute the error for the throttle pid. The error is the speed difference between the actual speed and the desired speed.
* Comment your code to explain why did you computed the error this way.
* Tune the parameters of the pid until you get satisfying results (a perfect trajectory is not expected).
## Step 3: PID controller for steer
* In [main.cpp](Code/main.cpp), complete the TODO (step 3) to compute the error for the steer pid. The error is the angle difference between the actual steer and the desired steer to reach the planned position.
* Comment your code to explain why did you computed the error this way.
* Tune the parameters of the pid until you get satisfying results (a perfect trajectory is not expected).
 ## Step 4: Evaluate the PID efficiency
![Alt text](Pic/step4.png "Steering")
![Alt text](Pic/step4_2.png "Control")

- Add the plots to your report and explain them (describe what you see)
  - The first plot shows the steering error and the second plot shows how the actuators are engaged. 
- What is the effect of the PID according to the plots, how each part of the PID affects the control command?
  - As suggested by their names: Proportional term produces an output proportional to the error,  Differential term produces an output related to the derivative of the error and reduce the oscillation, Integral term produces an output related to the error over time and improve convergence.
- How would you design a way to automatically tune the PID parameters?
  - Twiddle method can be used to automatically tune the PID controller.
- PID controller is a model free controller, i.e. it does not use a model of the car. Could you explain the pros and cons of this type of controller?
  - PID controller is generic and maybe easier to use but not considering the model of the car could introduce errors and affect performances.

## Reference code
[main.cpp](Code/main.cpp)
<br>
[pid_controller.cpp](Code/pid_controller.cpp)
<br>
[pid_controller.h](Code/pid_controller.h)

