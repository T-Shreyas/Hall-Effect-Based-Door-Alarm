# Hall-Effect-Based-Door-Alarm
# 1. INTRODUCTION

The Hall effect is the production of a voltage difference across an electrical conductor that
is transverse to an electric current in the conductor and to an applied magnetic field perpendicular
to the current. It was discovered by Edwin Hall in 1879. Magnetic contacts are one of the basic
components of electrical security and distress alarm systems (they are mostly used in securing the
object and therefore are only used partially – in the alarm intruder system).

Hall effect-based Door alarm is a very common and useful device for security purpose. They are
used to detect whether the door is opened or closed. When we put the magnet near to the wall or
door frame and the door is closed then the buzzer remains OFF. When we open the door, the door
goes far from the magnet then the buzzer is turned ON. Then it will produce an alarm. This door
alarm technique provides more security to the homes. Also, the installation process is simple and
it can be easily affordable. Hence, this project can be arranged in each and every house.

# 2. SOFTWARE USED:

## NI Multisim (Version 14.2)

## 2.1 PURPOSE OF SELECTING THE SOFTWARE:

Multisim is the most complete and robust circuit design and simulation suite available. It's
format and layout are simple and easy to use. Its component libraries are decent and it's easy to
use. Multisim software combines SPICE simulation and circuit design into an environment
optimized to simplify common design tasks, which helps us improve performance, minimize
errors, and shorten time to prototype. Plus, we got easily all our components required for our mini
project. Especially the Magnetic Flux generator and hall effect sensor which are the vital
components for our project is easily available here along with buzzer.


## 2.2 DESCRIPTION OF SOFTWARE: 
NI Multisim (formerly MultiSIM) is an electronic schematic capture and simulation program which is part of a suite of circuit design
programs, along with NI Ultiboard. Multisim is one of the few circuit design programs to employ
the original Berkeley SPICE based software simulation. Multisim was originally created by a
company named Electronics Workbench Group, which is now a division of National
Instruments. Multisim includes microcontroller simulation (formerly known as MultiMCU), as
well as integrated import and export features to the printed circuit board layout software in the suite, NI Ultiboard.

# 3. IMPLEMENTATION:

## 3.1 COMPONENTS REQUIRED:

### 3 .1.1 HALL EFFECT SENSOR:

Hall Effect Sensors are devices which are activated by an external magnetic field. We
know that a magnetic field has two important characteristics flux density and polarity (North and
South Poles). The output signal from a Hall effect sensor is the function of magnetic field density
around the device. When the magnetic flux density around the sensor exceeds a certain pre-set
threshold, the sensor detects it and generates an output voltage called the Hall Voltage, VH.
Consider the figure 3.1.1 below.

```
Figure3.1.1: hall effect-basic working principal
```
The model which we are using in this project for simulation is OHN3030U Hall effect sensor
where U represents unipolarity condition. A single magnet presenting a south polarity (positive)
magnetic field of sufficient strength (magnetic flux density) will cause the device to switch to its
ON state.


### 3.1.2 RESISTORS AND CAPACITORS:

A resistor is a passive two-terminal electrical component that implements electrical resistance as
a circuit element. In this mini project we have used 1k ohm,150 ohm,470 ohm and 100k ohm
resisters according to our circuit needs. These resisters protect our circuits sensitive components
such as hall effect sensors from high voltage. A capacitor (originally known as a condenser) is a
passive two-terminal electrical component used to store energy electrostatically in an electric field.
We have used a 0.01micro fared capacitor to maintain proper electro-static balance in our circuit.

### 3.1. 3 1N4148 DIODE:

In this project for simulation, we have used 1N4148 Diode which is a standard silicon switching
signal diode. It is one of the most popular and long-lived switching diodes because of its
dependable specifications and low cost. In our project the function of diode is to allow an
electric current to pass in one direction (called the diode's forward direction), while blocking it
in the opposite direction (the reverse direction).

### 3.1.4 BC557 TRANSISTOR:

BC557 is a PNP transistor hence the collector and emitter will be closed (Forward biased) when
the base pin is held at ground and will be opened (Reverse biased) when a signal is provided to
base pin. Its pin diagram is shown in figure 3.1.4.

### 3.1.5 BC547-TRANSISTOR:

The BC547 transistor is an NPN transistor. A small current of the base terminal of
this transistor will control the large current of emitter and base terminals. The main function of
this transistor is to amplify as well as switching purposes. The maximum gain current of
this transistor is 800A. In our case this transistor is mainly for switching purpose.

### 3.1.6 4V 0.5-WATT BULB:

Here we are using a 4V/0.5-watt bulb along with the buzzer circuit. The fixture does not use
power when it is turned off, with the exception of external controls, whose power should not
exceed 0.5 watts in the off state. If it does the bulb blows off as a result of which the buzzer gets
triggered.

### 3.1. 7 BUZZER:

A buzzer or beeper is an audio signalling device, which may be mechanical, electromechanical,
or piezoelectric (piezo for short). Typical uses of buzzers and beepers include alarm devices,
timers, and confirmation of user input such as a mouse click or keystroke. We are using this
buzzer for burglar alarm in our project.

### 3.1.8 JUMPING WIRES:

We are also required to use the jumping wires so that the internal connection between the
different components could be established.

### 3.1.9 BAR MAGNET:

The major component of our project is Bar Magnet. In simulation instead of bar magnet we are
using magnetic flux generator.

Magnetic flux is a measurement of the total magnetic field which passes through a given area. It
is a useful tool for helping describe the effects of the magnetic force on something occupying a
given area. The measurement of magnetic flux is tied to the particular area chosen. The hall
effect sensor senses this flux and according to which we obtain our results.

## 3.2 DESIGNED CIRCUIT IN MULTISIM:

```
Figure 3.2: CIRCUIT DIAGRAM
```

## 3. 3 IMPLIMENTATION CONCEPT:

Place the Alarm circuit connected to the AC power supply and make sure the expose hall effect
sensor OHN3030U to Magnet attached with door when the door is closed.

```
Figure 3.3: hardware implementation circuit
```
## 3. 4 PROCEDURE:

First, we have to rig up the circuit as shown in Figure 3.2. According to which the terminal 3 of
the Hall Effect sensor is connected to the Base of the PNP Transistor BC557AP and further the
collector of the BC557AP is connected to the base of NPN transistor BC547BG.Further the Buzzer
is connected across the bulb along with an ammeter (because without establishing connection with
the ammeter the buzzer won’t work in multisim platform).Then after adding all the resistors in
between finally we should connect our circuit with the AC supply of 230V/50Hz(Domestic supply)
through a switch. And finally, we have to adjust the position the Bar magnet with our circuit in
such a way that the south pole of our magnet faces the front side of the Hall effect sensor as
previously mentioned the hall effect sensor is sensitive to polarity. Once our circuit is all set, we
have to trigger it by just pressing the switch and the circuit becomes active. It’s hardware
implementation concept is clearly depicted in Figure 3.4.


# 4. RESULT ANALYSIS:

## 4.1 PRACTICAL RESULT ANALYSIS:

### 4.1.1 CIRCUIT OPERATION:

When we put magnate near Hall Sensor then hall sensor senses the magnetic field and
generates a Low signal as an output. This output goes to the base of the transistor. Due to Low
signal, transistor remains turned off and power is not supplied to the 0.5w bulb and buzzer remains
silent. This proves the fact that the door is closed as magnet is still close to our circuit.

Now when we take magnet far from the hall sensor then hall sensor generates a high signal which
goes to the base of the transistor. This happens because the hall effect sensor produces signals
based on the polarity of the magnet. This device works on the principle of halls effect according
to which, the voltage will be perpendicular to the current flowing through a semiconductor or a
conductor. Further on receiving high signal transistor gets turned on and make a path for Power
supply. Further the diode corrects the supply path to pass through the bulb, which in turn cannot
resist the power supply which is greater than 0.5W, breaks apart triggering the Buzzer to turn on
and alert the Householders of the Burglar activity. And The user can also change the frequency of
Buzzer tone according to his needs.

In the above simulation we infer that when the door is closed the magnet will be experiencing a
magnetic flux of magnitude 210 and as soon as the door opens there will be a decrease is the
magnetic field and as soon as it reaches 160 the alarm will go on through the buzzer placed in the
circuit

### 4.1.2 CONCLUSION:

This project gives a conclusion that the type of alarm system used here is based on Hall
effect. The main objective of the simulation project is to maintain safety of a house while no one
is present. If there is any emergency which needs to be attended soon and the house is left alone,
the hall effect door alarm comes into picture. If any burglar tries to break into the house without
keys, then the magnetic field variation would put on the alarm and it would indicate to the nearby
houses that the house is being broken and that the can inform the police about it.

The main inference is that using a hall effect sensor which increases or decreases the current
flowing in the circuit is the main component of this circuit.


### 4.1.3 ADVANTAGES:

o They can be used for multiple sensor functions like position sensing, speed sensing
as well as for sensing the direction of movement too.

o As they are solid state devices, there is absolutely no wear and tear due to absence
of moving parts.

o They are almost maintenance free.

o They are robust.

o They are immune to vibration, dust and water.

### 4.1.4 DISADVANTAGES:


o They are not capable to measure current flow at a distance more than 10 cm. The
only solution to overcome this issue is to use a very strong magnet that can generate
a wide magnetic field.


o Accuracy of the measured value is always a concern as external magnetic fields may
affect the values.

o High Temperature affects the conductor resistance. This will in turn affect the
charge carrier’s mobility and sensitivity of Hall Effect Sensors.

### 4.1.5 APPLICATION:

- Siren Annunciation
- Magnetic Door Release
- Border security control and defence purposes.
- Security systems in banking sectors such as lockers or safes.
- Small Motor Control
- Prisons/Jails and Zoological gardens.
- In SMART Homes as Door Tamper Alarm


# 5.REFERENCES:

1. Y Lavanya, Ch B K Rajeswari, SS Sriharsha, K Umeshchandra and K YR Prathyusha,
    DOOR ALARM USING HALL EFFECT SENSOR, 2019 Journal of Emerging
    Technologies and Innovative Research, June 2019, Volume 6, Issue 6.
2. Bilotti, A., Monreal, G., & Vig, R. (1997). Monolithic magnetic Hall sensor using
    dynamic quadrature offset cancellation. IEEE Journal of Solid-State Circuits, 829-836.
3. https://circuitdigest.com/
4. https://www.instructables.com/
5. https://electronicsforu.com/
