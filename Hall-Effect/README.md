# Hall-Effect Magnetic Sensor

A Hall-effect sensor detects the presence of a nearby magnet.  The magnet
must be strong, must be oriented in the correct direction, and must be
very close.  Hall-effect sensors can be used to detect a nearby moving part
(with a magnet mounted), without having to contact the moving part.

# What does a Hall-effect sensor look like?

Here's one type of Hall-effect sensor that we use:

![Image of a Hall-effect sensor](./Hall-effect-front.jpg)
![Image of a Hall-effect sensor](./Hall-effect-back.jpg)

This sensor is very small -- even mounted to the circuit board, its maximum
dimensions are 0.75" by 1.25".

# How do Hall-effect sensors work?

You can read about [[the Hall effect](https://en.wikipedia.org/wiki/Hall_effect)]
on Wikipedia.  The short answer is that it has to do with how electrical
current behaves in the presence of a magnetic field.

# How do I wire a Hall-effect sensor?

The sensor has a connection for a 3-wire male Dupont connector.  (Look
carefully -- the holes are on the side edge of the black plastic.)  You'll
need a 3-wire cable with a male Dupont connector on one end, and a female
Dupont connector on the other.  Plug the male end into the sensor, and the
female end into a Digital I/O port on the RoboRIO.

# What are part numbers for Hall-effect sensors we use?

We've qualified the following Hall-effect sensors:

* AndyMark am-3313a Hall-effect magnetic sensor [[specs](https://www.andymark.com/products/hall-effect-sensor-1)] [[vendor link](https://www.andymark.com/products/hall-effect-sensor-1)]
