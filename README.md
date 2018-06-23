# Industry_B

## Balancing Bot

## Library
- PID
- I2Cdev
- LMotorController
- MPU6050

## Arduino code
### Setting gyro offset
follow below site
[http://42bots.com/tutorials/arduino-script-for-mpu-6050-auto-calibration/]

### Setting PID parameter
```
//PID
double originalSetpoint = 172.50;
double setpoint = originalSetpoint;
double movingAngleOffset = 0.1;
double input, output;


double Kp = 55;   
double Kd = 3;
double Ki = 270;
PID pid(&input, &output, &setpoint, Kp, Ki, Kd, DIRECT);
```
