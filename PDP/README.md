# Sensors in the Power Distribution Panel (PDP)

The Power Distribution Panel (PDP) is primarily responsible for distributing
electrical power from the battery to the various robot subsystems, but it
also has internal sensors that we can get information from over the CAN bus.
These internal sensors measure current and power to each "channel" (output
connection, numbered 1-16) as well as the total current and power used by
everything.

# What are the limitations of the PDP's sensors?

The PDP's current sensors are very coarse.  They only measure currents over
about 2 amps.  Even a large motor like a Falcon 500, running unloaded at
20% output, will register as 0 amps and 0 watts to the PDP's sensors.  (That
use case is probably pulling about 2 amps.  Needless to say, low-power devices
such as sensors and the roboRIO itself won't register as drawing any power
from the PDP.)

# What can a coarse current/power reading tell us?

The main power draw on the battery will always be motors under load.  While
the PDP's sensors won't be able to track all power usage from the battery,
the sensors will detect the largest power draws.  If we want, we can track
power usage, either total or by channel, as part of our periodic functions,
and note when power usage spikes.  This could help us figure out what we're
doing to cause that, and therefore help avoid brownouts.

(Of course, a more reliable way to avoid brownouts is to tell the motor
controllers to limit the amount of current that their motors are allowed to
draw.  This can be done either by configuring them using tools like Phoenix
Tuner or the REV Hardware Configuration Tool, or in software by using methods
of the motor controllers to set current limits.)
