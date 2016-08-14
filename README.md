# DIY Hardware in Loop Simulation Testing Setup
This project is motivated from need to develop low cost HIL testing without use of expensive equipments. It uses the computational power of laptop computer to simulate the models in real time.
Currently the system is designed for single hardware input but can be extended to multiple input and outputs by using other data acquisition devices.
Requirements:
>Hardware
>>Arduino Uno (Any data acquisition device which can interact with simulink in real time)

>Software:
>> Matlab and Simulink.

Sample HIL simulation models are:
1) HIL testing of torque control knob of engine dynanometer. (https://youtu.be/6i_u7KHAUhQ)

  Files: 'EngineTorqueControl.slx' and 'arduino_daq.slx'
  'arduino_daq.slx' is to be flashed on Arduino board to receive data from analog input and send it to simulink via serial port.
  'EngineTorqueControl.slx' contain the model of engine and dyno controller. Also the input serial data from arduino is liked to controller.
  Note: The engine subsystem is kept empty so that one can easily replace their specific engine with it.

2) Accelerator Pedal to control of  hybrid vehicle.
  "Currently this is under development"
