# PID Controller
The purpose of this project is to create a PID controller to drive a car smoothly and successfully with controlling steer and throttle input around the Udacity simulator .

## Implementation
- The P ('Proportional'), component had the most directly observable effect on the car's behavior. It causes the car to steer proportional (and opposite) to the car's distance from the lane center (which is the CTE) or, desired path. An issue with just using a proportional controller is overshoot.
- The I ('Integral'), component counteracts a bias in the CTE which prevents the P-D controller from reaching the center line.       We integrate over the error and feed this signal back into our controller to compensate for any drfit in the vehicle. Here I believe, in this particular implementation the 'I' component serves to reduce the CTE around curves.
- The D ('Differential'), component counteracts the P component's tendency to ring and overshoot the center line. A properly tuned D parameter will cause the car to approach the center line smoothly without ringing.

I have used the codes present in the the sdcnd and referred the open forum portals.

## Parameter / Behavior Tuning
Here "Twiddle" algorithm is used to tune the coefficient for the P, I and D components of the controller.
pid.Init(0.151, 0.0011, 1.51)

## Run the code
This project involves the Term 2 Simulator which can be downloaded ([here](https://github.com/udacity/self-driving-car-sim/releases)). Follow the instructions preesent in the classroom section 'uWebSocketIO Starter Guide' for the environment setup. Once the install for uWebSocketIO is complete, the main program can be built and run by doing the following from the project top directory.
1. mkdir build
2. cd build
3. cmake ..
4. make
5. ./pid





