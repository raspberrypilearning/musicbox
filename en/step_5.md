##A pair of 555s

The control circuit for the music box uses a 556 integrated circuit, which is two 555 timers in a single package. The first 555 is running in Monostable mode and needs a ‘low’ signal to trigger it, but the sensor module provides a ‘high’ signal when it is triggered. To invert this signal we can use a simple transistor switch to connect the input to low and a resistor to pull it high when the transistor is turned off.

The first timer is configured in ‘Monostable’ mode. This means that, once triggered, the output stays high for a period of time before resetting. The period is defined by the resistors and capacitor connected to the threshold and discharge pins. The recommended values will set the period to around 15 seconds, which should be enough for a couple of plays of your music. The trim potentiometer will allow this to be fine-tuned.

When the output of the first timer is high, it will enable the second timer via its reset pin. This is configured in ‘Astable’ mode. In this mode the timer will send out a series of pulses. The frequency of these pulses is defined by the resistors and capacitor connected to the threshold and discharge pins. The trim potentiometer and diode allow the pulse width of these pulses to be adjusted. This is known as pulse-width modulation or PWM and can be used to control the power to the motor and hence the speed of rotation.

As the motor takes more current than the 555 can provide, a power transistor is used to turn the current on and off to the motor.
