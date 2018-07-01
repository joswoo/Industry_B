# Industry_B   
**'Balancing Bot'**

--------------------------------------------------------------------------
# ABSTRACT


*A lot of machine learning algorithms are being developed these days. Therefore, various algorithms that can improve the performance of existing control systems have also been improved. 
In this paper, we will learn the fundamental principles of various algorithms and optimize PID parameters using specific reinforcement learning algorithms. 
By using this algorithm, it is possible to easily balance and shorten the calculation time, so that it is possible to establish a good working environment. Therefore, this research team wants to analyze the pros and cons of the basic platform as much as possible and develop a platform suited to the target.*

--------------------------------------------------------------------------
# INTRODUCTION



**▶ Motivation**

*During the past decades, Engineering techniques have made great advancements in industry. Especially in control engineering, PID control is the most used. This technique is centered around a self-balancing posture control technique. It is possible to control the posture by oneself from external factors and is utilized in many fields. Segway is the product that is applied where we are closest and accessible. It allows users to maintain their own balance so that they do not fall within a certain range even if the center of gravity is changed randomly.*

*As such, PID technology is the most widely used technology, and it is thought to be applied to more fields in the future, but this control technique is difficult to handle. It requires a lot of expertise, and it takes a lot of time to tune the products using this technology. After all, this requires a lot of cost and time.*

*In order to solve these problems, ‘Parameter Optimization of PID Controller by Reinforcement Learning’ was selected as a research topic. We want to change this technology into a more accessible and easier-to-handle technology by combining the reinforcement learning algorithm. Reinforcement learning is a kind of machine learning, it has been reported that machine learning is suitable for sophisticated works, We want to be able to tune our PID technology through this reinforcement learning. We will implement it using a two wheeled self balancing bot.*




**▶ Previous Work**

*Our work is an early stage, we have studied PID control, and now we are demonstrating PID. It still has unstable control and will do a little more tuning work.
This is the final content of our interim report and we will soon be entering PID modeling.*



--------------------------------------------------------------------------------------
# PROPOSED METHODS


 
**▶ Motivation**


*A proportional–integral–derivative controller (PID controller or three term controller) is a control loop feedback mechanism widely used in industrial control systems and a variety of other applications requiring continuously modulated control.
In practical terms it automatically applies accurate and responsive correction to a control function. An everyday example is the cruise control on a road vehicle; where external influences such as gradients would cause speed changes, and the driver has the ability to alter the desired set speed. The PID algorithm converts the actual speed to the desired speed in the optimum way, without delay or overshoot, by controlling the power output of the vehicle's engine.
The distinguishing feature of the PID controller is the ability to use the three control terms of proportional, integral and derivative influence on the controller output to apply accurate and optimal control. 
Term P is proportional to the current value of the SP − PV error e(t). 
Term I accounts for past values of the SP − PV error and integrates them over time to produce the I term.
Term D is a best estimate of the future trend of the SP − PV error, based on its current rate of change.*

**▶ Reinforcement learning** 


*Reinforcement learning is an area of machine learning. It is a method to select an action or action sequence that maximizes the compensation among the selectable actions by recognizing the current state of the agent defined in an environment.These problems are so comprehensive that they are also studied in areas such as game theory, control theory, operational science, information theory, simulation-based optimization, multiagent systems, flock intelligence, statistics, and genetic algorithms.*

*The field in which reinforcement learning is studied in operational science and control theory is called "approximate dynamic programming". Reinforcement learning is also used to explain how equilibrium can occur under limited rationality. The 'environment' covered in reinforcement learning is mainly given by the Markov decision process.*

*Reinforcement learning also differs from general guidance learning in that there is no training set consisting of input and output pairs and no explicit correction is made for wrong behavior. Instead, the focus of reinforcement learning is on-line performance, which is enhanced by balancing exploration and exploitation.*

*Reinforcement means the frequency of action that given reward is increased. This method interact with environment and determine actions sequentially. This method do automatic tuning for PID parameter. so, it can compute more.*


-----------------------------------------------------------------------------------------
# CONCLUSION




*We created a balancing bot using a gyro sensor and a PID sensor. However, by repeatedly activating the balancing bot to determine the PID parameter value, this process is very cumbersome. Passively setting the PID parameters resulted in bad results for the balancing bot to continue to fall.*

*To overcome the difficulties of this semester, we will optimize the PID parameters based on the reinforcement learning algorithm in the second semester. To apply various parameter values of PID control to machine learning, we will train the algorithm with correct and incorrect answers.*

*The final plan is to use ML to improve the performance of PID control and to create a balancing bot that is more balanced than this semester and submit it to the graduation work.*




--------------------------------------------------------------------------------------------------------------
## Library

- PID
- I2Cdev
- LMotorController
- MPU6050


---------------------------------------------------------------------------------------------
## Arduino code
### ▶ Setting gyro offset


follow this site
http://42bots.com/tutorials/arduino-script-for-mpu-6050-auto-calibration/



### ▶ Setting PID parameter

```
//PID
double originalSetpoint = 172.50;
double setpoint = originalSetpoint;
double movingAngleOffset = 0.1;
double input, output;

//adjust these values to fit your own design
double Kp = 55;   
double Kd = 3;
double Ki = 270;
PID pid(&input, &output, &setpoint, Kp, Ki, Kd, DIRECT);
```

--------------------------------------------------------------------------------------------------
## Project Video Link




[![Alt text for your video](https://img.youtube.com/vi/iVVoLgYuxLA/0.jpg)](https://www.youtube.com/watch?v=iVVoLgYuxLA)
