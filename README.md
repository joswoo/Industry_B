# Industry_B

## Balancing Bot

## Library
- PID
- I2Cdev
- LMotorController
- MPU6050

## Arduino code
### Setting gyro offset
follow this site
http://42bots.com/tutorials/arduino-script-for-mpu-6050-auto-calibration/

### Setting PID parameter
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

## Project Video Link
[![Alt text for your video](https://img.youtube.com/vi/iVVoLgYuxLA/0.jpg)](https://www.youtube.com/watch?v=iVVoLgYuxLA)

[![Watch the video](https://raw.github.com/GabLeRoux/WebMole/master/ressources/WebMole_Youtube_Video.png)](http://youtu.be/vt5fpE0bzSY)
