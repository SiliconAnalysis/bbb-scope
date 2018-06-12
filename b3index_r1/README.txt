b3index
This is a cape for the BBB that breaks out GPIO to RJ45 connectors
This is intended to drive standalone stepper type drivers such as:
-Compumotor OEM650 stepper driver (15 mA @ 5V?)
-Compumotor M Drive stepper driver (20 mA @ 5V)
-Rorze RD-021M8 stepper driver (up to 15 mA @ 5.5 V)
-Gecko G320X DC servo driver (? mA)
-etc
With control signal (ie optoisolator) current given in parentheses

The reccomended buffer chip (CD74HC4050M96) can drive up to 25 mA,
which is plenty for all of the models I tried

While there are some limited provisions for other use cases,
the goal was to do this and do it well in a small form factor

Connectors are laid out as follows
__   _
| |_| |
| X A |
| Y B |
| Z C |
\_____/

In addition to soldering components you need to set I/O bank output voltages
XYZ and ABC are on separate banks and are configured as follows
-Pin1: 3.3V
-Pin3: 5V
Where pin 1 is the leftmost pad when reading the R text right side up
Controlled as follows:
-XYZ: R13
-ABC: R14

BOM
Digikey qty 1 cart: http://www.digikey.com/short/j9q5w9

