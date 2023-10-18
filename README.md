# TOOP17 Working with Pololu Motors and Gyro
Now that we can use the OLED and Push Buttons, it's time to make the robot move and turn!

## References
- [Pololu Motor Library Documentation](https://pololu.github.io/pololu-3pi-plus-32u4-arduino-library/class_pololu3pi_plus32_u4_1_1_motors.html)
- [Pololu IMU Library Documentation](https://pololu.github.io/pololu-3pi-plus-32u4-arduino-library/class_pololu3pi_plus32_u4_1_1_i_m_u.html)

## Working with Motors
Your Pololu robot comes with two micro motors. These can be made to turn clockwise or counterclockwise from zero to a maximum speed. The speed of your robot will vary with battery charge.  Like the OLED and Buttons, you must include the Pololu library and create a motor object from the `Motors` class:

`Motors motor`

Here are some of the commands you may frequently use:
```
void flipLeftMotor(bool flip)  //Flips the direction of the left motor
void flipRightMotor(bool flip)  //Flips the direction of the right motor
void setLeftSpeed(int16_t speed)  //Sets the speed for the the left motor
void setRightSpeed(int16_t speed)  //Sets the speed of the right motor
```

## Working with the IMU (Inertial Measurement Unit)
The 3pi+ 32U4 includes on-board inertial sensors that allow it to determine its own orientation by implementing an inertial measurement unit (IMU). The first chip, an ST LSM6DS33, combines a 3-axis accelerometer and 3-axis gyro into a single package. The second chip is an ST LIS3MDL 3-axis magnetometer.

